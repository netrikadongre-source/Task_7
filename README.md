# Task 7 - Monitor System Resources Using Netdata

## Objective
Install and run Netdata to monitor system and application performance metrics in real-time using Docker.

---

## Steps Followed

1. **Pulled and ran Netdata in Docker**:
   ```bash
   docker run -d --name=netdata \
     -p 19999:19999 \
     --cap-add SYS_PTRACE \
     --security-opt apparmor=unconfined \
     netdata/netdata
   ```
   
---

2. **Accessed the Dashboard**:
   Opened the browser and visited:
   ```
   http://localhost:19999
   ```
   Viewed live CPU, memory, disk, and Docker container metrics.

---

3. **Collected Logs from Netdata Containe**:
   ```bash
   docker exec netdata cat /var/log/netdata/error.log > logs/error.log
   docker exec netdata cat /var/log/netdata/access.log > logs/access.log
   ```

---

## Outcome / Learnings
   - Understood how to monitor system resources in real-time with Netdata.
   - Learned how to run monitoring tools inside Docker.
   - Collected and viewed Netdata logs for troubleshooting and insights.

---

## Tools Used
   - Docker for containerizing Netdata.
   - Netdata (open-source monitoring tool).

---

## Author

**Netrika Dongre**
- GitHub: `netrikadongre-source`
- DockerHub: `netrika0210`
   

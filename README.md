# NFS Configuration

NFS (Network File System) is a network file sharing protocol that defines the way files are stored and retrieved from storage devices across networks. This role is designed to automate the setup and configuration of NFS Server and Client.

---

## Requirements

- At least two servers:
  - One server for the **NFS server** setup.
  - One or more servers for the **NFS client** setup.
- Supported operating system:
  - **RedHat-based distributions** (e.g., CentOS, RHEL).

---

## Role Variables

The following variables can be defined for the role:

1. **Defined in `vars/main.yml`:**
   - `nfs_server_ip` - The IP address of the NFS server.
   - `nfs_server_dir` - The directory on the server that will be shared.
   - `nfs_client_ip` - The IP address of the NFS client.
   - `nfs_client_dir` - The directory on the client where the NFS share will be mounted.

   Example:
   ```yaml
   nfs_server_ip: 192.168.1.10
   nfs_server_dir: /nfs/server
   nfs_client_ip: 192.168.1.20
   nfs_client_dir: /nfs/client

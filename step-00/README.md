# Ansible Fundamentals

## Requirements

### 1. What is Ansible?

Research and answer:

- What is Ansible?
**Ansible** là một công cụ CNTT mã nguồn mở tự động hóa việc triển khai ứng dụng, cung cấp dịch vụ đám mây, điều phối nội bộ dịch vụ và các công cụ CNTT khác. 

- What problems does Ansible solve?
  - Triển khai phần mềm trên nhiều máy chủ cùng một lúc mà không cần sự can thiệp của con người
  - Sử dụng cấu hình máy chủ và tạo tài khoản người dùng
  - Không cần agent, không cần các phần mềm trên các node, sử dụng SSH để kết nối với các node và thực hieenjc ác thao tác cần thiết trên máy chủ
  
- How Ansible works at a high level ?
  - Control Node: máy đã cài Ansible và chạy các lệnh tự động hóa
  - Inventory: danh sách các máy sẽ được quản lý
  - Playbooks: File `yaml` định nghĩa các quy trình tự động
  - Task & Modules: các bước tự động hóa (tasks) được thực thi bằng các module nhỏ
  - Execution: Ansible kết nối qua SSH tới máy đích và chạy các module để thực hiện nhiệm vụ

### 2. Why Ansible?

Research and explain:

- Why Ansible is used in system administration.
- Advantages of Ansible compared to manual configuration.
  - 
- Use cases where Ansible is appropriate.

### 3. Core Ansible Terms

Terms to research:

- Inventory
- Host
- Playbook
- Play
- Task
- Module
- Library

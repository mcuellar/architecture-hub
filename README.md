# Architecture Hub

A repository for cloud architecture diagrams and documentation.

## AWS Web Application Architecture

This repository contains a secure, resilient, and fault-tolerant AWS web application architecture diagram that demonstrates best practices for building production-ready applications on AWS.

### Architecture Overview

The architecture diagram (`aws-web-app-architecture.drawio`) includes the following components:

#### **Frontend Layer**
- **Route 53**: DNS service for domain name resolution with health checks and failover
- **CloudFront**: Content Delivery Network (CDN) for global content distribution and caching
- **S3**: Storage for static content (HTML, CSS, JavaScript, images)
- **WAF (Web Application Firewall)**: Protection against common web exploits and attacks

#### **Application Layer**
- **Application Load Balancer (ALB)**: Distributes incoming traffic across multiple targets
- **Auto Scaling Groups**: Automatically scales EC2 instances across multiple Availability Zones
- **VPC**: Isolated network environment with public and private subnets
- **NAT Gateways**: Enable instances in private subnets to access the internet

#### **Database Layer**
- **Amazon RDS (Multi-AZ)**: Managed relational database with automatic failover
- **Primary and Standby instances**: Synchronous replication across Availability Zones

#### **Security & Monitoring**
- **Security Groups**: Firewall rules controlling inbound and outbound traffic
- **Secrets Manager**: Secure storage and rotation of database credentials
- **CloudWatch**: Monitoring, logging, and alerting for all resources

### Key Features

**High Availability**: Deployed across multiple Availability Zones (AZs)  
**Fault Tolerance**: Multi-AZ RDS with automatic failover, redundant NAT Gateways  
**Auto Scaling**: Automatic capacity adjustment based on demand  
**Security**: WAF protection, private subnets, security groups, encrypted credentials  
**Resilience**: Load balancing, health checks, and redundant infrastructure  
**Monitoring**: CloudWatch for comprehensive observability  

## Setting Up Draw.io in VSCode

To view and edit the architecture diagrams in this repository, you'll need to install the Draw.io Integration extension in Visual Studio Code.

### Installation Steps

1. **Open Visual Studio Code**

2. **Install the Draw.io Integration Extension**
   - Press `Ctrl+Shift+X` (Windows/Linux) or `Cmd+Shift+X` (Mac) to open the Extensions view
   - Search for "Draw.io Integration" or "hediet.vscode-drawio"
   - Click **Install** on the extension by Henning Dieterichs

   Alternatively, you can install via command line:
   ```bash
   code --install-extension hediet.vscode-drawio
   ```

3. **Verify Installation**
   - After installation, you should see the Draw.io Integration extension in your installed extensions list
   - The extension supports `.drawio`, `.dio`, `.drawio.svg`, and `.drawio.png` file formats

### Using Draw.io in VSCode

#### Opening a Diagram

1. **Navigate to the diagram file** in the VSCode Explorer
   - For this repository: `aws-web-app-architecture.drawio`

2. **Open the file**
   - Simply click on the `.drawio` file
   - VSCode will automatically open it with the Draw.io editor

#### Editing a Diagram

Once the diagram is open:

1. **Select elements**: Click on any shape or connector
2. **Move elements**: Click and drag selected elements
3. **Edit text**: Double-click on shapes to edit their labels
4. **Add new shapes**: 
   - Use the shape panel on the left side
   - Search for AWS icons, shapes, or connectors
   - Drag and drop onto the canvas

5. **Connect elements**:
   - Hover over a shape until connection points appear (small 'x' marks)
   - Click and drag from one connection point to another

6. **Format elements**:
   - Select an element
   - Use the format panel on the right to change colors, fonts, and styles

7. **Zoom and pan**:
   - Zoom: Use `Ctrl/Cmd + Mouse Wheel` or the zoom controls
   - Pan: Hold `Space` and drag, or use scroll bars

#### Saving Changes

- **Auto-save**: The extension auto-saves your changes when you modify the diagram
- **Manual save**: Press `Ctrl+S` (Windows/Linux) or `Cmd+S` (Mac)
- Changes are saved directly to the `.drawio` file

#### Exporting Diagrams

While the extension primarily works with `.drawio` files, you can export to other formats:

1. Open the diagram in VSCode
2. Use the Draw.io menu (typically accessible via right-click or the command palette)
3. Export options may include PNG, SVG, PDF, and HTML

Alternatively, you can use the desktop version of Draw.io (https://www.drawio.com/) to open the file and export to various formats.

### Tips and Tricks

- **Command Palette**: Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (Mac) and type "Draw.io" to see all available commands
- **Multiple pages**: Draw.io files can contain multiple pages (tabs) - use the tabs at the bottom of the editor
- **Grid and guides**: Enable grid snapping for better alignment (View menu in Draw.io)
- **AWS shapes**: Search for "aws" in the shapes panel to find AWS-specific icons
- **Undo/Redo**: Use `Ctrl+Z`/`Ctrl+Y` (Windows/Linux) or `Cmd+Z`/`Cmd+Shift+Z` (Mac)

### Troubleshooting

**Issue**: Diagram doesn't open or shows as XML text  
**Solution**: Ensure the Draw.io Integration extension is installed and enabled

**Issue**: Can't find AWS shapes  
**Solution**: In the shapes panel, click "More Shapes" and enable the AWS architecture library

**Issue**: Changes aren't saving  
**Solution**: Check file permissions and ensure VSCode has write access to the repository folder

## Additional Resources

- [Draw.io VSCode Extension Documentation](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio)
- [Draw.io Official Website](https://www.drawio.com/)
- [AWS Architecture Icons](https://aws.amazon.com/architecture/icons/)
- [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/)

## Contributing

Feel free to submit improvements to the architecture diagrams or documentation via pull requests.

## License

This repository is provided as-is for educational and reference purposes.
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
<p>This guide covers the steps needed to configure osTicket after installation, transforming the open-source help desk ticketing system from its initial state into a fully functioning, production ready platform for handling real support tickets.</p>

<h2>Environments and Technologies Used</h2>
<p>The following environments and technologies are used:</p>
<ul>
  <li><strong>Microsoft Azure:</strong> Provides the virtual machine and cloud compute resources used to host the osTicket installation.</li>
  <li><strong>Remote Desktop:</strong> Enables secure remote access to the virtual machine for configuring and managing osTicket.</li>
  <li><strong>Internet Information Services (IIS):</strong> The web server software running on Windows that hosts and serves the osTicket web application.</li>
</ul>

<h2>Operating Systems Used</h2>
<p>The following operating system was utilized:</p>
<ul>
  <li><strong>Windows 10 :</strong> The operating system running on the virtual machine, used to host the IIS server and osTicket application.</li>
</ul>

<h2>Configuration:</h2>
<p><strong>Objective:</strong> The objective in this section is to move osTicket beyond its basic installation and into a fully operational system capable of managing tickets, handling user requests, and supporting staff assignments.</p>

<h3>Overview: Set up and Configure Key Components</h3>
<p>Here we'll configure important components within osTicket to ensure it functions effectively such as:</p>
<ul>
  <li><strong>Roles:</strong> Defines what each agent is permitted to do in the system — for example, Admins have full access, while Support Staff may be limited to responding to tickets.</li>
  <li><strong>Departments:</strong> Groups tickets by category (e.g., IT, Customer Support) so they're routed to the team best suited to handle them.</li>
  <li><strong>Teams:</strong> Groups of agents assigned to a specific support tier (e.g., Level I, Level II), used to structure how tickets get escalated when they can't be resolved at the first level.</li>
  <li><strong>Agents (Workers):</strong> Staff accounts used to view, respond to, and resolve tickets.</li>
  <li><strong>Users (Customers):</strong> The accounts belonging to the people submitting support requests such as an end user.</li>
  <li><strong>SLAs (Service Level Agreements):</strong> Rules that set expected response and resolution times based on how urgent a ticket is.</li>
  <li><strong>Help Desk Topics:</strong> Categories a user selects when submitting a ticket, which can also be used to automatically route it to the right department.</li>
</ul>

<h3>Outline</h3>

<ul>
  <li><strong>Configure Roles</strong>
    <ul>
      <li>Navigate to Admin Panel to Agents to Roles</li>
      <li>Set the "Supreme Admin" role for full administrative control.</li>
    </ul>
  </li>
  
  <li><strong>Configure Departments</strong>
    <ul>
      <li>Navigate to Admin Panel to Agents to Departments</li>
      <li>Make a department named "SysAdmins" to handle system-level issues (used to separate ticket visibility between Help Desk, SysAdmins, and Networking).</li>
    </ul>
  </li>
  
  <li><strong>Configure Teams</strong>
    <ul>
      <li>Navigate to Admin Panel to Agents to Teams</li>
      <li>Teams pull agents from different departments. Set up a team called "Online Banking" to handle that specific area of support.</li>
    </ul>
  </li>
  
  <li><strong>Allow Anyone to Create Tickets</strong>
    <ul>
      <li>Navigate to Admin Panel to Settings to User Settings</li>
      <li>Uncheck "Registration Required" so unregistered users are able to create tickets without first logging in.</li>
    </ul>
  </li>
  
  <li><strong>Configure Agents (Workers)</strong>
    <ul>
      <li>Navigate to Admin Panel to Agents to Add New</li>
      <li>Add agents like "Eric(Dept:SysAdmins)" and "Alex(Dept:Support" to handle incoming tickets.</li>
    </ul>
  </li>
  
  <li><strong>Configure Users (Customers)</strong>
    <ul>
      <li>Navigate to Agent Panel to Users to Add New</li>
      <li>Add users like "Marcelo" and "Luis" who will submit tickets for support.</li>
    </ul>
  </li>

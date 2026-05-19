<%@ Master Language="C#" AutoEventWireup="true" CodeBehind="Site.Master.cs" Inherits="YourProject.SiteMaster" %>

<%@ Register Src="~/UserControls/Header.ascx" TagPrefix="uc1" TagName="Header" %>

<!DOCTYPE html>
<html>
<head runat="server">
    <title>My Website</title>

    <style>
        body { font-family: Arial; margin:0; }

        .menu {
            background: black;
            padding: 15px;
        }

        .menu a {
            color: white;
            margin: 15px;
            text-decoration: none;
            font-size: 18px;
        }

        .menu a:hover {
            color: yellow;
        }

        .content {
            padding: 20px;
        }
    </style>
</head>

<body>
<form runat="server">

    <!-- USER CONTROL -->
    <uc1:Header ID="Header1" runat="server" />

    <!-- MENU -->
    <div class="menu">
        <a href="Default.aspx">Home</a>
        <a href="About.aspx">About</a>
        <a href="Contact.aspx">Contact</a>
    </div>

    <!-- CONTENT -->
    <div class="content">
        <asp:ContentPlaceHolder ID="MainContent" runat="server" />
    </div>

</form>
</body>
</html>

<%@ Control Language="C#" AutoEventWireup="true" CodeBehind="Header.ascx.cs" Inherits="YourProject.Header" %>

<div style="background: orange; padding: 20px; text-align:center;">
    <h1>☕ My Cafe Website</h1>
</div>

<%@ Page Title="Home" Language="C#" MasterPageFile="~/Site.Master" AutoEventWireup="true" %>

<asp:Content ContentPlaceHolderID="MainContent" runat="server">
    <h2>Welcome to Home Page</h2>
</asp:Content>

<%@ Page Title="About" Language="C#" MasterPageFile="~/Site.Master" AutoEventWireup="true" %>

<asp:Content ContentPlaceHolderID="MainContent" runat="server">
    <h2>About Us</h2>
</asp:Content>

<%@ Page Title="Contact" Language="C#" MasterPageFile="~/Site.Master" AutoEventWireup="true" %>

<asp:Content ContentPlaceHolderID="MainContent" runat="server">
    <h2>Contact Page</h2>
</asp:Content>

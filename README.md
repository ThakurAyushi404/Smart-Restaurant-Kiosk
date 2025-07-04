# 🍽️ Smart Restaurant Kiosk System

This repository presents an overview of the **Kiosk system** I built using **ASP.NET Core MVC**, **Web API**, **JavaScript**, and **Bootstrap**. It is used for contactless ordering, real-time payment integration, and customized item selection.

> ⚠️ This repository contains **only selected code and design previews** to protect project integrity. Full project access is restricted for IP and security reasons.

## 📸 Preview

<p align="center">
    <img src="Resturant-kiosk\Home-1.jpg" width="300"/>
  <img src="Resturant-kiosk\Menu.jpg" width="300"/>
     <img src="Resturant-kiosk\Description1.jpg" width="300"/>
  <img src="Resturant-kiosk\Promotions-popup.jpg" width="300"/>
  <img src="Resturant-kiosk\Thank You-1.jpg" width="300"/>
 

</p>

## 🛠️ Tech Stack

- ASP.NET Core MVC
- Entity Framework
- Razor Views
- JavaScript + jQuery
- Bootstrap
- SQL Server
- Integration: Eftpos (Payment), QR receipts

## 🧪 Sample Code Snippet

```csharp
// Sample controller action
public IActionResult ComboDetail(string itemId)
{
    var item = _context.Items.Include(i => i.Instructions)
                             .FirstOrDefault(i => i.ItemId == itemId);
    return View(item);
}

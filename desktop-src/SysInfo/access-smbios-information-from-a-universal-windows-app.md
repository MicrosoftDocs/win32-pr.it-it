---
description: Come accedere alle informazioni di System Management BIOS (SMBIOS) da un'app di Windows universale.
ms.assetid: 4D185319-C093-4B1B-A182-E845E72FEA5D
title: Accedere alle informazioni di SMBIOS da un'app di Windows universale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76791622ad4bcba15ddd889f36a6f0feeb5e3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529317"
---
# <a name="access-smbios-information-from-a-universal-windows-app"></a><span data-ttu-id="d1186-103">Accedere alle informazioni di SMBIOS da un'app di Windows universale</span><span class="sxs-lookup"><span data-stu-id="d1186-103">Access SMBIOS information from a Universal Windows App</span></span>

> <span data-ttu-id="d1186-104">Si noti Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="d1186-104">[NOTE] Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d1186-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.</span><span class="sxs-lookup"><span data-stu-id="d1186-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="d1186-106">Come accedere alle informazioni di System Management BIOS (SMBIOS) da un'app di Windows universale.</span><span class="sxs-lookup"><span data-stu-id="d1186-106">How to access System Management BIOS (SMBIOS) information from a Universal Windows app.</span></span>

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a><span data-ttu-id="d1186-107">Accedere alle informazioni di SMBIOS da un'app piattaforma UWP (Universal Windows Platform)</span><span class="sxs-lookup"><span data-stu-id="d1186-107">Access SMBIOS information from a Universal Windows Platform App</span></span>

<span data-ttu-id="d1186-108">A partire da Windows 10, versione 1803, le app di Windows universale possono usare [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) e [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) per accedere alle informazioni SMBIOS dichiarando la funzionalità limitata **SMBIOS** nel manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d1186-108">Starting with Windows 10, version 1803, Universal Windows apps can use [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) and [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) to access SMBIOS information by declaring the **smbios** restricted capability in the app manifest.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1186-109">Solo l'accesso alle tabelle del firmware SMBIOS (RSMB) non elaborate è supportato da un'app di Windows universale.</span><span class="sxs-lookup"><span data-stu-id="d1186-109">Only access to raw SMBIOS (RSMB) firmware tables is supported from a Universal Windows app.</span></span> <span data-ttu-id="d1186-110">**Accesso \_ a** Se si tenta di accedere ad altri tipi di tabella del firmware da un'app di Windows universale, viene restituito negato.</span><span class="sxs-lookup"><span data-stu-id="d1186-110">**ACCESS\_DENIED** will be returned if you try to access other firmware table types from a Universal Windows app.</span></span>

 

<span data-ttu-id="d1186-111">Per dichiarare la funzionalità con restrizioni **SMBIOS** nel manifesto dell'applicazione, aggiungere lo spazio dei nomi **rescap** e la funzionalità **SMBIOS** come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="d1186-111">To declare the **smbios** restricted capability in the app manifest, add the **rescap** namespace and **smbios** capability as follows:</span></span>

``` syntax
<Package
  ...
  xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
  IgnorableNamespaces="uap mp rescap">  
  ...
  <Capabilities>
    <rescap:Capability Name="smbios"/>
  </Capabilities>
</Package>
```

## <a name="related-topics"></a><span data-ttu-id="d1186-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1186-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1186-113">Funzionalità speciali e con restrizioni</span><span class="sxs-lookup"><span data-stu-id="d1186-113">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="d1186-114">GetSystemFirmwareTable</span><span class="sxs-lookup"><span data-stu-id="d1186-114">GetSystemFirmwareTable</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[<span data-ttu-id="d1186-115">EnumSystemFirmwareTables</span><span class="sxs-lookup"><span data-stu-id="d1186-115">EnumSystemFirmwareTables</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[<span data-ttu-id="d1186-116">Accedere alle variabili del firmware UEFI da un'app di Windows universale</span><span class="sxs-lookup"><span data-stu-id="d1186-116">Access UEFI firmware variables from a Universal Windows App</span></span>](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 

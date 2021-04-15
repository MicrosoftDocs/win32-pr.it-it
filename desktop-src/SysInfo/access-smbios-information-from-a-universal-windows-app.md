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
# <a name="access-smbios-information-from-a-universal-windows-app"></a>Accedere alle informazioni di SMBIOS da un'app di Windows universale

> Si noti Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.

Come accedere alle informazioni di System Management BIOS (SMBIOS) da un'app di Windows universale.

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a>Accedere alle informazioni di SMBIOS da un'app piattaforma UWP (Universal Windows Platform)

A partire da Windows 10, versione 1803, le app di Windows universale possono usare [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) e [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) per accedere alle informazioni SMBIOS dichiarando la funzionalità limitata **SMBIOS** nel manifesto dell'applicazione.

> [!IMPORTANT]
> Solo l'accesso alle tabelle del firmware SMBIOS (RSMB) non elaborate è supportato da un'app di Windows universale. **Accesso \_ a** Se si tenta di accedere ad altri tipi di tabella del firmware da un'app di Windows universale, viene restituito negato.

 

Per dichiarare la funzionalità con restrizioni **SMBIOS** nel manifesto dell'applicazione, aggiungere lo spazio dei nomi **rescap** e la funzionalità **SMBIOS** come indicato di seguito:

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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzionalità speciali e con restrizioni](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[Accedere alle variabili del firmware UEFI da un'app di Windows universale](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 

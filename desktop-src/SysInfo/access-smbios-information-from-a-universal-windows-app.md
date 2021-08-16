---
description: Come accedere alle informazioni DEL BIOS (System Management BIOS) da un'app Windows universali.
ms.assetid: 4D185319-C093-4B1B-A182-E845E72FEA5D
title: Accedere alle informazioni SMBIOS da un'app Windows universale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936d30a653059b3573e962b2e52770aa2bd000180ee0612c1855de3d6a1a9778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764955"
---
# <a name="access-smbios-information-from-a-universal-windows-app"></a>Accedere alle informazioni SMBIOS da un'app Windows universale

> [NOTA] Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.

Come accedere alle informazioni DEL BIOS (System Management BIOS) da un'app Windows universali.

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a>Accedere alle informazioni SMBIOS da un'app della Windows universali

A partire da Windows 10, versione 1803, le app Universal Windows possono usare [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) ed [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) per accedere alle informazioni SMBIOS dichiarando la funzionalità con restrizioni **smbios** nel manifesto dell'app.

> [!IMPORTANT]
> Da un'app Universal Windows è supportato solo l'accesso alle tabelle firmware SMBIOS (RSMB) non elaborati. **ACCESSO \_ DENIED verrà** restituito se si tenta di accedere ad altri tipi di tabella del firmware da un'app Windows universale.

 

Per dichiarare la **funzionalità smbios** con restrizioni nel manifesto dell'app, aggiungere lo spazio dei nomi **rescap** e la funzionalità **smbios** come indicato di seguito:

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

[Accedere alle variabili del firmware UEFI da un'app Windows universale](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 

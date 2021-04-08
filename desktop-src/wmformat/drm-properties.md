---
title: Proprietà DRM
description: Proprietà DRM
ms.assetid: 862fc8bc-6e40-4496-862a-c12c8a382116
keywords:
- Windows Media Format SDK, proprietà DRM
- ASF (Advanced Systems Format), proprietà DRM
- ASF (Advanced Systems Format), proprietà DRM
- Digital Rights Management (DRM), proprietà
- DRM (Digital Rights Management), proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb8542d360c38ab3f12406462cefc0454e7eae33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045376"
---
# <a name="drm-properties"></a>Proprietà DRM

La tabella seguente elenca le proprietà DRM che le applicazioni possono ottenere o impostare durante la scrittura o la lettura di file protetti. Queste proprietà non sono attributi di file. non vengono scritte nell'intestazione del file ASF.



| Proprietà DRM                                                                             | Identificatore globale                               | Tipo di dati             |
|------------------------------------------------------------------------------------------|-------------------------------------------------|-----------------------|
| [**\_ACTIONALLOWED DRM**](drm-actionallowed.md)                                          | g \_ wszWMDRM \_ ActionAllowed                      | **\_tipo WMT \_ bool**   |
| [**\_Backup ACTIONALLOWED \_ DRM**](drm-actionallowed-backup.md)                           | g \_ wszWMDRM \_ ActionAllowed \_ backup              | **\_tipo WMT \_ bool**   |
| [**\_CollaborativePlay ACTIONALLOWED \_ DRM**](drm-actionallowed-collaborativeplay.md)     | g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay   | **\_tipo WMT \_ bool**   |
| [**\_Copia di ACTIONALLOWED DRM \_**](drm-actionallowed-copy.md)                               | g \_ wszWMDRM \_ ActionAllowed \_ Copy                | **\_tipo WMT \_ bool**   |
| [**\_CopyToCD ACTIONALLOWED \_ DRM**](drm-actionallowed-copytocd.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD            | **\_tipo WMT \_ bool**   |
| [**\_CopyToNonSDMIDevice ACTIONALLOWED \_ DRM**](drm-actionallowed-copytononsdmidevice.md) | g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice | **\_tipo WMT \_ bool**   |
| [**\_CopyToSDMIDevice ACTIONALLOWED \_ DRM**](drm-actionallowed-copytosdmidevice.md)       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice    | **\_tipo WMT \_ bool**   |
| [**\_Riproduzione ACTIONALLOWED \_ DRM**](drm-actionallowed-playback.md)                       | \_ \_ riproduzione ActionAllowed g \_ wszWMDRM            | **\_tipo WMT \_ bool**   |
| [**\_PlaylistBurn ACTIONALLOWED \_ DRM**](drm-actionallowed-playlistburn.md)               | g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn        | **\_tipo WMT \_ bool**   |
| [**\_BASELICENSEACQURL DRM**](drm-baselicenseacqurl.md)                                  | g \_ wszWMDRM \_ BaseLicenseAcqURL                  | **\_stringa di tipo WMT \_** |
| [**\_Flag DRM**](drm-flags.md)                                                          | \_flag g wszWMDRM \_                              | **WMT \_ tipo \_ DWORD**  |
| [**\_HEADERSIGNPRIVKEY DRM**](drm-headersignprivkey.md)                                  | g \_ wszWMDRM \_ HeaderSignPrivKey                  | **\_stringa di tipo WMT \_** |
| [**\_ISDRM DRM**](drm-isdrm.md)                                                          | g \_ wszIsDRM                                     | **\_tipo WMT \_ bool**   |
| [**\_ISDRMCACHED DRM**](drm-isdrmcached.md)                                              | g \_ wszIsDRMCached                               | **\_tipo WMT \_ bool**   |
| [**Valore di inizializzazione del valore DRM \_**](drm-keyseed.md)                                                      | valore \_ di \_ inizializzazione g wszWMDRM                            | **\_stringa di tipo WMT \_** |
| [**\_Livello DRM**](drm-level.md)                                                          | \_livello g wszWMDRM \_                              | **WMT \_ tipo \_ DWORD**  |
| [**\_LICENSEID DRM**](drm-licenseid.md)                                                  | g \_ wszWMDRM \_ LicenseID                          | **\_stringa di tipo WMT \_** |
| [**\_LICENSESTATE DRM**](drm-licensestate.md)                                            | g \_ wszWMDRM \_ LicenseState                       | **WMT \_ tipo \_ DWORD**  |
| [**\_CollaborativePlay LICENSESTATE \_ DRM**](drm-licensestate-collaborativeplay.md)       | g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | **\_binario di tipo WMT \_** |
| [**\_Copia di LICENSESTATE DRM \_**](drm-licensestate-copy.md)                                 | g \_ wszWMDRM \_ LicenseState \_ Copy                 | **\_binario di tipo WMT \_** |
| [**\_CopyToCD LICENSESTATE \_ DRM**](drm-licensestate-copytocd.md)                         | g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | **\_binario di tipo WMT \_** |
| [**\_CopyToSDMIDevice LICENSESTATE \_ DRM**](drm-licensestate-copytosdmidevice.md)         | g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | **\_binario di tipo WMT \_** |
| [**\_CopyToNonSDMIDevice LICENSESTATE \_ DRM**](drm-licensestate-copytononsdmidevice.md)   | g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | **\_binario di tipo WMT \_** |
| [**\_Riproduzione LICENSESTATE \_ DRM**](drm-licensestate-playback.md)                         | \_ \_ riproduzione LicenseState g \_ wszWMDRM             | **\_binario di tipo WMT \_** |
| [**\_PlaylistBurn LICENSESTATE \_ DRM**](drm-licensestate-playlistburn.md)                 | g \_ wszWMDRM \_ LicenseState \_ PlaylistBurn         | **\_binario di tipo WMT \_** |
| [**\_Diritti DRM**](drm-rights.md)                                                        | \_diritti g wszWMDRM \_                             | **\_stringa di tipo WMT \_** |
| [**\_SAPLEVEL DRM**](drm-saplevel--deprecated.md)                                        | g \_ wszWMDRM \_ SAPLEVEL                           | **\_stringa di tipo WMT \_** |
| [**USA \_ \_ DRM avanzato**](use-advanced-drm.md)                                           | g \_ wszWMUse \_ Advanced \_ DRM                      | **\_tipo WMT \_ bool**   |
| [**USA \_ DRM**](use-drm.md)                                                              | g \_ wszWMUse \_ DRM                                | **\_tipo WMT \_ bool**   |
| [**\_Revoca WMDRMNET**](wmdrmnet-revocation.md)                                      | \_revoca g wszWMDRMNET \_                      | **\_stringa di tipo WMT \_** |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Elenco attributi DRM**](drm-attribute-list.md)
</dt> </dl>

 

 





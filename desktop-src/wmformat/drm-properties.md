---
title: Proprietà DRM
description: Proprietà DRM
ms.assetid: 862fc8bc-6e40-4496-862a-c12c8a382116
keywords:
- Windows Media Format SDK, proprietà DRM
- Advanced Systems Format (ASF), proprietà DRM
- ASF (Advanced Systems Format), proprietà DRM
- digital rights management (DRM), proprietà
- DRM (digital rights management), proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d553d644a6f3ec7130262d0e8567a4aa6ceab53286b24248607b1928991f51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848267"
---
# <a name="drm-properties"></a>Proprietà DRM

Nella tabella seguente sono elencate le proprietà DRM che le applicazioni possono ottenere o impostare durante la scrittura o la lettura di file protetti. Queste proprietà non sono attributi di file. non vengono scritti nell'intestazione del file ASF.



| Proprietà DRM                                                                             | Identificatore globale                               | Tipo di dati             |
|------------------------------------------------------------------------------------------|-------------------------------------------------|-----------------------|
| [**Azione DRM \_ Consentita**](drm-actionallowed.md)                                          | g \_ wszWMDRM \_ ActionAllowed                      | **TIPO WMT \_ \_ BOOL**   |
| [**Azione DRM \_ Backup \_ consentito**](drm-actionallowed-backup.md)                           | g \_ wszWMDRM \_ ActionAllowed \_ Backup              | **TIPO WMT \_ \_ BOOL**   |
| [**Azione \_ DRMAllowed \_ CollaborativePlay**](drm-actionallowed-collaborativeplay.md)     | g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay   | **TIPO WMT \_ \_ BOOL**   |
| [**Azione DRM \_ Copia \_ consentita**](drm-actionallowed-copy.md)                               | g \_ wszWMDRM \_ ActionAllowed \_ Copy                | **TIPO WMT \_ \_ BOOL**   |
| [**Azione \_ DRMAllowed \_ CopyToCD**](drm-actionallowed-copytocd.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD            | **TIPO WMT \_ \_ BOOL**   |
| [**Azione \_ DRMAllowed \_ CopyToNonSDMIDevice**](drm-actionallowed-copytononsdmidevice.md) | g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice | **TIPO WMT \_ \_ BOOL**   |
| [**Azione \_ DRMAllowed \_ CopyToSDMIDevice**](drm-actionallowed-copytosdmidevice.md)       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice    | **TIPO WMT \_ \_ BOOL**   |
| [**Azione \_ DRMEseguata \_ consentita**](drm-actionallowed-playback.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ Playback            | **TIPO WMT \_ \_ BOOL**   |
| [**DRM \_ ActionAllowed Playlist (Azione DRM \_ Playlist consentita)**](drm-actionallowed-playlistburn.md)               | g \_ wszWMDRM \_ ActionAllowed \_ Playlist        | **TIPO WMT \_ \_ BOOL**   |
| [**DRM \_ BaseLicenseAcqURL**](drm-baselicenseacqurl.md)                                  | g \_ wszWMDRM \_ BaseLicenseAcqURL                  | **STRINGA DI TIPO WMT \_ \_** |
| [**Flag \_ DRM**](drm-flags.md)                                                          | g \_ wszWMDRM \_ Flags                              | **DWORD \_ DI TIPO \_ WMT**  |
| [**Intestazione \_ DRMSignPrivKey**](drm-headersignprivkey.md)                                  | g \_ wszWMDRM \_ HeaderSignPrivKey                  | **STRINGA DI TIPO WMT \_ \_** |
| [**DRM \_ IsDRM**](drm-isdrm.md)                                                          | g \_ wszIsDRM                                     | **TIPO WMT \_ \_ BOOL**   |
| [**DRM \_ IsDRMCached**](drm-isdrmcached.md)                                              | g \_ wszIsDRMCached                               | **TIPO WMT \_ \_ BOOL**   |
| [**DRM \_ KeySeed**](drm-keyseed.md)                                                      | g \_ wszWMDRM \_ KeySeed                            | **STRINGA DI TIPO WMT \_ \_** |
| [**Livello \_ DRM**](drm-level.md)                                                          | g \_ wszWMDRM \_ Level                              | **DWORD \_ DI TIPO \_ WMT**  |
| [**ID licenza \_ DRM**](drm-licenseid.md)                                                  | g \_ wszWMDRM \_ LicenseID                          | **STRINGA DI TIPO WMT \_ \_** |
| [**Stato licenza \_ DRM**](drm-licensestate.md)                                            | g \_ wszWMDRM \_ LicenseState                       | **DWORD \_ DI TIPO \_ WMT**  |
| [**DRM \_ LicenseState \_ CollaborativePlay**](drm-licensestate-collaborativeplay.md)       | g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | **FILE \_ BINARIO DI TIPO WMT \_** |
| [**Copia di \_ LicenseState \_ DRM**](drm-licensestate-copy.md)                                 | g \_ wszWMDRM \_ LicenseState \_ Copy                 | **FILE \_ BINARIO DI TIPO WMT \_** |
| [**DRM \_ LicenseState \_ CopyToCD**](drm-licensestate-copytocd.md)                         | g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | **FILE \_ BINARIO DI TIPO WMT \_** |
| [**DRM \_ LicenseState \_ CopyToSDMIDevice**](drm-licensestate-copytosdmidevice.md)         | g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | **FILE \_ BINARIO DI TIPO WMT \_** |
| [**DRM \_ LicenseState \_ CopyToNonSDMIDevice**](drm-licensestate-copytononsdmidevice.md)   | g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | **FILE \_ BINARIO DI TIPO WMT \_** |
| [**Riproduzione di \_ DRM \_ LicenseState**](drm-licensestate-playback.md)                         | g \_ wszWMDRM \_ LicenseState \_ Playback             | **FILE \_ BINARIO DI TIPO WMT \_** |
| [**Playlist \_ licenseState \_ DRMRescita**](drm-licensestate-playlistburn.md)                 | g \_ wszWMDRM \_ LicenseState \_ PlaylistCombotta         | **FILE \_ BINARIO DI TIPO WMT \_** |
| [**Diritti \_ DRM**](drm-rights.md)                                                        | g \_ wszWMDRM \_ Rights                             | **STRINGA DI TIPO WMT \_ \_** |
| [**DRM \_ SAPLEVEL**](drm-saplevel--deprecated.md)                                        | g \_ wszWMDRM \_ SAPLEVEL                           | **STRINGA DI TIPO WMT \_ \_** |
| [**Usare \_ \_ DRM avanzato**](use-advanced-drm.md)                                           | g \_ wszWMUse \_ Advanced \_ DRM                      | **TIPO WMT \_ \_ BOOL**   |
| [**Usare \_ DRM**](use-drm.md)                                                              | g \_ wszWMUse \_ DRM                                | **TIPO WMT \_ \_ BOOL**   |
| [**Revoca WMDRMNET \_**](wmdrmnet-revocation.md)                                      | g \_ wszWMDRMNET \_ Revocation                      | **STRINGA DI \_ TIPO \_ WMT** |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Elenco attributi DRM**](drm-attribute-list.md)
</dt> </dl>

 

 





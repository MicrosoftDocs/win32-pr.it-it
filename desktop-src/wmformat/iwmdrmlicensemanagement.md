---
title: Interfaccia IWMDRMLicenseManagement
description: L'interfaccia IWMDRMLicenseManagement fornisce metodi che eseguono operazioni generali correlate all'archivio licenze locale. Per ottenere un'istanza di questa interfaccia, chiamare IWMDRMProvider CreateObject. Passare IID \_ IWMDRMLicenseManagement come parametro riid.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- Formato Windows Media Interface IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14a7c555200e2eac99def75a1ad8c1d5dc1223fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333935"
---
# <a name="iwmdrmlicensemanagement-interface"></a>Interfaccia IWMDRMLicenseManagement

L'interfaccia **IWMDRMLicenseManagement** fornisce metodi che eseguono operazioni generali correlate all'archivio licenze locale.

Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Passare **IID \_ IWMDRMLicenseManagement** come parametro *riid* .

## <a name="members"></a>Membri

L'interfaccia **IWMDRMLicenseManagement** eredita da [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMLicenseManagement** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMDRMLicenseManagement** dispone di questi metodi.



| Metodo                                                                                               | Descrizione                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)                                     | Acquisisce in modo asincrono una licenza da un URL specificato.<br/>                                                      |
| [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md)                                     | Crea una copia di backup delle licenze nell'archivio licenze locale.<br/>                                                 |
| [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md)                               | Rimuove le licenze contrassegnate dall'archivio licenze e deframmenta l'archivio per migliorare le prestazioni.<br/>             |
| [**CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | Crea un oggetto enumeratore di licenze popolato con le informazioni sulla licenza basate sui valori dei parametri.<br/>            |
| [**CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | Genera una richiesta di revoca delle licenze.<br/>                                                                    |
| [**DeleteLicense**](iwmdrmlicensemanagement-deletelicense.md)                                       | Elimina una licenza dall'archivio licenze locale temporaneo.<br/>                                                    |
| [**MonitorLicenseAcquisition**](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | Avvia il monitoraggio per un processo di acquisizione delle licenze.<br/>                                                      |
| [**ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | Elimina una licenza importata per il contenuto originariamente protetto con un altro sistema di protezione del contenuto.<br/> |
| [**ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | Revoca le licenze dall'archivio licenze locale.<br/>                                                               |
| [**RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md)                                   | Ripristina le licenze di cui è stato eseguito il backup in precedenza.<br/>                                                                      |
| [**StoreLicense**](iwmdrmlicensemanagement-storelicense.md)                                         | Aggiunge una licenza all'archivio licenze locale.<br/>                                                                   |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 






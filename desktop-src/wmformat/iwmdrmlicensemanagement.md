---
title: Interfaccia IWMDRMLicenseManagement
description: L'interfaccia IWMDRMLicenseManagement fornisce metodi che eseguono operazioni generali correlate all'archivio licenze locale. Per ottenere un'istanza di questa interfaccia, chiamare IWMDRMProvider CreateObject. Passare \_ IWMDRMLicenseManagement IWMDRMLicenseManagement come parametro riid.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- IWMDRMLicenseManagement interfaccia Windows Media Format
- Interfaccia IWMDRMLicenseManagement windows Media Format , descritta
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63baeeb46baa877ccc294d1136351ec123d6c4661ee73d548b62d8cb4db05734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027549"
---
# <a name="iwmdrmlicensemanagement-interface"></a>Interfaccia IWMDRMLicenseManagement

**L'interfaccia IWMDRMLicenseManagement** fornisce metodi che eseguono operazioni generali correlate all'archivio licenze locale.

Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md). Passare **\_ IWMDRMLicenseManagement IWMDRMLicenseManagement** come *parametro riid.*

## <a name="members"></a>Membri

**L'interfaccia IWMDRMLicenseManagement** eredita da [**IWMDRMEventGenerator.**](iwmdrmeventgenerator.md) **IWMDRMLicenseManagement** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IWMDRMLicenseManagement.**



| Metodo                                                                                               | Descrizione                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)                                     | Acquisisce in modo asincrono una licenza da un URL specificato.<br/>                                                      |
| [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md)                                     | Crea un backup delle licenze nell'archivio licenze locale.<br/>                                                 |
| [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md)                               | Rimuove le licenze contrassegnate dall'archivio licenze e deframmenta l'archivio per migliorare le prestazioni.<br/>             |
| [**CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | Crea un oggetto enumeratore di licenza popolato con le informazioni sulla licenza in base ai valori dei parametri.<br/>            |
| [**CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | Genera una richiesta di revoca della licenza.<br/>                                                                    |
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

 

 






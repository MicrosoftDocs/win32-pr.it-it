---
title: Interfaccia ITsSbResourcePluginStoreEx
description: Espone metodi che consentono ai plug-in di risorse di archiviare oggetti quali sessioni e destinazioni.
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- Interfaccia ITsSbResourcePluginStoreEx Servizi Desktop remoto
- Interfaccia ITsSbResourcePluginStoreEx Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23c3ba6689f52d592d9c9799b6c7bec0acd58e1afcbc8e7a18e0cb9dbe6db98b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351292"
---
# <a name="itssbresourcepluginstoreex-interface"></a>Interfaccia ITsSbResourcePluginStoreEx

Espone metodi che consentono ai plug-in di risorse di archiviare oggetti quali sessioni e destinazioni. Questi metodi consentono di aggiungere, eliminare ed eseguire query su questi oggetti.

Questa interfaccia è disponibile solo in Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato. I [**metodi AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) [**e ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) dell'interfaccia [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) sono disponibili a partire da Windows Server 2016.

## <a name="members"></a>Membri

**L'interfaccia ITsSbResourcePluginStoreEx** eredita da [**ITsSbResourcePluginStore.**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) **ITsSbResourcePluginStoreEx** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITsSbResourcePluginStoreEx** include questi metodi.



| Metodo                                                                                                            | Descrizione                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**AcquireTargetLock**](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | Blocca una destinazione.<br/>                                                                                      |
| [**AddEnvironmentToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | Aggiunge un ambiente all'archivio plug-in delle risorse.<br/>                                                   |
| [**AddSessionToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | Aggiunge una nuova sessione all'archivio plug-in risorse.<br/>                                                    |
| [**AddTargetToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | Aggiunge una destinazione all'archivio plug-in delle risorse.<br/>                                                         |
| [**DeleteTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | Elimina una destinazione.<br/>                                                                                    |
| [**EnumerateEnvironments**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | Restituisce una matrice che contiene gli ambienti presenti nell'archivio plug-in delle risorse.<br/>               |
| [**EnumerateFarms**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | Enumera tutte le farm aggiunte all'archivio plug-in risorse.<br/>                         |
| [**EnumerateSessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | Enumera un set specificato di sessioni.<br/>                                                              |
| [**EnumerateTargets**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | Restituisce una matrice che contiene le destinazioni specificate presenti nell'archivio plug-in delle risorse.<br/> |
| [**GetFarmProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | Recupera una proprietà di una farm.<br/>                                                                      |
| [**QueryEnvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | Restituisce l'oggetto ambiente specificato.<br/>                                                            |
| [**QuerySessionBySessionId**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | Restituisce l'oggetto sessione con l'ID sessione specificato.<br/>                                        |
| [**Destinazione query**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | Restituisce la destinazione con il nome di destinazione e il nome della farm specificati.<br/>                                 |
| [**ReleaseTargetLock**](itssbresourcepluginstoreex-releasetargetlock.md)                                         | Rilascia un blocco su una destinazione.<br/>                                                                         |
| [**RemoveEnvironmentFromStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | Rimuove l'ambiente specificato dall'archivio plug-in risorse.<br/>                                   |
| [**SaveEnvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | Salva un ambiente.<br/>                                                                                |
| [**SaveSession**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | Salva una sessione.<br/>                                                                                     |
| [**Salva destinazione**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | Salva una destinazione.<br/>                                                                                      |
| [**SetEnvironmentProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | Imposta una proprietà in un ambiente.<br/>                                                                   |
| [**SetEnvironmentPropertyWithVersionCheck**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | Imposta una proprietà in un ambiente.<br/>                                                                   |
| [**SetSessionState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | Imposta lo stato di una sessione.<br/>                                                                         |
| [**SetTargetProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | Imposta una proprietà in una destinazione.<br/>                                                                         |
| [**SetTargetPropertyWithVersionCheck**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | Imposta una proprietà in una destinazione.<br/>                                                                         |
| [**SetTargetState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | Imposta lo stato di una destinazione.<br/>                                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                             |
| Fine del supporto server<br/>    | R2 per Windows Server 2012<br/>                                                             |
| IID<br/>                      | IID \_ ITsSbResourcePluginStoreEx è definito come 80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[Desktop remoto virtualization interface](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 






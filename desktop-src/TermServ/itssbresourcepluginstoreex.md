---
title: Interfaccia ITsSbResourcePluginStoreEx
description: Espone metodi che consentono ai plug-in di risorse di archiviare oggetti, ad esempio sessioni e destinazioni.
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- Interfaccia ITsSbResourcePluginStoreEx Servizi Desktop remoto
- Interfaccia ITsSbResourcePluginStoreEx Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a192b90f38d9b306c59f275d1fed3933d5cbd56a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120182"
---
# <a name="itssbresourcepluginstoreex-interface"></a>Interfaccia ITsSbResourcePluginStoreEx

Espone metodi che consentono ai plug-in di risorse di archiviare oggetti, ad esempio sessioni e destinazioni. Questi metodi aggiungono, eliminano ed eseguono query su questi oggetti.

Questa interfaccia è disponibile solo in Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato. I metodi [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) e [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) dell'interfaccia [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) sono disponibili a partire da Windows Server 2016.

## <a name="members"></a>Membri

L'interfaccia **ITsSbResourcePluginStoreEx** eredita da [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore). **ITsSbResourcePluginStoreEx** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITsSbResourcePluginStoreEx** dispone di questi metodi.



| Metodo                                                                                                            | Descrizione                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**AcquireTargetLock**](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | Blocca una destinazione.<br/>                                                                                      |
| [**AddEnvironmentToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | Aggiunge un ambiente all'archivio plug-in delle risorse.<br/>                                                   |
| [**AddSessionToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | Aggiunge una nuova sessione all'archivio plug-in della risorsa.<br/>                                                    |
| [**AddTargetToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | Aggiunge una destinazione all'archivio plug-in della risorsa.<br/>                                                         |
| [**DeleteTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | Elimina una destinazione.<br/>                                                                                    |
| [**EnumerateEnvironments**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | Restituisce una matrice che contiene gli ambienti presenti nell'archivio di plug-in di risorse.<br/>               |
| [**EnumerateFarms**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | Enumera tutte le farm che sono state aggiunte all'archivio plug-in di risorse.<br/>                         |
| [**EnumerateSessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | Enumera un set specificato di sessioni.<br/>                                                              |
| [**EnumerateTargets**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | Restituisce una matrice che contiene le destinazioni specificate presenti nell'archivio di plug-in di risorse.<br/> |
| [**GetFarmProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | Recupera una proprietà di una farm.<br/>                                                                      |
| [**QueryEnvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | Restituisce l'oggetto ambiente specificato.<br/>                                                            |
| [**QuerySessionBySessionId**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | Restituisce l'oggetto sessione con l'ID di sessione specificato.<br/>                                        |
| [**QueryTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | Restituisce la destinazione con il nome di destinazione e il nome della farm specificati.<br/>                                 |
| [**ReleaseTargetLock**](itssbresourcepluginstoreex-releasetargetlock.md)                                         | Rilascia un blocco su una destinazione.<br/>                                                                         |
| [**RemoveEnvironmentFromStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | Rimuove l'ambiente specificato dall'archivio di plug-in di risorse.<br/>                                   |
| [**SaveEnvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | Salva un ambiente.<br/>                                                                                |
| [**SaveSession**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | Salva una sessione.<br/>                                                                                     |
| [**SaveTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | Salva una destinazione.<br/>                                                                                      |
| [**SetEnvironmentProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | Imposta una proprietà in un ambiente.<br/>                                                                   |
| [**SetEnvironmentPropertyWithVersionCheck**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | Imposta una proprietà in un ambiente.<br/>                                                                   |
| [**SessionState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | Imposta lo stato di una sessione.<br/>                                                                         |
| [**SetTargetProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | Imposta una proprietà in una destinazione.<br/>                                                                         |
| [**SetTargetPropertyWithVersionCheck**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | Imposta una proprietà in una destinazione.<br/>                                                                         |
| [**SetTargetState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | Imposta lo stato di una destinazione.<br/>                                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                             |
| Fine del supporto server<br/>    | Windows Server 2012 R2<br/>                                                             |
| IID<br/>                      | IID \_ ITsSbResourcePluginStoreEx è definito come 80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[Interfacce di virtualizzazione Desktop remoto](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 






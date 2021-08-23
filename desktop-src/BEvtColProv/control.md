---
description: Controllo dell'istanza dell'agente di raccolta. Richiede i privilegi di amministratore (BA).
ms.assetid: 83b485b2-b03b-4882-a3ff-187eac299755
ms.tgt_platform: multiple
title: Control (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5eeccd31f3d9ab1f0b0ec05ebf80ea9f880a73fed21b21fe67fe63257af28871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589021"
---
# <a name="control-class"></a>Control (classe)

Controllo dell'istanza dell'agente di raccolta. Richiede i privilegi di amministratore (BA).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Provider("BootEventCollectorWmiProvider"), AMENDMENT]
class Control
{
};
```

## <a name="members"></a>Members

La **classe Control** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe Control** dispone di questi metodi.



| Metodo                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Checkpoint**](control-checkpoint.md)                       | Se la configurazione corrente è il risultato di Undo/Redo/Restore, la contrassegna come se fosse stata impostata in modo esplicito, in modo che la cronologia conservi l'ora in cui è stata impostata e verrà creato un file di backup alla successiva modifica della configurazione. Se la configurazione corrente è già stata impostata in modo esplicito, non ha alcun effetto. Restituisce 1 in caso di esito positivo, 0 in caso di errore.<br/> |
| [**DumpDiagnostics**](control-dumpdiagnostics.md)             | Eseguire il dump delle informazioni di diagnostica nel log.<br/>                                                                                                                                                                                                                                                                                                                  |
| [**FastShutdown**](control-fastshutdown.md)                   | Arrestare rapidamente l'agente di raccolta, rimuovendo tutti i dati in coda.<br/>                                                                                                                                                                                                                                                                                                    |
| [**Svuotamento**](control-flush.md)                                 | Scaricare i buffer del server d'inoltro.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**GetConfiguration**](control-getconfiguration.md)           | Leggere la configurazione attiva dell'agente di raccolta.<br/>                                                                                                                                                                                                                                                                                                                |
| [**IsConfigurationEqual**](control-isconfigurationequal.md)   | Confrontare l'argomento con la configurazione attiva dell'agente di raccolta. Restituisce 1 se corrispondono, 0 in caso contrario.<br/>                                                                                                                                                                                                                                                 |
| [**ListBackups**](control-listbackups.md)                     | Restituisce l'elenco dei file di configurazione di backup salvati che possono essere ripristinati.<br/>                                                                                                                                                                                                                                                                                  |
| [**Ripeti**](control-redo.md)                                   | Reimpostare la configurazione attiva dell'agente di raccolta dal file di backup successivo (determinato dal timestamp originale corrente). Se la configurazione è stata annullata, significa ripetere la modifica annullata. Restituisce 1 in caso di esito positivo, 0 in caso di errore.<br/>                                                                                                    |
| [**RestoreFile**](control-restorefile.md)                     | Ripristinare la configurazione attiva dell'agente di raccolta da un file di backup. Restituisce 1 in caso di esito positivo, 0 in caso di errore.<br/>                                                                                                                                                                                                                                                        |
| [**RestoreFromTime**](control-restorefromtime.md)             | Ripristinare la configurazione attiva dell'agente di raccolta da un file di backup, selezionato da un timestamp. Restituisce 1 in caso di esito positivo, 0 in caso di errore.<br/>                                                                                                                                                                                                                               |
| [**SetConfiguration**](control-setconfiguration.md)           | Impostare la nuova configurazione attiva dell'agente di raccolta. Restituisce 1 in caso di esito positivo, 0 in caso di errore.<br/>                                                                                                                                                                                                                                                                           |
| [**Arresto**](control-shutdown.md)                           | Arrestare l'agente di raccolta. Se l'agente di raccolta viene eseguito come servizio, l'arresto del servizio è l'approccio migliore.<br/>                                                                                                                                                                                                                                                     |
| [**Annulla**](control-undo.md)                                   | Ripristinare la configurazione attiva dell'agente di raccolta dal file di backup precedente (determinato dal timestamp originale corrente). Se la configurazione è stata appena impostata, significa annullare la modifica. Le chiamate consecutive verranno annullate nelle configurazioni precedenti e precedenti. Restituisce 1 in caso di esito positivo, 0 in caso di errore.<br/>                           |
| [**ValidateConfiguration**](control-validateconfiguration.md) | Convalidare la correttezza di un testo di configurazione senza impostarlo come attivo. Restituisce 1 in caso di esito positivo, 0 in caso di errore.<br/>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                       |
| Spazio dei nomi<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



 

 





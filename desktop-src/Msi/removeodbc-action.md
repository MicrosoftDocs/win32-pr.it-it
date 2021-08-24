---
description: L'azione RemoveODBC rimuove le origini dati, i convertitori e i driver elencati per la rimozione durante l'installazione.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Azione RemoveODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6619bc5b8a18cff2ee33dbe45261764c682953bad75a17cb9d6e93cbe487147b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580431"
---
# <a name="removeodbc-action"></a>Azione RemoveODBC

L'azione RemoveODBC rimuove le origini dati, i convertitori e i driver elencati per la rimozione durante l'installazione. Questa azione esegue una query sulla tabella [ODBCDataSource,](odbcdatasource-table.md)sulla tabella [ODBCTranslator](odbctranslator-table.md)e sulla tabella [ODBCDriver](odbcdriver-table.md) per ogni origine dati, convertitore o driver pianificata per la rimozione.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

Non sono presenti restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData

Per ogni driver installato.



| Campo | Descrizione dei dati dell'azione               |
|-------|------------------------------------------|
| \[1\] | Descrizione del driver. Chiave del driver ODBC. |
| \[2\] | Componentid                              |



 

Per ogni convertitore installato.



| Campo | Descrizione dei dati dell'azione               |
|-------|------------------------------------------|
| \[1\] | Descrizione del driver. Chiave del driver ODBC. |
| \[2\] | Componentid                              |



 

Per ogni origine dati installata.



| Campo | Descrizione dei dati dell'azione                              |
|-------|---------------------------------------------------------|
| \[1\] | Descrizione del driver. Chiave del driver ODBC.                |
| \[2\] | Componentid                                             |
| \[3\] | Registrazione: SQL \_ REMOVE \_ DSN o SQL \_ REMOVE SYS \_ \_ DSN |



 

## <a name="remarks"></a>Commenti

Se il numero di utilizzo di ODBC e il numero di utilizzo del file diventano zero, il file viene rimosso. La registrazione dipende dai conteggi di utilizzo di ODBC e la rimozione dei file si basa sui conteggi dei riferimenti alle chiavi delle DLL condivise.

 

 




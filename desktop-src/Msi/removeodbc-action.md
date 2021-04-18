---
description: L'azione RemoveODBC rimuove le origini dati, i traduttori e i driver elencati per la rimozione durante l'installazione.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Azione RemoveODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1234ed736a8cb8258bccf3085de92bfb1b324cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312319"
---
# <a name="removeodbc-action"></a>Azione RemoveODBC

L'azione RemoveODBC rimuove le origini dati, i traduttori e i driver elencati per la rimozione durante l'installazione. Questa azione esegue una query sulla tabella [ODBCDataSource](odbcdatasource-table.md), sulla [tabella ODBCTranslator](odbctranslator-table.md)e sulla [tabella ODBCDriver](odbcdriver-table.md) per ogni origine dati, convertitore o driver pianificato per la rimozione.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Non esistono restrizioni di sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData

Per ogni driver installato.



| Campo | Descrizione dei dati dell'azione               |
|-------|------------------------------------------|
| \[1\] | Descrizione del driver. Chiave del driver ODBC. |
| \[2\] | ComponentId                              |



 

Per ogni traduttore installato.



| Campo | Descrizione dei dati dell'azione               |
|-------|------------------------------------------|
| \[1\] | Descrizione del driver. Chiave del driver ODBC. |
| \[2\] | ComponentId                              |



 

Per ogni origine dati installata.



| Campo | Descrizione dei dati dell'azione                              |
|-------|---------------------------------------------------------|
| \[1\] | Descrizione del driver. Chiave del driver ODBC.                |
| \[2\] | ComponentId                                             |
| \[3\] | Registrazione: SQL \_ Remove \_ DSN o SQL \_ Remove \_ sys \_ DSN |



 

## <a name="remarks"></a>Commenti

Se il conteggio di utilizzo di ODBC e il conteggio di utilizzo file diventano zero, il file verrà rimosso. La registrazione dipende dai conteggi di utilizzo di ODBC e la rimozione dei file è basata sui conteggi dei riferimenti chiave delle DLL condivise.

 

 




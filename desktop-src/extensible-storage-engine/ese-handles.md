---
description: 'Altre informazioni su: Handle ESE'
title: Handle ESE
TOCTitle: ESE Handles
ms:assetid: 969ae14f-3548-431d-a19d-5df92891441d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269349(v=EXCHG.10)
ms:contentKeyID: 32765636
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5177de8b7fbc07d592bb599941a1fd02810bbbf81e16b65cd15c6ebdfd75d3d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786297"
---
# <a name="ese-handles"></a>Handle ESE


_**Si applica a:** Windows | Windows Server_

## <a name="ese-handles"></a>Handle ESE

Gli handle ESE vengono usati per creare sessioni e accedere ai database. Vengono mantenuti in una gerarchia, il che significa che l'output di un livello viene usato per accedere alle risorse al livello successivo.

Il diagramma mostra la gerarchia degli handle e le funzioni corrispondenti che creano gli handle. Oltre alle funzioni sono indicati anche gli handle usati nella chiamata per creare il nuovo handle.

![ESE_Documentation_handles2](images/Gg269349.ESE_Documentation_handles2(EXCHG.10).gif "ESE_Documentation_handles2")

Come illustrato nel diagramma, l'istanza è l'handle radice e il livello di recupero del database in caso di arresto imprevisto del processo o del sistema. L'handle dell'JET_INSTANCE viene creato da [JetCreateInstance](./jetcreateinstance-function.md) e [JetCreateInstance2.](./jetcreateinstance2-function.md) Il livello successivo, ovvero il livello di sessione, è il contesto della transazione del motore di database e il livello in cui vengono eseguite tutte le operazioni di database. L'handle di sessione, JET_SESID, viene creato nel contesto dell'istanza nella chiamata a [JetBeginSession](./jetbeginsession-function.md). L'ID sessione viene usato in tutte le chiamate successive per accedere a tabelle e database. Se l'istanza viene usata da più thread alla volta, ogni thread deve usare il proprio handle di sessione. L'handle di database viene creato usando l'handle di sessione e usato principalmente per gestire lo schema del database, ma può anche essere usato per gestire le tabelle all'interno del database. Gli handle di database possono essere usati solo nella sessione in cui vengono creati. L'handle per il database viene creato nella chiamata a [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetOpenDatabase](./jetopendatabase-function.md). Le tabelle sono associate all'ID del database in cui vengono create.

Il JET_TABLEID di dati contiene un handle per un cursore di database. Viene usato per analizzare record, cercare record o creare record di aggiornamento ed eliminazione. L'handle di tabella viene creato nella chiamata a [JetOpenTable](./jetopentable-function.md)o [JetCreateTable](./jetcreatetable-function.md). [JetOpenTempTable,](./jetopentemptable-function.md) [JetOpenTempTable2](./jetopentemptable2-function.md)e [JetOpenTempTable3](./jetopentemptable3-function.md) creano anche ID tabella per le tabelle temporanee e [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) e [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) restituiscono gli ID tabella nella struttura out. Le colonne create all'interno della tabella hanno ognuna un identificatore di colonna univoco o COLUMN_ID. Gli ID delle colonne vengono creati nelle chiamate a [JetAddColumn](./jetaddcolumn-function.md)o nelle chiamate a [JetOpenTempTable,](./jetopentemptable-function.md) [JetOpenTempTable2](./jetopentemptable2-function.md)o [JetOpenTempTable3](./jetopentemptable3-function.md) per le tabelle temporanee. Gli ID colonna possono essere recuperati anche per una determinata colonna in base al nome con API come [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).

---
description: 'Altre informazioni su: handle ESE'
title: Handle ESE
TOCTitle: ESE Handles
ms:assetid: 969ae14f-3548-431d-a19d-5df92891441d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269349(v=EXCHG.10)
ms:contentKeyID: 32765636
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: cc91a4586fc1619c55b5f45afbca39ce04c0c6cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233236"
---
# <a name="ese-handles"></a>Handle ESE


_**Si applica a:** Windows | Windows Server_

## <a name="ese-handles"></a>Handle ESE

Gli handle ESE vengono utilizzati per creare sessioni e database di Access. Vengono mantenute in una gerarchia, il che significa che l'output di un livello viene usato per accedere alle risorse al livello successivo.

Il diagramma mostra la gerarchia di handle e le funzioni corrispondenti che creano gli handle. Inoltre, con le funzioni sono inclusi gli handle utilizzati nella chiamata per creare il nuovo handle.

![ESE_Documentation_handles2](images/Gg269349.ESE_Documentation_handles2(EXCHG.10).gif "ESE_Documentation_handles2")

Come illustrato nel diagramma, l'istanza è l'handle radice e il livello in cui viene recuperato il database in caso di interruzione imprevista del processo o di arresto del sistema. L'handle dell'istanza, JET_INSTANCE, viene creato da [JetCreateInstance](./jetcreateinstance-function.md) e [JetCreateInstance2](./jetcreateinstance2-function.md). Il livello successivo, ovvero il livello di sessione, è il contesto di transazione del motore di database e il livello in base al quale vengono eseguite tutte le operazioni di database. L'handle di sessione, JET_SESID, viene creato nel contesto dell'istanza nella chiamata a [JetBeginSession](./jetbeginsession-function.md). L'ID sessione viene usato in tutte le chiamate successive per accedere a tabelle e database. Se l'istanza viene utilizzata da più di un thread alla volta, ogni thread deve utilizzare il proprio handle di sessione. L'handle di database viene creato utilizzando l'handle di sessione e utilizzato principalmente per gestire lo schema del database, ma può essere utilizzato anche per gestire le tabelle all'interno del database. Gli handle di database possono essere utilizzati solo nella sessione in cui sono stati creati. L'handle per il database viene creato nella chiamata a [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetOpenDatabase](./jetopendatabase-function.md). Le tabelle sono associate all'ID del database in cui vengono create.

Il tipo di dati JET_TABLEID contiene un handle per un cursore del database. Viene usato per analizzare i record, cercare i record o creare i record di aggiornamento ed eliminazione. L'handle di tabella viene creato nella chiamata a [JetOpenTable](./jetopentable-function.md)o [JetCreateTable](./jetcreatetable-function.md). [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md)e [JetOpenTempTable3](./jetopentemptable3-function.md) creano anche gli ID tabella per le tabelle temporanee e [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) e [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) restituiscono gli ID tabella nella struttura out. Ogni colonna creata all'interno della tabella contiene un identificatore di colonna o un COLUMN_ID univoco. Gli ID delle colonne vengono creati nelle chiamate a [JetAddColumn](./jetaddcolumn-function.md)o nelle chiamate a [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md)o [JetOpenTempTable3](./jetopentemptable3-function.md) per le tabelle temporanee. Gli ID di colonna possono anche essere recuperati per una determinata colonna per nome con API, ad esempio [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).

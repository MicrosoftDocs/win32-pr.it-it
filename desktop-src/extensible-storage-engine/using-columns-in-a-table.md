---
description: Altre informazioni sull'uso delle colonne in una tabella
title: Utilizzo di colonne in una tabella
TOCTitle: Using Columns in a Table
ms:assetid: 064ac59e-d306-4335-a623-754a003f5ebc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269178(v=EXCHG.10)
ms:contentKeyID: 32765481
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 332cca1c64c851ded44951fc9bb7f68ebd9f6818030cefeb8406f965a1bd5d6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471301"
---
# <a name="using-columns-in-a-table"></a>Utilizzo di colonne in una tabella


_**Si applica a:** Windows | Windows Server_

## <a name="using-columns-in-a-table"></a>Utilizzo di colonne in una tabella

È possibile creare una tabella con un set iniziale di colonne chiamando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o senza colonne chiamando [JetCreateTable](./jetcreatetable-function.md). Quando la tabella viene creata con un set iniziale di colonne nella chiamata a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o [JetCreateTableColumnIndex2,](./jetcreatetablecolumnindex2-function.md)contiene una struttura [JET_TABLECREATE](./jet-tablecreate-structure.md) [(o JET_TABLECREATE2](./jet-tablecreate2-structure.md)). Queste strutture contengono una matrice [di JET_COLUMNCREATE](./jet-columncreate-structure.md) che definiscono il set di colonne nella tabella. Il **membro grbit** imposta le opzioni per la colonna e il membro **coltyp** imposta il tipo di dati che è possibile impostare nella colonna.

Quando la tabella viene creata senza colonne, devono essere aggiunte chiamando [JetAddColumn](./jetaddcolumn-function.md) con la [JET_COLUMNDEF](./jet-columndef-structure.md) struttura . Il **membro grbit** della [struttura JET_COLUMNDEF](./jet-columndef-structure.md) imposta le opzioni nella colonna e il membro **coltyp** imposta il tipo di dati che è possibile impostare nella colonna. I valori predefiniti della colonna vengono impostati nella chiamata a [JetAddColumn](./jetaddcolumn-function.md) specificando un valore nel parametro *pvDefault* e le dimensioni nel *parametro cbDefault.* Una colonna senza un valore predefinito ha effettivamente un valore predefinito NULL.

I valori nella tabella possono essere impostati solo all'interno del contesto di una transazione. La transazione inizia nella chiamata [a JetBeginTransaction](./jetbegintransaction-function.md) e termina con la chiamata a [JetCommitTransaction.](./jetcommittransaction-function.md) All'interno della transazione è possibile impostare un singolo valore di colonna chiamando [JetSetColumn](./jetsetcolumn-function.md)oppure impostare più valori di colonne chiamando [JetSetColumns.](./jetsetcolumns-function.md) [JetSetColumns](./jetsetcolumns-function.md) usa una matrice [di JET_SETCOLUMN](./jet-setcolumn-structure.md) per impostare più colonne nella tabella. I dati sono contenuti nel *parametro pvData* di [JetSetColumn](./jetsetcolumn-function.md)o nel membro **pvData** nella [JET_SETCOLUMN](./jet-setcolumn-structure.md) struttura.

Le [strutture JET_COLUMNBASE](./jet-columnbase-structure.md), [JET_COLUMNLIST](./jet-columnlist-structure.md)e [JET_COLUMNDEF](./jet-columndef-structure.md) vengono restituite nelle chiamate a [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)e [JetGetColumnInfo](./jetgetcolumninfo-function.md) a seconda del tipo di colonna recuperato. La [JET_COLUMNBASE](./jet-columnbase-structure.md) descrive i parametri della colonna di base e [il JET_COLUMNLIST](./jet-columnlist-structure.md) contiene le informazioni necessarie per attraversare la tabella temporanea creata dalle funzioni [JetGetColumnInfo](./jetgetcolumninfo-function.md) e [JetGetTableColumnInfo.](./jetgettablecolumninfo-function.md)

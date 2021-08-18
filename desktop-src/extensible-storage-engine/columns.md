---
description: 'Altre informazioni su: Colonne'
title: Colonne
TOCTitle: Columns
ms:assetid: bc16ca4c-e3c9-43db-ac16-284d7cc0926d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294073(v=EXCHG.10)
ms:contentKeyID: 32765688
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 8cc7e3921c1904cdae3a09432d6a17eae3953251d3bd39c288cb6d6ffe184ffc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982701"
---
# <a name="columns"></a>Colonne


_**Si applica a:** Windows | Windows Server_

## <a name="columns"></a>Colonne

È possibile creare una tabella con un set iniziale di colonne chiamando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o senza un set iniziale di colonne chiamando [JetCreateTable](./jetcreatetable-function.md). Le tabelle in ESE possono contenere fino a 127 colonne a lunghezza fissa, 128 colonne a lunghezza variabile e 64.993 colonne con tag. Le colonne vengono identificate in base al nome e all'ID e possono essere aggiunte dinamicamente alla tabella [con JetAddColumn.](./jetaddcolumn-function.md) Le colonne vengono create con un tipo di dati specifico e un set facoltativo di attributi, ad esempio se la colonna è a lunghezza fissa o se può essere NULL o meno.

Il tipo di una colonna determina i dati che possono essere archiviati nella colonna e molte delle proprietà della colonna, incluso l'ordine di indicizzazione. ESE supporta un'ampia gamma di tipi di colonna, con dimensioni comprese tra 1 bit e 2 GB (2146483647 caratteri ASCII o 1073741823 Unicode). Per un elenco completo dei tipi di dati di colonna supportati da ESE, vedere l'argomento [JET_COLTYP.](./jet-coltyp.md) Negli argomenti seguenti vengono illustrati alcuni dei tipi di colonne supportati da ESE:

  - [Colonne con tag, fisse e variabili](./tagged-fixed-and-variable-columns.md)

  - [Colonne Version, Auto-Increment e Escrow](./version-auto-increment-and-escrow-columns.md)

  - [Colonne con valori lunghi](./long-value-columns.md)

  - [Colonne di tipo sparse multivalore](./multi-valued-sparse-columns.md)

  - [Colonne definite dall'utente](./user-defined-columns.md)

  - [Uso di colonne in una tabella](./using-columns-in-a-table.md)

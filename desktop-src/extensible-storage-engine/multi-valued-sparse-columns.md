---
description: 'Altre informazioni su: colonne di tipo sparse multivalore'
title: Colonne di tipo sparse multivalore
TOCTitle: Multi-Valued Sparse Columns
ms:assetid: 36e82a73-aad4-4e0d-a743-a2182c41fe9c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269225(v=EXCHG.10)
ms:contentKeyID: 32765527
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 21448d50e17881517086c1b258dcce02e84286a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313091"
---
# <a name="multi-valued-sparse-columns"></a>Colonne di tipo sparse multivalore


_**Si applica a:** Windows | Windows Server_

## <a name="multi-valued-sparse-columns"></a>Colonne di tipo sparse multivalore

Le colonne di tipo sparse possono essere a lunghezza fissa o variabile e sono univoche perché non prendono spazio in un record se sono NULL o rimangono al valore predefinito. Le colonne di tipo sparse, definite anche colonne con tag, possono contenere più di un valore in un singolo record. Le colonne con tag possono essere qualsiasi tipo di colonna descritto nelle costanti [JET_coltyp](./jet-coltyp.md) . Vengono creati quando la colonna viene aggiunta alla tabella impostando il flag JET_bitColumnTagged nella struttura [JET_COLUMNDEF](./jet-columndef-structure.md) nella chiamata a [JetAddColumn](./jetaddcolumn-function.md)o nella struttura [JET_COLUMNCREATE](./jet-columncreate-structure.md) utilizzata nella chiamata a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md). Le colonne di tipo JET_coltypLongText e JET_coltypLongBinary vengono create automaticamente come colonne con tag.

Solo le colonne con tag possono contenere più valori in un record, le colonne a lunghezza fissa o variabile non possono contenere più valori. Esistono due tipi di colonne multivalore:

  - Per impostazione predefinita, le colonne con tag sono multivalore. Quando un secondo valore viene aggiunto alla colonna, diventa automaticamente multivalore.

  - Colonne con tag creati con l'opzione JET_bitColumnMultiValued nella struttura [JET_COLUMNDEF](./jet-columndef-structure.md) nella chiamata a [JetAddColumn](./jetaddcolumn-function.md).

L'opzione JET_bitColumnMultiValued modifica la modalità di indicizzazione della colonna. Le colonne multivalore con l'opzione JET_bitColumnMultiValued sono indicizzate in maniera più approfondita rispetto a quelle con tag multivalore. Queste colonne vengono indicizzate su tutti i valori nella colonna multivalore, mentre le colonne con valori con tag vengono indicizzate solo sul primo valore della colonna multivalore. Si consideri, ad esempio, una colonna multivalore in cui è impostata l'opzione JET_bitColumnMultiValued ed è la prima colonna multivalore in un indice. Questa colonna contiene tre valori: A, B e C. Un indice in questa colonna contiene le voci per tutti e tre i valori, A, B e C. Se l'opzione JET_bitColumnMultiValued non è stata impostata, l'indice su questa colonna contiene solo il primo valore, a, nell'indice.

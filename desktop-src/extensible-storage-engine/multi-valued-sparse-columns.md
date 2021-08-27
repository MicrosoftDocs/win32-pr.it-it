---
description: 'Altre informazioni su: Colonne di tipo sparse multivalore'
title: Colonne di tipo sparse multivalore
TOCTitle: Multi-Valued Sparse Columns
ms:assetid: 36e82a73-aad4-4e0d-a743-a2182c41fe9c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269225(v=EXCHG.10)
ms:contentKeyID: 32765527
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 21dbe18be8be26af9fe32d9b80cbd5744c172793e27701d46438df4d63dcf395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115581"
---
# <a name="multi-valued-sparse-columns"></a>Colonne di tipo sparse multivalore


_**Si applica a:** Windows | Windows Server_

## <a name="multi-valued-sparse-columns"></a>Colonne di tipo sparse multivalore

Le colonne di tipo sparse possono essere a lunghezza fissa o variabile e sono univoche in quanto non accettano spazio in un record se sono NULL o vengono lasciato al valore predefinito. Le colonne di tipo sparse, note anche come colonne con tag, possono contenere più di un valore in un singolo record. Le colonne con tag possono essere qualsiasi tipo di colonna descritto nelle [costanti JET_coltyp.](./jet-coltyp.md) Vengono creati quando la colonna viene aggiunta alla tabella impostando il flag [JET_bitColumnTagged](./jet-columndef-structure.md) nella struttura JET_COLUMNDEF nella chiamata a [JetAddColumn](./jetaddcolumn-function.md)o nella struttura [JET_COLUMNCREATE](./jet-columncreate-structure.md) usata nella chiamata a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o [JetCreateTableColumnIndex2.](./jetcreatetablecolumnindex2-function.md) Le colonne di JET_coltypLongText e JET_coltypLongBinary vengono create automaticamente come colonne con tag.

Solo le colonne con tag possono contenere più valori in un record, le colonne a lunghezza fissa o variabile non possono contenere più valori. Esistono due tipi di colonne multivalore:

  - Le colonne contrassegnate sono multivalore per impostazione predefinita. Quando un secondo valore viene aggiunto alla colonna, diventa automaticamente multivalore.

  - Colonne contrassegnate create con l'opzione JET_bitColumnMultiValued nella struttura JET_COLUMNDEF [nella](./jet-columndef-structure.md) chiamata a [JetAddColumn](./jetaddcolumn-function.md).

L JET_bitColumnMultiValued'opzione cambia il modo in cui la colonna viene indicizzata. Le colonne multivalore con JET_bitColumnMultiValued sono indicizzate in modo più esteso rispetto alle colonne con più valori con tag. Queste colonne vengono indicizzate su tutti i valori nella colonna multivalore, mentre le colonne multivalore con tag vengono indicizzate solo sul primo valore della colonna multivalore. Si consideri ad esempio una colonna multivalore in cui è impostata l'opzione JET_bitColumnMultiValued ed è la prima colonna multivalore in un indice. Questa colonna contiene tre valori: A, B e C. Un indice su questa colonna contiene voci per tutti e tre i valori, A, B e C. Se l'JET_bitColumnMultiValued non è stata impostata, l'indice su questa colonna contiene solo il primo valore, A, nell'indice.

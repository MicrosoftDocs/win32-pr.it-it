---
description: 'Altre informazioni: colonne con tag, fisse e variabili'
title: Colonne con tag, fisse e variabili
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 3f27237c5f75874f7320f675affe20f3833084b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484869"
---
# <a name="tagged-fixed-and-variable-columns"></a>Colonne con tag, fisse e variabili


_**Si applica a:** Windows | Windows Server_

## <a name="tagged-fixed-and-variable-columns"></a>Colonne con tag, fisse e variabili

Le colonne con tag, a lunghezza fissa e a lunghezza variabile sono i tipi di colonna primari supportati da ESE. Le colonne con tag non sono presenti in un record a meno che i dati non vengano archiviati nella colonna e possano essere a lunghezza fissa o variabile. Le colonne con tag possono anche contenere più di un valore in un singolo record. Le colonne fisse accettano la stessa quantità di spazio in ogni riga e richiedono 1 bit per rappresentare il valore NULL. Le colonne a lunghezza variabile richiedono 2 byte per rappresentare le dimensioni e il valore NULL e occupano una quantità variabile di spazio in ogni record. Per ulteriori informazioni sulle colonne contrassegnate e fisse, vedere il Jet_bitColumnTagged e Jet_bitColumnFixed opzione nel membro **grbit** della struttura [JET_COLUMNDEF](./jet-columndef-structure.md) utilizzata nella chiamata a [JetAddColumn](./jetaddcolumn-function.md).

Le colonne a lunghezza variabile sono determinate dal tipo di colonna impostato nel parametro *coltyp* nella chiamata a [JetAddColumn](./jetaddcolumn-function.md). I tipi di colonna seguenti possono essere a lunghezza fissa o variabile a seconda che sia impostata l'opzione Jet_bitColumnFixed:

  - JET_coltypBinary

  - JET_coltypText

  - JET_coltypLongBinary

  - JET_coltypLongText

In generale, i dati nel record vengono archiviati con l'intervallo fisso per primo, l'intervallo di variabili successivo e l'intervallo con tag archiviato per ultimo. Nel diagramma seguente viene illustrato il modo in cui i record vengono archiviati nella tabella. Come illustrato nel diagramma, l'intervallo con tag può contenere colonne con più valori.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")

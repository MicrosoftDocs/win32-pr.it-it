---
description: 'Altre informazioni su: Colonne con tag, fisse e variabili'
title: Colonne con tag, fisse e variabili
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: af2ab8ece57342f211b0dd4488b6feb25b191c1977ae39038fb61ea56f20d543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484743"
---
# <a name="tagged-fixed-and-variable-columns"></a>Colonne con tag, fisse e variabili


_**Si applica a:** Windows | Windows Server_

## <a name="tagged-fixed-and-variable-columns"></a>Colonne con tag, fisse e variabili

Le colonne con tag, fisse e a lunghezza variabile sono i tipi di colonna primari supportati da ESE. Le colonne contrassegnate non sono presenti in un record, a meno che i dati non siano archiviati nella colonna e possano essere di lunghezza fissa o variabile. Le colonne contrassegnate possono contenere anche più valori in un singolo record. Le colonne fisse richiedono la stessa quantità di spazio in ogni riga e richiedono 1 bit per rappresentare il valore NULL. Le colonne a lunghezza variabile richiedono 2 byte per rappresentare le dimensioni e il valore NULL e occupano una quantità variabile di spazio in ogni record. Per altre informazioni sulle colonne con tag e fisse, vedere l'opzione Jet_bitColumnTagged e Jet_bitColumnFixed nel membro **grbit** della struttura JET_COLUMNDEF usata nella chiamata [a](./jet-columndef-structure.md) [JetAddColumn](./jetaddcolumn-function.md).

Le colonne a lunghezza variabile sono determinate dal tipo di colonna impostato nel *parametro coltyp* nella chiamata a [JetAddColumn](./jetaddcolumn-function.md). I tipi di colonna seguenti possono essere a lunghezza fissa o variabile a seconda che l'opzione Jet_bitColumnFixed sia impostata:

  - JET_coltypBinary

  - JET_coltypText

  - JET_coltypLongBinary

  - JET_coltypLongText

In generale, i dati nel record vengono archiviati con prima l'intervallo fisso, l'intervallo di variabili successivo e l'intervallo con tag archiviato per ultimo. Il diagramma seguente illustra come vengono archiviati i record nella tabella . Come illustrato nel diagramma, l'intervallo con tag può contenere colonne con più valori.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")

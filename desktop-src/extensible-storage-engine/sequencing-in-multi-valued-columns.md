---
description: 'Altre informazioni su: sequenziazione in colonne multivalore'
title: Sequenziazione in colonne multivalore
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 54f4bd7734cb8c1bf5a87eb444c3205d89f4a6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555725"
---
# <a name="sequencing-in-multi-valued-columns"></a>Sequenziazione in colonne multivalore


_**Si applica a:** Windows | Windows Server_

## <a name="sequencing-in-multi-valued-columns"></a>Sequenziazione in colonne multivalore

I valori in una colonna multivalore sono identificati da un numero di indice denominato *itagSequence*. Questo numero è un riferimento a un singolo valore della colonna. Questo numero viene utilizzato quando i nuovi valori vengono impostati, recuperati o enumerati nella colonna. *ItagSequence* viene utilizzato in varie strutture, tra cui:

  - [JET_RETINFO](./jet-retinfo-structure.md)

  - [JET_SETINFO](./jet-setinfo-structure.md)

  - [JET_SETCOLUMN](./jet-setcolumn-structure.md)

  - [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)

  - [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)

Questo *itagSequence* inizia da 1 per ogni valore nella colonna multivalore. Il numero di sequenza viene aumentato quando vengono aggiunti nuovi valori alla colonna. L'impostazione di un valore in una colonna con un valore di *itagSequence* pari a 0 indica che il valore deve essere aggiunto al set di valori già presenti in tale colonna. L'utilizzo di un *itagSequence* maggiore del numero di valori attualmente impostati per una colonna avrà lo stesso effetto. Se si specifica il valore di *itagSequence* di un valore esistente, questo valore non viene inserito. Se si imposta un valore esistente su NULL, il valore viene rimosso dal set di valori già presenti in tale colonna. In questo modo, tutti i valori successivi nella colonna verranno spostati di uno slot, in modo che il successivo accesso a tali valori da parte di *itagSequence* sarà di un numero uno inferiore rispetto a quello usato in precedenza.

Nel diagramma seguente viene illustrato un *itagSequence* in una colonna multivalore. La colonna denominata ColA include tre voci: val1, val2 e Val3 con *itagSequence* rispettivamente 1, 2 e 3.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")

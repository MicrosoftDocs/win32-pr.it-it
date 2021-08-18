---
description: 'Altre informazioni: Sequenziazione in colonne multivalore'
title: Sequenziazione in colonne multivalore
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 45c8c192becdb616b94360b491bd66f9e6fa492542da320a5536527c2bd45605
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016021"
---
# <a name="sequencing-in-multi-valued-columns"></a>Sequenziazione in colonne multivalore


_**Si applica a:** Windows | Windows Server_

## <a name="sequencing-in-multi-valued-columns"></a>Sequenziazione in colonne multivalore

I valori in una colonna multivalore sono identificati da un numero di indice denominato *itagSequence*. Questo numero è un riferimento a un singolo valore della colonna. Questo numero viene usato quando i nuovi valori vengono impostati, recuperati o enumerati nella colonna. *ItagSequence* viene usato in varie strutture, tra cui:

  - [JET_RETINFO](./jet-retinfo-structure.md)

  - [JET_SETINFO](./jet-setinfo-structure.md)

  - [JET_SETCOLUMN](./jet-setcolumn-structure.md)

  - [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)

  - [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)

Questo *itagSequence* inizia da 1 per ogni valore nella colonna multivalore. Il numero di sequenza viene aumentato quando vengono aggiunti nuovi valori alla colonna. L'impostazione di un valore in una colonna con *un valore itagSequence* pari a 0 indica che il valore deve essere aggiunto al set di valori già presenti in tale colonna. *L'uso di un oggetto itagSequence* maggiore del numero di valori attualmente impostati per una colonna avrà lo stesso effetto. Se si specifica *itagSequence* di un valore esistente, tale valore verrà sovrascritto, non ne verrà inserito uno nuovo. Se si imposta un valore esistente su NULL, tale valore verrà rimosso dal set di valori già in tale colonna. In questo modo tutti i valori successivi nella colonna verranno spostati di uno slot verso il basso in modo che l'accesso successivo a tali valori tramite *itagSequence* sia di un numero minore di quello usato in precedenza.

Il diagramma seguente illustra *un oggetto itagSequence* in una colonna multivalore. La colonna denominata ColA ha tre voci: Val1, Val2 e Val3 con *itagSequence* rispettivamente di 1, 2 e 3.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")

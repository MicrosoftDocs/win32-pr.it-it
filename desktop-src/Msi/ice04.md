---
description: ICE04 verifica che il numero di sequenza di ogni file nella tabella file sia minore o uguale al numero di sequenza più grande nella colonna LastSequence della tabella media.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da25a23a26f8a2c49e224ad334791a6081b697b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967797"
---
# <a name="ice04"></a>ICE04

ICE04 verifica che il numero di sequenza di ogni file nella [tabella file](file-table.md) sia minore o uguale al numero di sequenza più grande nella colonna LastSequence della [tabella media](media-table.md).

Ogni record della tabella multimediale rappresenta un disco del supporto di origine contenente tutti i file con un numero di sequenza minore o uguale al valore nella colonna LastSequence e maggiore del valore di LastSequence nel record del disco precedente.

## <a name="result"></a>Risultato

ICE04 Invia un messaggio di errore se è presente un file con un numero di sequenza maggiore del numero di LastSequence più grande per il supporto di origine.

## <a name="example"></a>Esempio

ICE04 segnala l'errore seguente per l'esempio illustrato:

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

[Tabella file](file-table.md) (parziale)



| File   | Sequenza |
|--------|----------|
| MyFile | 210      |



 

[Tabella media](media-table.md) (parziale)



| DiskId | LastSequence |
|--------|--------------|
| 1      | 100          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




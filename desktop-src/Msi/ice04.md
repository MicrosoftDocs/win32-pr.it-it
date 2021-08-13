---
description: ICE04 verifica che il numero di sequenza di ogni file nella tabella File sia minore o uguale al numero di sequenza più grande nella colonna LastSequence della tabella Media.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b77bf11d26d694a25f62db8da005139566b2c92310e2bb2dded4eecbca79719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635663"
---
# <a name="ice04"></a>ICE04

ICE04 verifica che il numero di sequenza di ogni file nella tabella [File](file-table.md) sia minore o uguale al numero di sequenza più grande nella colonna LastSequence della [tabella Media](media-table.md).

Ogni record nella tabella Media rappresenta un disco nel supporto di origine contenente tutti i file con un numero di sequenza minore o uguale al valore nella colonna LastSequence e maggiore del valore LastSequence nel record del disco precedente.

## <a name="result"></a>Risultato

ICE04 invia un messaggio di errore se è presente un file con un numero di sequenza maggiore del numero lastSequence più grande per il supporto di origine.

## <a name="example"></a>Esempio

ICE04 segnala l'errore seguente per l'esempio illustrato:

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

[Tabella file](file-table.md) (parziale)



| File   | Sequenza |
|--------|----------|
| Documento | 210      |



 

[Media Table](media-table.md) (partial)



| DiskId | LastSequence |
|--------|--------------|
| 1      | 100          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




---
description: ICE65 verifica che la tabella dell'ambiente non contenga valori di prefisso o di Accodamento non validi.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3d2b7bcd844c970ccc7fddf376b27c2ec54f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317132"
---
# <a name="ice65"></a>ICE65

ICE65 verifica che la [tabella dell'ambiente](environment-table.md) non contenga valori di prefisso o di Accodamento non validi.

La mancata correzione di un avviso o di un errore segnalato da ICE65 in genere causa problemi di installazione, disinstallazione o ripristino della variabile di ambiente. Ad esempio, è possibile rimuovere solo alcuni valori di una determinata variabile se uno o più valori per tale variabile hanno un separatore finale.

## <a name="result"></a>Risultato

ICE65 Invia un avviso o un errore se nella tabella dell'ambiente sono presenti valori di prefisso o di Accodamento non validi.

## <a name="example"></a>Esempio

ICE65 segnala l'errore e l'avviso seguenti per l'esempio illustrato.

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

Il valore null finale alla fine del valore ( \[ ~ \] ) contrassegna questo valore come anteposto a qualsiasi valore esistente. Il carattere immediatamente prima del valore null (un punto e virgola) diventa il separatore per questo valore. Questo valore dispone anche di un punto e virgola all'inizio della stringa.

Per correggere l'errore, è sufficiente eliminare il punto e virgola principale.

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

Il valore null principale nel valore ( \[ ~ \] ) contrassegna questo valore come accodato a qualsiasi valore esistente. Il carattere immediatamente successivo a null diventa il separatore per questo valore. In questo caso, tale carattere è la lettera "e", che si verifica anche al centro della stringa da accodare. Questa condizione (con un separatore che corrisponde a un carattere all'interno della stringa da accodare) può causare risultati imprevedibili.

La lettera "e", che è una lettera comune, è probabile che sia presente nel valore. Una scelta migliore è ";" o un altro carattere non alfanumerico. (Tuttavia, se il valore è un percorso, ":" e " \\ " e "." sono scelte rischiose).

Per correggere il problema, usare un carattere separatore diverso.

[Tabella ambiente](environment-table.md)



| Componente | Directory | Attributi         | KeyPath       |
|-----------|-----------|--------------------|---------------|
| Var1      | TestVar   | \[~\]; AppendThis   | TestComponent |
| Var2      | TestVar   | \[~\]eAppendThis   | TestComponent |
| Var3      | TestVar   | ; PrependThis;\[~\] | TestComponent |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




---
description: ICE65 verifica che la tabella Environment non abbia valori di prefisso o append non validi.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 543c75f3abe6cb44a405f41bcb788dc71adf85ae954f013244bfc1cded4e6d27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946588"
---
# <a name="ice65"></a>ICE65

ICE65 verifica che la [tabella Environment](environment-table.md) non abbia valori di prefisso o di accodamento non validi.

La mancata correzione di un avviso o di un errore segnalato da ICE65 causa in genere problemi di installazione, disinstallazione o ripristino della variabile di ambiente. Ad esempio, solo alcuni valori di una determinata variabile possono essere rimossi se uno o più valori per tale variabile hanno un separatore finale.

## <a name="result"></a>Risultato

ICE65 invia un avviso o un errore se la tabella dell'ambiente contiene valori di prefisso o di accodamento non validi.

## <a name="example"></a>Esempio

ICE65 segnala l'errore e l'avviso seguenti per l'esempio illustrato.

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

Il valore Null finale alla fine del valore ( ) contrassegna questo valore come anteposto \[ ~ \] a qualsiasi valore esistente. Il carattere immediatamente prima del valore Null (un punto e virgola) diventa il separatore per questo valore. Questo valore include anche un punto e virgola all'inizio della stringa.

Per correggere l'errore, è sufficiente eliminare il punto e virgola iniziale.

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

Il valore Null iniziale nel valore ( ) contrassegna questo valore da \[ ~ \] aggiungere a qualsiasi valore esistente. Il carattere immediatamente dopo null diventa il separatore per questo valore. In questo caso, tale carattere è la lettera "e", che si verifica anche al centro della stringa da aggiungere. Questa condizione (con un separatore uguale a un carattere all'interno della stringa da aggiungere) può causare risultati imprevedibili.

È probabile che la lettera "e", essendo una lettera comune, venga trovata nel valore . Una scelta migliore è ";" o un altro carattere non alfanumerico. Se tuttavia il valore è un percorso, ":" e " \\ " e "." sono scelte rischiose.

Per correggere questo avviso, usare un carattere separatore diverso.

[Tabella dell'ambiente](environment-table.md)



| Componente | Directory | Attributi         | KeyPath       |
|-----------|-----------|--------------------|---------------|
| Var1      | TestVar   | \[~\]; AppendThis   | TestComponent |
| Var2      | TestVar   | \[~\]eAppendThis   | TestComponent |
| Var3      | TestVar   | ; PrependThis;\[~\] | TestComponent |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




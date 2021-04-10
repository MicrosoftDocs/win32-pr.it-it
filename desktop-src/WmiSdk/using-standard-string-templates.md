---
description: Diversi consumer, ad esempio il consumer di eventi di script attivo o il consumer di eventi della riga di comando, hanno proprietà di stringa con il qualificatore del modello.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Utilizzo di modelli di stringa standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc95f4b2b9b9f22e993d1de9cc8b35915918643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883510"
---
# <a name="using-standard-string-templates"></a>Utilizzo di modelli di stringa standard

Diversi consumer, ad esempio il consumer di eventi di script attivo o il consumer di eventi della riga di comando, hanno proprietà di stringa con il qualificatore del **modello** . Queste proprietà utilizzano modelli di stringa standard per costruire una stringa configurata in parte dall'istanza del consumer e in parte da un evento. La struttura di un modello di stringa standard è simile alla specifica della variabile di ambiente Microsoft Windows.

Nell'elenco seguente vengono illustrati alcuni esempi del linguaggio del modello:

-   La stringa "some text here" produce sempre la stringa "some text here".
-   "% CPUUtilization%" produce sempre il valore della proprietà **CPUUtilization** dell'evento da recapitare. Se la proprietà non è una stringa, viene convertita in una stringa. ad esempio, "90" o "TRUE".
-   "L'utilizzo della CPU da parte del processore è% CPUUtilization% al momento" incorpora il valore della proprietà **CPUUtilization** dell'evento nella stringa, producendo un risultato simile al seguente: "l'utilizzo della CPU del processore è 90 al momento".
-   "% TargetInstance. CPUUtilization%" Recupera il valore della proprietà **CPUUtilization** nell'istanza incorporata della proprietà **TargetInstance** .
-   "%%" produce un solo segno di%.
-   Se la proprietà da recuperare è una matrice, l'intera matrice viene prodotta nel formato seguente: "(1, 5, 10, 1024)". Se nella matrice è presente un solo elemento, le parentesi vengono omesse. Se nella matrice non sono presenti elementi, viene prodotto "()".
-   Se una proprietà è un oggetto incorporato, viene prodotta la rappresentazione MOF dell'oggetto (simile al metodo [**IWbemClassObject:: GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) ).
-   Se viene richiesta una proprietà di una matrice incorporata di oggetti, viene considerata come una proprietà con un valore di matrice. Ad esempio:% DriverLetter. TargetInstance .% potrebbe produrre ' ("C:", "D:")' se l'oggetto è una matrice di eventi di modifica dell'istanza incorporata.

## <a name="string-literals"></a>Valori letterali stringa

Qualsiasi elemento all'interno di una coppia di virgolette viene considerato un valore letterale stringa e non verrà sostituito.

Nell'esempio seguente viene illustrata la stringa visualizzata dal compilatore per "utilizzo CPU% CPUUtilization%".

``` syntax
CPU utilization is %CPUUtilization%
```

Questa stringa produce l'output seguente.

``` syntax
CPU utilization is 90
```

D'altra parte, la stringa "utilizzo CPU è \\ "% CPUUtilization% \\ "" viene visualizzata dal compilatore come indicato di seguito.

``` syntax
CPU utilization is "%CPUUtilization%"
```

Questa stringa produce l'output seguente, senza alcuna sostituzione delle variabili.

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 




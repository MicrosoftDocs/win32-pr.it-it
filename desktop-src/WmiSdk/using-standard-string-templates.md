---
description: Diversi consumer, ad esempio Active Script Event Consumer o Command Line Event Consumer, hanno proprietà stringa con il qualificatore Template.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Uso di modelli di stringa standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c60a28730b890a5e922489a47b5b382b545cd6712d61cb976e96b549039ef7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049939"
---
# <a name="using-standard-string-templates"></a>Uso di modelli di stringa standard

Diversi consumer, ad esempio Active Script Event Consumer o Command Line Event Consumer, hanno proprietà stringa con il **qualificatore Template.** Queste proprietà usano modelli di stringa standard per costruire una stringa configurata in parte dall'istanza del consumer e in parte da un evento . La struttura di un modello di stringa standard è simile alla specifica della variabile Windows di ambiente Microsoft.

L'elenco seguente mostra alcuni esempi del linguaggio del modello:

-   La stringa "Some text here" produce sempre la stringa "Some text here".
-   "%CPUUtilization%" produce sempre il valore della **proprietà CPUUtilization** dell'evento recapitato. Se la proprietà non è una stringa, viene convertita in una stringa. ad esempio "90" o "TRUE".
-   "The CPU utilization of this processor is %CPUUtilization% at this time" embeds the value of the **CPUUtilization property** of the event into the string, producing something like, "The CPU utilization of this processor is 90 at this time".
-   "%TargetInstance.CPUUtilization%" recupera il valore della **proprietà CPUUtilization** nell'istanza incorporata della **proprietà TargetInstance.**
-   "%%" produce un singolo segno di % .
-   Se la proprietà recuperata è una matrice, l'intera matrice viene prodotta nel formato seguente: "(1,5,10,1024)". Se nella matrice è presente un solo elemento, le parentesi vengono omesse. Se non sono presenti elementi nella matrice, viene prodotto "()".
-   Se una proprietà è un oggetto incorporato, viene prodotta la rappresentazione MOF dell'oggetto (simile al [**metodo IWbemClassObject::GetObjectText).**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext)
-   Se viene richiesta una proprietà di una matrice incorporata di oggetti , viene considerata come una proprietà con un valore di matrice. Ad esempio: %MyEvents.TargetInstance.DriverLetter% potrebbe produrre '("C:","D:")' se MyEvents è una matrice di eventi di modifica dell'istanza incorporati.

## <a name="string-literals"></a>Valori letterali stringa

Qualsiasi elemento all'interno di una coppia di virgolette viene considerato un valore letterale stringa e non verrà sostituito.

Nell'esempio seguente viene illustrata la stringa visualizzata dal compilatore per "L'utilizzo della CPU è %CPUUtilization%".

``` syntax
CPU utilization is %CPUUtilization%
```

Questa stringa produce l'output seguente.

``` syntax
CPU utilization is 90
```

D'altra parte, la stringa "Utilizzo CPU è \\ "%CPUUtilization% "" viene vista dal compilatore \\ come segue.

``` syntax
CPU utilization is "%CPUUtilization%"
```

Questa stringa produce l'output seguente, senza sostituzione di variabili.

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 




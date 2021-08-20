---
description: L'uso di virgole e punti e virgola può essere il problema di sintassi più complesso nel formato di file e questo utilizzo è molto rigido. Le virgole vengono usate per separare i membri di matrice. I punti e virgola terminano ogni elemento di dati.
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: Uso di virgole e punti e virgola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44d20d4a8e99a75522fa3703d58d82f3bf4dfe130e530d18141b7f45e572717
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044059"
---
# <a name="use-of-commas-and-semicolons"></a>Uso di virgole e punti e virgola

L'uso di virgole e punti e virgola può essere il problema di sintassi più complesso nel formato di file e questo utilizzo è molto rigido. Le virgole vengono usate per separare i membri di matrice. I punti e virgola terminano ogni elemento di dati.

Ad esempio, se un modello viene definito nel modo seguente:


```
template mytemp {
DWORD myvar;
}
```



Un'istanza di questo modello sarà quindi simile alla seguente:


```
mytemp dataTemp {
1;
}
```



Se un modello contenente un altro modello viene definito nel modo seguente.


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
FLOAT aFloat;
mytemp aTemp;
}
```



Un'istanza di questo modello sarà quindi simile alla seguente:


```
container dataContainer {
1.1;
2; 
3;;
}
```



Si noti che la seconda riga che rappresenta mytemp all'interno del contenitore contiene due punti e virgola alla fine della riga. Il primo punto e virgola indica la fine dell'elemento di dati, aTemp (all'interno del contenitore) e il secondo punto e virgola indica la fine del contenitore.

Se una matrice viene definita nel modo seguente:


```
Template mytemp {

array DWORD myvar[3];

}
```



Quindi, un'istanza di è simile alla seguente:


```
mytemp aTemp {
1, 2, 3;
}
```



Nell'esempio di matrice non è necessario che gli elementi di dati siano separati da punti e virgola perché sono delimitati da virgole. Il punto e virgola alla fine contrassegna la fine della matrice.

Si consideri un modello che contiene una matrice di elementi di dati definiti da un modello.


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
DWORD count;
array mytemp tempArray[count];
}
```



Un'istanza di sarà simile all'esempio seguente.


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codifica testo](text-encoding.md)
</dt> </dl>

 

 




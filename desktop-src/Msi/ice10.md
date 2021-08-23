---
description: ICE10 convalida che lo stato di annuncio delle funzionalità figlio corrisponda a quello della funzionalità padre.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80071bdb7f219904c03d7c6b5b947a1bd818af2c3ebc270b0bfb17f2cf185280
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581211"
---
# <a name="ice10"></a>ICE10

ICE10 convalida che lo stato di annuncio delle funzionalità figlio corrisponda a quello della funzionalità padre.

Una funzionalità figlio potrebbe non consentire l'annuncio mentre la funzionalità padre lo consente. La combinazione seguente di attributi padre e figlio non è pertanto valida.

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

Questa combinazione non è valida perché disattiva l'elemento padre ogni volta che l'elemento padre doveva essere annunciato. Tuttavia, è consentito il contrario. Un elemento figlio può essere contrassegnato per favorire l'annuncio mentre l'elemento padre è contrassegnato per non consentire l'annuncio.

L'azione personalizzata ICE10 determina lo stato delle funzionalità padre e figlio dalla colonna Attributi della [tabella](feature-table.md) Funzionalità. Si noti che è valido impostare lo stato di una funzionalità su 0 e impostare il relativo elemento padre o figlio per favorire o non consentire l'annuncio.

## <a name="result"></a>Risultato

ICE10 invia un errore se la colonna Attributi della tabella [Feature](feature-table.md) contiene una mancata corrispondenza nello stato advertise.

## <a name="example"></a>Esempio

ICE10 pubblica il messaggio di errore seguente per l'esempio illustrato.

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

Si noti che per questo esempio Microsoft Excel e Microsoft Word sono funzionalità figlio di Microsoft Office.

[Tabella](feature-table.md) delle funzionalità (parziale)



| Funzionalità | Elemento \_ padre della funzionalità | Attributi |
|---------|-----------------|------------|
| Office  | Null            | 4          |
| Excel   | Office          | 4          |
| Word    | Office          | 8          |



 

Nell'esempio, Word è impostato per non consentire l'annuncio, che è in conflitto con lo stato consenti annuncio del relativo elemento padre, Office.

In alcuni casi ICE10 invia l'errore seguente:

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

Si riferisce a un riferimento a chiave esterna non valido. La correzione è fare in modo che 'Child' punti alla funzionalità padre corretta o aggiungere una voce per la funzionalità padre 'Parent' alla [tabella Feature.](feature-table.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




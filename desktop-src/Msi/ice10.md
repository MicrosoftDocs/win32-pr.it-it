---
description: ICE10 verifica che lo stato di annuncio delle funzionalità figlio corrisponda a quello della relativa funzionalità padre.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac8f1304f4444a0f087d747328cdea4b3d714ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314241"
---
# <a name="ice10"></a>ICE10

ICE10 verifica che lo stato di annuncio delle funzionalità figlio corrisponda a quello della relativa funzionalità padre.

Una funzionalità figlio potrebbe non impedire l'annuncio quando la funzionalità padre consente l'annuncio. La seguente combinazione di attributi padre e figlio non è quindi valida.

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

Questa combinazione non è valida perché potrebbe disattivare l'elemento padre ogni volta che l'elemento padre doveva essere pubblicizzato. È tuttavia consentito il contrario. Un elemento figlio può essere contrassegnato per favorire l'annuncio mentre l'elemento padre è contrassegnato per non consentire l'annuncio.

L'azione personalizzata ICE10 determina lo stato delle funzionalità padre e figlio dalla colonna attributi della tabella delle [funzionalità](feature-table.md) . Si noti che è possibile impostare lo stato di una funzionalità su 0 e che l'elemento padre o figlio impostato su predilige o non consenta l'annuncio.

## <a name="result"></a>Risultato

ICE10 Invia un errore se la colonna Attributes della tabella [feature](feature-table.md) contiene una mancata corrispondenza nello stato advertise.

## <a name="example"></a>Esempio

ICE10 invia il messaggio di errore seguente per l'esempio illustrato.

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

Si noti che per questo esempio Microsoft Excel e Microsoft Word sono funzionalità figlio di Microsoft Office.

Tabella delle [funzionalità](feature-table.md) (parziale)



| Funzionalità | \_Elemento padre della funzionalità | Attributi |
|---------|-----------------|------------|
| Office  | Null            | 4          |
| Excel   | Office          | 4          |
| Word    | Office          | 8          |



 

Nell'esempio, Word è impostato su non consentire l'annuncio pubblicitario, che è in conflitto con lo stato Consenti annuncio del padre, Office.

In alcuni casi ICE10 invia l'errore seguente:

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

Si riferisce a un riferimento di chiave esterna non valido. Per risolvere il problema, è necessario che "Child" punti alla relativa funzionalità padre corretta oppure aggiungere una voce per la funzionalità padre ' Parent ' alla tabella [feature](feature-table.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




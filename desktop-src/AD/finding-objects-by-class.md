---
title: Ricerca di oggetti per classe
description: Una tipica query di ricerca per una classe di oggetti specifica.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Ricerca di oggetti per classe AD
- Active Directory, uso, ricerca, per classe
- oggetto AD , ricerca per classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81d90dbcd50a3ce001c1dec57d8fafb0f1987376cf71314902b7f035f923512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189170"
---
# <a name="finding-objects-by-class"></a>Ricerca di oggetti per classe

Una tipica query di ricerca per una classe di oggetti specifica. L'esempio di codice seguente cerca i computer con posizione nell'edificio 7N.


```C++
(&(objectCategory=computer)(location=Building 7N))
```



Considerare il **motivo per cui objectClass** non viene usato. Non usare **objectClass senza** un altro confronto che contiene un attributo indicizzato. Gli attributi dell'indice possono aumentare l'efficienza di una query. **L'attributo objectClass** è multivalore e non indicizzato. Per specificare il tipo o la classe di un oggetto, usare **objectCategory.**

Meno efficiente:


```C++
(objectClass=computer)
```



Più efficiente:


```C++
(objectCategory=computer)
```



Tenere presente che in alcuni casi è necessario usare una combinazione di **objectClass** e **objectCategory.** La classe utente e la classe contact devono essere specificate come indicato di seguito.


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



Tenere presente che è possibile cercare sia utenti che contatti con quanto segue.


```C++
(objectCategory=person)
```



 

 





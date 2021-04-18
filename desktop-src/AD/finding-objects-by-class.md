---
title: Ricerca di oggetti per classe
description: Query di ricerca tipiche per una classe di oggetti specifica.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Ricerca di oggetti per classe AD
- Active Directory, utilizzo, ricerca, per classe
- oggetto AD, ricerca per classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297735"
---
# <a name="finding-objects-by-class"></a>Ricerca di oggetti per classe

Query di ricerca tipiche per una classe di oggetti specifica. Nell'esempio di codice seguente viene eseguita la ricerca di computer con percorso nella compilazione di 7N.


```C++
(&(objectCategory=computer)(location=Building 7N))
```



Considerare il motivo per cui **objectClass** non viene utilizzato. Non utilizzare **objectClass** senza un altro confronto che contenga un attributo indicizzato. Gli attributi di indice possono aumentare l'efficienza di una query. L'attributo **objectClass** è multivalore e non indicizzato. Per specificare il tipo o la classe di un oggetto, usare **objectCategory**.

Meno efficiente:


```C++
(objectClass=computer)
```



Maggiore efficienza:


```C++
(objectCategory=computer)
```



Tenere presente che in alcuni casi è necessario usare una combinazione di **objectClass** e **objectCategory** . È necessario specificare la classe utente e la classe Contact come indicato di seguito.


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



Tenere presente che è possibile cercare gli utenti e i contatti con il codice seguente.


```C++
(objectCategory=person)
```



 

 





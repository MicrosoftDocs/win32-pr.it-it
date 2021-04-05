---
title: Cerca solo attributi
description: A volte viene eseguita una ricerca per determinare il tipo di dati disponibile per un oggetto.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Cerca solo attributi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c2a97873dfb52f56b123919c3eedd277a63a74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955085"
---
# <a name="search-attributes-only"></a>Cerca solo attributi

A volte viene eseguita una ricerca per determinare il tipo di dati disponibile per un oggetto. In questo caso, si è interessati solo agli attributi e non ai valori dell'oggetto. A tale scopo, è necessario impostare l'opzione "Cerca solo attributi". Se si specifica questa opzione, vengono restituiti i nomi di attributo senza i relativi valori. Il set di risultati include tuttavia solo gli attributi a cui sono assegnati valori. Si consideri, ad esempio, un oggetto con gli attributi seguenti:

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

Quando viene impostata l'opzione solo attributi di ricerca, il set di risultati include:

``` syntax
First Name
Last Name
Phone Number
```

Per ulteriori informazioni sull'utilizzo dell'opzione solo attributi di ricerca con un'interfaccia di ricerca specifica, vedere:

-   [Restituzione solo dei nomi di attributo con IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)
-   [Ricerca con ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

 

 





---
title: Cerca solo attributi
description: In alcuni casi si esegue una ricerca per determinare il tipo di dati disponibili per un oggetto.
ms.assetid: 97eccea6-6a2b-4785-afd8-4af3dc7bd657
ms.tgt_platform: multiple
keywords:
- Cerca solo attributi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b1775c759975a508f5382ef2a30f290ac4a96b3b92120d4face6b1d0556426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443931"
---
# <a name="search-attributes-only"></a>Cerca solo attributi

In alcuni casi si esegue una ricerca per determinare il tipo di dati disponibili per un oggetto. In questo caso, si è interessati solo agli attributi e non ai valori dell'oggetto. A tale scopo, impostare l'opzione "solo attributi di ricerca". Se si specifica questa opzione, i nomi degli attributi vengono restituiti senza i relativi valori. Tuttavia, il set di risultati include solo gli attributi a cui sono assegnati valori. Si consideri ad esempio un oggetto con gli attributi seguenti:

``` syntax
First Name = Jeff
Last Name = Smith
Department = <Empty>
Phone Number = (425) 432-3442
```

Quando è impostata l'opzione solo attributi di ricerca, il set di risultati include:

``` syntax
First Name
Last Name
Phone Number
```

Per altre informazioni sull'uso dell'opzione solo attributi di ricerca con un'interfaccia di ricerca specifica, vedere:

-   [Restituzione solo dei nomi di attributo con IDirectorySearch](returning-only-attribute-names-with-idirectorysearch.md)
-   [Ricerca con oggetti ActiveX dati](searching-with-activex-data-objects-ado.md)
-   [Ricerca con OLE DB](searching-with-ole-db.md)

 

 





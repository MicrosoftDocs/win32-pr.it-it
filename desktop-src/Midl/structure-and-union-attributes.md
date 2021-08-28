---
title: Attributi di struttura e unione
description: Usare \_ l'opzione \ attributes per specificare la caratteristica di un'unione in una chiamata di procedura remota. Usare l'attributo ignore per designare determinati membri di struttura o unione come locali per l'applicazione client.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- IDL MIDL, attributi, struttura e unione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc179632bb7e0d64b777f3c8a08b9de2af7bbf818978d6bb0a7ee2ea8b515542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066671"
---
# <a name="structure-and-union-attributes"></a>Attributi di struttura e unione

Usare gli **attributi switch \_** per specificare la caratteristica di \* un'unione in una chiamata di procedura remota. Usare [**l'attributo ignore**](ignore.md) per designare determinati membri di struttura o unione come locali per l'applicazione client.



| Attributo                           | Utilizzo                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Interruttore**](switch.md)            | Seleziona il discriminante per un'unione incapsulata.                                                                           |
| [**\_l'opzione è**](switch-is.md)     | Identifica la discriminante per un'unione non incapsulata.                                                                      |
| [**tipo di \_ commutatore**](switch-type.md) | Identifica il tipo di discriminante per un'unione non incapsulata.                                                          |
| [**Ignorare**](ignore.md)            | Indica che un puntatore contenuto in una struttura o in un'unione e l'oggetto indicato dal puntatore non devono essere trasmessi. |



 

È anche possibile usare gli attributi [di matrice e ridimensionato del puntatore](array-and-sized-pointer-attributes.md) per specificare le caratteristiche dei membri della struttura o dell'unione.

 

 





---
title: Attributi di struttura e di Unione
description: Utilizzare l'opzione \_ \ attributi per specificare la caratteristica di un'Unione in una chiamata di procedura remota. Usare l'attributo Ignore per definire determinati membri di struttura o di Unione come locali per l'applicazione client.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- MIDL, attributi, struttura e unione IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2a7764d56c8557bd71923021a9f324a118ac81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471142"
---
# <a name="structure-and-union-attributes"></a>Attributi di struttura e di Unione

Utilizzare gli **attributi \_ Switch** \* per specificare la caratteristica di un'Unione in una chiamata di procedura remota. Usare l'attributo [**Ignore**](ignore.md) per definire determinati membri di struttura o di Unione come locali per l'applicazione client.



| Attributo                           | Utilizzo                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**commutatore**](switch.md)            | Seleziona discriminante per un'Unione incapsulata.                                                                           |
| [**opzione \_**](switch-is.md)     | Identifica discriminante per un'Unione non incapsulata.                                                                      |
| [**tipo di opzione \_**](switch-type.md) | Identifica il tipo di discriminante per un'Unione non incapsulata.                                                          |
| [**ignorare**](ignore.md)            | Indica che un puntatore contenuto in una struttura o in un'Unione e l'oggetto indicato dal puntatore non devono essere trasmessi. |



 

Per specificare le caratteristiche dei membri di struttura o di Unione, è inoltre possibile utilizzare la [matrice e gli attributi del puntatore ridimensionati](array-and-sized-pointer-attributes.md) .

 

 





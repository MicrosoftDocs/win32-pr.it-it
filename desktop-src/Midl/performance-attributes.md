---
title: Attributi relativi alle prestazioni
description: Utilizzare i seguenti attributi in un file IDL per ridurre le dimensioni del codice stub o per migliorare le prestazioni.
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- MIDL, attributi e prestazioni di IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbfa518b400d237c9fd3789f61b7e74a0c38276
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045353"
---
# <a name="performance-attributes"></a>Attributi relativi alle prestazioni

Utilizzare i seguenti attributi in un file IDL per ridurre le dimensioni del codice stub o per migliorare le prestazioni.



| Attributo                             | Utilizzo                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ignorare**](ignore.md)              | Indica che un puntatore contenuto in una struttura o in un'Unione e l'oggetto indicato dal puntatore non devono essere trasmessi.                        |
| [**locale**](local.md)                | Definisce una funzione locale per l'applicazione per la quale MIDL non deve generare codice stub.                                           |
| [**\_marshalling di rete**](wire-marshal.md) | Definisce un tipo di dati come tipo più semplice per la trasmissione in rete e consente di implementare routine di marshalling e di unmarshalling per il tipo. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi ACF di gestione della memoria](memory-management-acf-attributes.md)
</dt> <dt>

[Attributi ACF di ottimizzazione Stub](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 





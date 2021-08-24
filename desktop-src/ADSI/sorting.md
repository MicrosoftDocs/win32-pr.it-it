---
title: Ordinamento (ADSI)
description: Un client può richiedere a un server di ordinare il set di risultati.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555b4b6f1868b2e4fddc1891cdf349ef6f44bc47dca6eb80e021ec49cb91b5d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082225"
---
# <a name="sorting-adsi"></a>Ordinamento (ADSI)

Un client può richiedere a un server di ordinare il set di risultati. È possibile specificare:

-   Ordinamento: è possibile specificare l'ordinamento crescente o decrescente.
-   Attributi di ordinamento: è possibile specificare più attributi in una stringa di ordinamento. Ad esempio, ordinare in base al cognome e quindi a Nome.

Quando si specifica l'ordinamento, è consigliabile provare a usare uno degli attributi indicizzati. In caso contrario, il server deve calcolare un set di risultati completo prima di inviarlo al client. Questo vale anche se è stata richiesta una ricerca di pagine e sono state specificate le dimensioni della pagina.

> [!Note]  
> Non tutti i server di directory supportano più tipi di ordinamento o ordinamento degli attributi.

 

 

 





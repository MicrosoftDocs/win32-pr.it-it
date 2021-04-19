---
title: Ordinamento (ADSI)
description: Un client può richiedere un server per ordinare il set di risultati.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4ee790a646367366afe33639abd8f5aa57ed4f
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2019
ms.locfileid: "106299323"
---
# <a name="sorting-adsi"></a>Ordinamento (ADSI)

Un client può richiedere un server per ordinare il set di risultati. È possibile specificare:

-   Tipo di ordinamento: è possibile specificare l'ordinamento crescente o decrescente.
-   Attributi di ordinamento: è possibile specificare più attributi in una stringa di ordinamento. Ad esempio, Ordina in base al cognome e quindi al nome.

Quando si specifica l'ordinamento, provare a usare uno degli attributi indicizzati. In caso contrario, è necessario che il server calcoli un set di risultati completo prima di inviarlo al client. Questo vale anche se è stata richiesta una ricerca di paging e sono state specificate le dimensioni della pagina.

> [!Note]  
> Non tutti i server di directory supportano più tipi di attributi o ordinamento.

 

 

 





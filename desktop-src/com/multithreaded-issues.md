---
title: Problemi multithread
description: Problemi multithread
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910e1602d00d3429bb9e4c7a1667bf8113cd659
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104397007"
---
# <a name="multi-threaded-issues"></a>Problemi multithread

OLE fornisce supporto per le applicazioni multithreading, consentendo alle applicazioni di effettuare chiamate OLE da più thread. Questo supporto multithreading è denominato modello di Apartment, è importante che tutti i componenti OLE che usano più thread seguano questo modello. Il modello di Apartment richiede che i puntatori di interfaccia vengano sottoposti a marshalling (tramite [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)e [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) quando vengono passati tra thread.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Processi, thread e Apartment](processes--threads--and-apartments.md)
</dt> </dl>

 

 





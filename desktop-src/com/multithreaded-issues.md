---
title: Problemi a più thread
description: Problemi a più thread
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ffd1dc3f73c33ca30ebee0072f1c5059c73f25e9e2318d384cd0c3d0dc7bc94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918531"
---
# <a name="multi-threaded-issues"></a>Problemi a più thread

OLE fornisce il supporto per le applicazioni multithreading, consentendo alle applicazioni di effettuare chiamate OLE da più thread. Questo supporto multithreading è denominato modello apartment. È importante che tutti i componenti OLE che usano più thread seguano questo modello. Il modello di apartment richiede il marshalling dei puntatori a interfaccia (tramite [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)e [**CoUnmarshalInterface)**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)quando vengono passati tra thread.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Processi, thread e apartment](processes--threads--and-apartments.md)
</dt> </dl>

 

 





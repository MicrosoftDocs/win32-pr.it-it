---
title: Svantaggi
description: Svantaggi
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a22e409414a1df60e2dd9dff3adbfc6000b953a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516006"
---
# <a name="disadvantages"></a>Svantaggi

I server in-process forniscono la velocità e le dimensioni vantaggiose di un gestore di oggetti con la funzionalità di modifica di un server locale. Quindi, perché scegliere di implementare l'applicazione OLE come server locale anziché come server in-process? Esistono diversi motivi:

-   Sicurezza. Solo un server locale ha lo spazio degli indirizzi isolato rispetto a quello del client. Un server in-process condivide lo spazio di indirizzi e il contesto di processo del client e pertanto può essere meno affidabile in caso di errori o di programmazione dannosa.
-   Granularità. Un server locale può ospitare più istanze del relativo oggetto in molti client diversi, condividendo lo stato del server tra oggetti in più client in modi che sarebbero difficili o impossibili se implementati come server in-process, che è semplicemente una DLL caricata in ogni client.
-   Compatibilità. Se si sceglie di implementare un server in-process, si rinuncia alla compatibilità con OLE 1, che non supporta tali server. Questo non è un aspetto da considerare per molti sviluppatori, ma, in caso contrario, si tratta di un problema critico.
-   Impossibilità di supportare i collegamenti. Un server in-process non può fungere da origine di collegamento. Poiché una DLL non può essere eseguita da sola, non può creare un oggetto file a cui essere collegato.

Nonostante questi svantaggi, un server in-process può essere un'ottima scelta per la velocità e le dimensioni, se è adatto a tutti gli altri requisiti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vantaggi](advantages.md)
</dt> <dt>

[Server in-process](in-process-servers.md)
</dt> </dl>

 

 





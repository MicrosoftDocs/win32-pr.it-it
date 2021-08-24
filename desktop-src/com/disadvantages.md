---
title: Svantaggi
description: Svantaggi
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2b9d41a632c202a25c3383ffb2d1069505c0dc988651e9fc886cfeecca5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501116"
---
# <a name="disadvantages"></a>Svantaggi

I server in-process offrono il vantaggio di velocità e dimensioni di un gestore di oggetti con la funzionalità di modifica di un server locale. Perché quindi si dovrebbe scegliere di implementare l'applicazione OLE come server locale anziché come server in-process? Esistono diversi motivi:

-   Sicurezza. Solo un server locale ha lo spazio degli indirizzi isolato da quello del client. Un server in-process condivide lo spazio degli indirizzi e il contesto del processo del client e può quindi essere meno affidabile in caso di errori o programmazione dannosa.
-   Granularità. Un server locale può ospitare più istanze del relativo oggetto tra molti client diversi, condividendo lo stato del server tra oggetti in più client in modi difficili o impossibili se implementati come server in-process, ovvero semplicemente una DLL caricata in ogni client.
-   Compatibilità. Se si sceglie di implementare un server in-process, si rinuncia alla compatibilità con OLE 1, che non supporta tali server. Questo non sarà una considerazione per molti sviluppatori, ma se lo è, è di importanza critica.
-   Impossibilità di supportare i collegamenti. Un server in-process non può fungere da origine di collegamento. Poiché una DLL non può essere eseguita da sola, non può creare un oggetto file a cui collegarsi.

Nonostante questi svantaggi, un server in-process può essere una scelta eccellente per la velocità e le dimensioni, se soddisfa tutti gli altri requisiti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vantaggi](advantages.md)
</dt> <dt>

[Server in-process](in-process-servers.md)
</dt> </dl>

 

 





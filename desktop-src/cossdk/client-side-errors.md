---
description: Errori Client-Side
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Errori Client-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef309858d1527fdcabe0f487de87df19d20635c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304649"
---
# <a name="client-side-errors"></a>Errori Client-Side

Gli errori sul lato client vengono gestiti in modo analogo agli errori sul lato server. [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) può spostare un messaggio nella coda di destinazione se, ad esempio, il messaggio non può essere spostato da client a server. In questo caso, il messaggio viene spostato nella coda dei messaggi non recapitabili sul lato client.

Il servizio componenti in coda COM+ monitora la coda dei messaggi non recapitabili. Se i messaggi sono stati spostati, il servizio componenti in coda crea un'istanza della classe Exception e chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per richiedere [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol). Se l'operazione ha esito positivo, il monitoraggio della coda dei messaggi non recapitabili richiama [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).

L'oggetto può intraprendere alcune azioni per invertire l'effetto di una transazione precedente. Se viene eseguito il commit della riproduzione, il messaggio viene rimosso dalla coda dei messaggi non recapitabili di XACT. Se la riproduzione ha esito negativo o il CLSID e l'interfaccia necessari non sono disponibili, il messaggio rimane nella coda dei messaggi non recapitabili XACT.

Se è necessario intervenire nel processo descritto in precedenza o se è necessario spostare un messaggio non elaborabile dalla coda di riposo finale, usare l'utilità di spostamento messaggi. Per ulteriori informazioni sull'utilità Message Mover, vedere [gestione degli errori](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori persistenti Client-Side](persistent-client-side-failures.md)
</dt> <dt>

[Errori sul lato server](server-side-errors.md)
</dt> </dl>

 

 

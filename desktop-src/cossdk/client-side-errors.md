---
description: Client-Side errori
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Client-Side errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c27c73cd2be39d98c881021e1a042f15dc623766af0d52a578c6cd49c30e0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129363"
---
# <a name="client-side-errors"></a>Client-Side errori

Gli errori lato client vengono gestiti in modo analogo agli errori lato server. [Accodamento messaggi può](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) spostare un messaggio nella coda di destinazione se, ad esempio, il messaggio non può essere spostato da client a server. In questo caso, il messaggio viene spostato nella coda dei messaggi non recapitali sul lato client.

Il servizio componenti in coda COM+ monitora la coda dei messaggi non recapitati. Se i messaggi sono stati spostati, il servizio dei componenti in coda crea un'istanza della classe di eccezione e chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per richiedere [**IPlaybackControl.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) Se l'operazione ha esito positivo, il monitoraggio della coda dei messaggi non recapitare richiama [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).

L'oggetto può eseguire un'azione per invertire l'effetto di una transazione precedente. Se viene eseguito il commit della riproduzione, il messaggio viene rimosso dalla coda di messaggi non recapitare Xact. Se la riproduzione ha esito negativo o il CLSID e l'interfaccia necessari non sono disponibili, il messaggio rimane nella coda di messaggi non recapitati Xact.

Se è necessario intervenire nel processo descritto in precedenza o se è necessario spostare un messaggio non elaborabile dalla coda in attesa finale, usare l'utilità di spostamento dei messaggi. Per altre informazioni sull'utilità di spostamento dei messaggi, vedere [Gestione degli errori](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori Client-Side persistenti](persistent-client-side-failures.md)
</dt> <dt>

[Errori lato server](server-side-errors.md)
</dt> </dl>

 

 

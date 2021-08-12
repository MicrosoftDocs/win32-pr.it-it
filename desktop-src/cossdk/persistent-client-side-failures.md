---
description: Errori Client-Side persistenti
ms.assetid: f991db71-8319-414d-8a25-2d02bc7c8b51
title: Errori Client-Side persistenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e832ec8339c33263600a1657b8d29ef2d2aecf4ceb3e000666f9db5776b3ac13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305774"
---
# <a name="persistent-client-side-failures"></a>Errori Client-Side persistenti

In alcuni casi, [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) può spostare un messaggio nella coda di destinazione. Ad esempio, se i controlli di accesso alla coda non consentono lo spostamento del messaggio dal client al server, il messaggio in errore viene spostato nella coda dei messaggi non recapitati sul lato client. In questo caso, il servizio componenti in coda COM+ consente di associare una classe di eccezione a un componente. Per associare la classe di eccezione al componente, usare la **scheda** Avanzate nella pagina delle proprietà del componente dello strumento di amministrazione di Servizi componenti. È anche possibile associare la classe di eccezione a livello di codice, usando l'attributo del componente del catalogo ExceptionClass delle funzioni amministrative COM+.

La classe di eccezione è definita come ProgID o CLSID di un componente che implementa [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol). Il servizio componenti in coda dispone di un monitoraggio della coda di messaggi non recapitati che analizza la coda dei messaggi non recapitati Xact. Se nella coda è presente un messaggio, il monitoraggio della coda dei messaggi non recapitabili crea un'istanza del gestore eccezioni associato al componente di destinazione e chiama [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry), a indicare che si è verificato un errore irreversibile sul lato client.

Oltre a [**IPlaybackControl,**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol)il gestore eccezioni deve implementare lo stesso set di interfacce del componente server per cui gestisce le eccezioni. Quando [**viene chiamato IPlaybackControl::FinalClientRetry,**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) il run-time dei componenti in coda riproduce il messaggio non riuscito nel gestore eccezioni. Ciò consente al gestore eccezioni di implementare un comportamento alternativo per i messaggi che non possono essere spostati nel server, ad esempio generando una transazione di compensazione.

Se il gestore eccezioni completa tutte le chiamate al metodo riprodotte, il messaggio viene rimosso dalla coda dei messaggi non recapitati Xact e viene ignorato. Se, tuttavia, il gestore eccezioni interrompe il messaggio restituisce uno stato di errore da una delle chiamate al metodo, il messaggio viene restituito alla coda dei messaggi non recapitare Xact. La sequenza di eventi seguente mostra come vengono gestite le eccezioni sul lato client:

1.  Accodamento messaggi non riesce a recapitare un messaggio al server e lo inserisce nella coda di messaggi non recapitati Xact.
2.  Il listener della coda di messaggi non recapitare (DLQL) trova un messaggio nella coda dei messaggi non recapitare Xact.
3.  DLQL recupera il CLSID del componente di destinazione dal messaggio e verifica la presenza di una classe di eccezione.
4.  DLQL crea un'istanza della classe di eccezione.
5.  DLQL esegue una query [**per IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) per la classe di eccezione.
6.  DLQL chiama il [**metodo IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) nella classe di eccezione.
7.  DLQL riproduce tutte le chiamate di proprietà e metodi dal messaggio alla classe di eccezione.
8.  DLQL elimina il messaggio se il gestore eccezioni completa correttamente la transazione. Il gestore delle eccezioni può generare [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)e il messaggio rimarrà nella coda dei messaggi non recapitare.

Se uno dei passaggi precedenti ha esito negativo, il messaggio viene lasciato nella coda dei messaggi non recapitare Xact.

All'avvio, DLQL legge ogni messaggio nella coda dei messaggi non recapitati transazionali di Accodamento messaggi e crea un'istanza della classe di eccezione per ogni messaggio dei componenti in coda. Dopo un passaggio attraverso la coda, attende nuovi messaggi. Elabora quindi ogni nuovo messaggio della coda di messaggi non recapitati all'arrivo.

Se è necessario intervenire nel processo descritto qui o se è necessario spostare un messaggio non elaborabile dalla coda di attesa finale, usare l'utilità di spostamento dei messaggi. Per altre informazioni sull'utilità di spostamento dei messaggi, vedere [Gestione degli errori](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori sul lato client](client-side-errors.md)
</dt> <dt>

[Errori sul lato server](server-side-errors.md)
</dt> </dl>

 

 




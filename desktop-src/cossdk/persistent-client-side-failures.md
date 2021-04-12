---
description: Errori persistenti Client-Side
ms.assetid: f991db71-8319-414d-8a25-2d02bc7c8b51
title: Errori persistenti Client-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d303e712257d62e4ae42497cb4463e782cfbb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401452"
---
# <a name="persistent-client-side-failures"></a>Errori persistenti Client-Side

In alcuni casi, [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) può spostare un messaggio nella coda di destinazione. Se, ad esempio, i controlli di accesso della coda non consentono lo spostamento del messaggio da client a server, il messaggio danneggiato viene spostato nella coda di messaggi non recapitabili sul lato client. Quando si verifica questa situazione, il servizio COM+ Queued Components consente di associare una classe di eccezione a un componente. Per associare la classe Exception al componente, utilizzare la scheda **Avanzate** della pagina Proprietà componente dello strumento di amministrazione Servizi componenti. È anche possibile associare la classe di eccezione a livello di codice, usando l'attributo Component Catalog P:System.EnterpriseServices.ExceptionClassAttribute.value delle funzioni amministrative COM+.

La classe Exception è definita come ProgID o CLSID di un componente che implementa [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol). Il servizio componenti in coda dispone di un monitoraggio coda messaggi non recapitabili che esegue l'analisi della coda dei messaggi non recapitabili. Se è presente un messaggio nella coda, il monitoraggio della coda dei messaggi non recapitabili crea un'istanza del gestore di eccezioni associato al componente di destinazione e chiama [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry), a indicare che si è verificato un errore irreversibile sul lato client.

Oltre a [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol), il gestore di eccezioni deve implementare lo stesso set di interfacce del componente server per cui gestisce le eccezioni. Quando viene chiamato [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) , la fase di esecuzione dei componenti in coda riproduce il messaggio non riuscito nel gestore di eccezioni. Ciò consente al gestore di eccezioni di implementare un comportamento alternativo per i messaggi che non possono essere spostati nel server, ad esempio generando una transazione di compensazione.

Se il gestore di eccezioni completa tutte le chiamate al metodo riprodotte, il messaggio viene rimosso dalla coda dei messaggi non recapitabili di XACT e viene rimosso. Se, tuttavia, il gestore di eccezioni interrompe il messaggio restituendo uno stato di errore da una delle chiamate al metodo, il messaggio viene restituito alla coda dei messaggi non recapitabili XACT. La sequenza di eventi seguente mostra come vengono gestite le eccezioni sul lato client:

1.  Accodamento messaggi non è in grado di recapitare un messaggio al server e inserisce il messaggio nella coda dei messaggi non recapitabili XACT.
2.  Il listener della coda dei messaggi non recapitabili (DLQL) rileva un messaggio nella coda dei messaggi non recapitabili di XACT.
3.  DLQL Recupera il CLSID del componente di destinazione dal messaggio e verifica la presenza di una classe di eccezione.
4.  DLQL crea un'istanza della classe Exception.
5.  DLQL esegue una query per [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) per la classe Exception.
6.  DLQL chiama il metodo [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) nella classe Exception.
7.  Il DLQL riproduce tutte le chiamate a proprietà e metodi dal messaggio alla classe di eccezione.
8.  DLQL Elimina il messaggio se il gestore di eccezioni completa correttamente la transazione. Il gestore di eccezioni può eseguire [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)e il messaggio rimarrà nella coda dei messaggi non recapitabili.

Se uno dei passaggi precedenti ha esito negativo, il messaggio viene lasciato nella coda dei messaggi non recapitabili XACT.

Quando viene avviato, DLQL legge ogni messaggio nella coda di messaggi non recapitabili transazionale di Accodamento messaggi e crea un'istanza della classe Exception per ogni messaggio di componenti in coda. Una volta passato attraverso la coda, resta in attesa di nuovi messaggi. Elabora quindi ogni nuovo messaggio della coda dei messaggi non recapitabili in arrivo.

Se è necessario intervenire nel processo descritto qui o se è necessario spostare un messaggio non elaborabile dalla coda di riposo finale, usare l'utilità di spostamento messaggi. Per ulteriori informazioni sull'utilità Message Mover, vedere [gestione degli errori](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori lato client](client-side-errors.md)
</dt> <dt>

[Errori sul lato server](server-side-errors.md)
</dt> </dl>

 

 




---
title: Sequenza di avvio
description: Procedura per avviare il protocollo personalizzato.
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29dbb899905dd96e806ffe17a0eafd0091ad97b547ba9f172527ab0acc1b2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000546"
---
# <a name="start-sequence"></a>Sequenza di avvio

Per avviare il provider di protocolli, Servizi Desktop remoto servizio:

-   Recupera il nome del listener e il CLSID dell'oggetto di gestione protocollo ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) dal Registro di sistema. Per altre informazioni, vedere [Registrazione di Protocol Manager.](registering-the-custom-protocol.md)
-   Chiama [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) per inizializzare il gestore di protocolli.
-   Crea un oggetto di gestione protocollo usando il CLSID. Anche se sono presenti più listener registrati per lo stesso provider di protocolli, il servizio crea un solo oggetto di gestione protocolli.
-   Chiama [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) per indicare all'oggetto gestore di protocollo di creare un oggetto listener [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) e restituirlo al servizio. L'oggetto gestore di protocolli deve aggiungere un riferimento all'oggetto listener prima di restituirlo al servizio. Il servizio rilascerà l'oggetto quando il servizio viene arrestato o il listener viene eliminato.
-   Chiama [**StartListen sull'oggetto**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) listener in modo che il listener possa avviare l'ascolto delle connessioni in ingresso.
-   Chiama [**StopListen per**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) arrestare l'ascolto dell'oggetto listener.
-   Chiama [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) per annullare l'inizializzazione della gestione protocolli.

Il listener crea un [**oggetto IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) quando un client tenta di connettersi. L'oggetto listener chiama [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) per notificare al servizio Servizi Desktop remoto che un nuovo client sta tentando di connettersi o riconnettersi e passa l'oggetto **IWRdsProtocolConnection** nella chiamata. Il Servizi Desktop remoto restituirà a sua volta un oggetto [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) nella chiamata in modo che il protocollo possa comunicare con il servizio Servizi Desktop remoto in base alle esigenze. Il servizio aggiunge un riferimento all'oggetto callback prima della restituzione e il protocollo deve rilasciare tale riferimento alla chiusura della connessione.

La figura seguente illustra l'interazione tra i vari oggetti durante l'avvio.

![Sequenza di avvio rcm](images/protocol-startsequence.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenza di chiamate al metodo](method-call-sequence.md)
</dt> <dt>

[Sequenza di connessione](connection-sequence.md)
</dt> </dl>

 

 





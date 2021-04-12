---
title: Sequenza di avvio
description: Procedura per avviare il protocollo personalizzato.
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af0716e39d1df96bbdf29f4a3abbb14e32bc752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221020"
---
# <a name="start-sequence"></a>Sequenza di avvio

Per avviare il provider di protocolli, il servizio Servizi Desktop remoto:

-   Recupera il nome del listener e il CLSID dell'oggetto del gestore di protocollo ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) dal registro di sistema. Per ulteriori informazioni, vedere [la pagina relativa alla registrazione di gestione protocolli](registering-the-custom-protocol.md).
-   Chiama [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) per inizializzare Gestione protocolli.
-   Crea un oggetto di gestione protocollo usando il CLSID. Anche se sono presenti più listener registrati per lo stesso provider di protocollo, il servizio crea solo un oggetto di gestione protocolli.
-   Chiama [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) per indicare all'oggetto di gestione protocollo di creare un oggetto listener [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) e restituirlo al servizio. L'oggetto di gestione protocolli deve aggiungere un riferimento all'oggetto listener prima di restituirlo al servizio. Il servizio rilascerà l'oggetto quando il servizio viene arrestato o il listener viene eliminato.
-   Chiama [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) sull'oggetto listener in modo che il listener possa iniziare ad ascoltare le connessioni in ingresso.
-   Chiama [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) per arrestare l'attesa dell'oggetto listener.
-   Chiama [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) per annullare l'inizializzazione di gestione protocolli.

Il listener crea un oggetto [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) quando un client tenta di connettersi. L'oggetto listener chiama [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) per notificare al servizio Servizi Desktop remoto che un nuovo client sta tentando di connettersi o riconnettersi e passa l'oggetto **IWRdsProtocolConnection** nella chiamata. Il servizio Servizi Desktop remoto restituirà a sua volta un oggetto [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) nella chiamata, in modo che il protocollo possa comunicare con il servizio Servizi Desktop remoto in base alle esigenze. Il servizio aggiunge un riferimento all'oggetto callback prima della restituzione e il protocollo deve rilasciare tale riferimento alla chiusura della connessione.

Nella figura seguente viene illustrata l'interazione tra i vari oggetti durante l'avvio.

![sequenza di avvio RCM](images/protocol-startsequence.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sequenza di chiamate al metodo](method-call-sequence.md)
</dt> <dt>

[Sequenza di connessione](connection-sequence.md)
</dt> </dl>

 

 





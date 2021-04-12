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
# <a name="start-sequence"></a><span data-ttu-id="7e6a8-103">Sequenza di avvio</span><span class="sxs-lookup"><span data-stu-id="7e6a8-103">Start Sequence</span></span>

<span data-ttu-id="7e6a8-104">Per avviare il provider di protocolli, il servizio Servizi Desktop remoto:</span><span class="sxs-lookup"><span data-stu-id="7e6a8-104">To start your protocol provider, the Remote Desktop Services service:</span></span>

-   <span data-ttu-id="7e6a8-105">Recupera il nome del listener e il CLSID dell'oggetto del gestore di protocollo ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-105">Retrieves the name of the listener and the CLSID of your protocol manager object ([**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) from the registry.</span></span> <span data-ttu-id="7e6a8-106">Per ulteriori informazioni, vedere [la pagina relativa alla registrazione di gestione protocolli](registering-the-custom-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="7e6a8-106">For more information, see [Registering the Protocol Manager](registering-the-custom-protocol.md).</span></span>
-   <span data-ttu-id="7e6a8-107">Chiama [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) per inizializzare Gestione protocolli.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-107">Calls [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) to initialize the protocol manager.</span></span>
-   <span data-ttu-id="7e6a8-108">Crea un oggetto di gestione protocollo usando il CLSID.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-108">Creates a protocol manager object using the CLSID.</span></span> <span data-ttu-id="7e6a8-109">Anche se sono presenti più listener registrati per lo stesso provider di protocollo, il servizio crea solo un oggetto di gestione protocolli.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-109">Even if there are multiple listeners registered for the same protocol provider, the service only creates one protocol manager object.</span></span>
-   <span data-ttu-id="7e6a8-110">Chiama [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) per indicare all'oggetto di gestione protocollo di creare un oggetto listener [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) e restituirlo al servizio.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-110">Calls [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) to instruct the protocol manager object to create an [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) listener object and return it to the service.</span></span> <span data-ttu-id="7e6a8-111">L'oggetto di gestione protocolli deve aggiungere un riferimento all'oggetto listener prima di restituirlo al servizio.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-111">The protocol manager object must add a reference to the listener object before returning it to the service.</span></span> <span data-ttu-id="7e6a8-112">Il servizio rilascerà l'oggetto quando il servizio viene arrestato o il listener viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-112">The service will release the object when the service stops or the listener is deleted.</span></span>
-   <span data-ttu-id="7e6a8-113">Chiama [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) sull'oggetto listener in modo che il listener possa iniziare ad ascoltare le connessioni in ingresso.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-113">Calls [**StartListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) on the listener object so that the listener can start listening for incoming connections.</span></span>
-   <span data-ttu-id="7e6a8-114">Chiama [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) per arrestare l'attesa dell'oggetto listener.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-114">Calls [**StopListen**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) to stop the listener object from listening.</span></span>
-   <span data-ttu-id="7e6a8-115">Chiama [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) per annullare l'inizializzazione di gestione protocolli.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-115">Calls [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) to uninitialize the protocol manager.</span></span>

<span data-ttu-id="7e6a8-116">Il listener crea un oggetto [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) quando un client tenta di connettersi.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-116">The listener creates an [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) object when a client tries to connect.</span></span> <span data-ttu-id="7e6a8-117">L'oggetto listener chiama [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) per notificare al servizio Servizi Desktop remoto che un nuovo client sta tentando di connettersi o riconnettersi e passa l'oggetto **IWRdsProtocolConnection** nella chiamata.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-117">The listener object calls [**OnConnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) to notify the Remote Desktop Services service that a new client is trying to connect or reconnect, and passes the **IWRdsProtocolConnection** object in that call.</span></span> <span data-ttu-id="7e6a8-118">Il servizio Servizi Desktop remoto restituirà a sua volta un oggetto [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) nella chiamata, in modo che il protocollo possa comunicare con il servizio Servizi Desktop remoto in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-118">The Remote Desktop Services service will in turn return an [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) object in that call so that the protocol can communicate with the Remote Desktop Services service as needed.</span></span> <span data-ttu-id="7e6a8-119">Il servizio aggiunge un riferimento all'oggetto callback prima della restituzione e il protocollo deve rilasciare tale riferimento alla chiusura della connessione.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-119">The service adds a reference to the callback object before returning, and the protocol must release that reference when the connection closes.</span></span>

<span data-ttu-id="7e6a8-120">Nella figura seguente viene illustrata l'interazione tra i vari oggetti durante l'avvio.</span><span class="sxs-lookup"><span data-stu-id="7e6a8-120">The following illustration shows the interaction between the various objects during startup.</span></span>

![sequenza di avvio RCM](images/protocol-startsequence.png)

## <a name="related-topics"></a><span data-ttu-id="7e6a8-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e6a8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e6a8-123">Sequenza di chiamate al metodo</span><span class="sxs-lookup"><span data-stu-id="7e6a8-123">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="7e6a8-124">Sequenza di connessione</span><span class="sxs-lookup"><span data-stu-id="7e6a8-124">Connection Sequence</span></span>](connection-sequence.md)
</dt> </dl>

 

 





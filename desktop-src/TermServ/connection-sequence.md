---
title: Sequenza di connessione
description: Illustrazione che mostra le chiamate al metodo effettuate tra il servizio Servizi Desktop remoto e il protocollo durante la sequenza di connessione del client.
ms.assetid: 60e56093-c457-43bc-b152-15c5acbfb016
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fe18d1a3b305a99fb0aaa35c51696f66de5c09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396678"
---
# <a name="connection-sequence"></a><span data-ttu-id="17542-103">Sequenza di connessione</span><span class="sxs-lookup"><span data-stu-id="17542-103">Connection Sequence</span></span>

<span data-ttu-id="17542-104">Nella figura seguente sono illustrate le chiamate al metodo effettuate tra il servizio Servizi Desktop remoto e il protocollo durante la sequenza di connessione del client.</span><span class="sxs-lookup"><span data-stu-id="17542-104">The following illustration shows the method calls made between the Remote Desktop Services service and your protocol during the client connection sequence.</span></span> <span data-ttu-id="17542-105">Le azioni illustrate di seguito seguono la [sequenza di avvio](start-sequence.md).</span><span class="sxs-lookup"><span data-stu-id="17542-105">The actions shown here follow the [Start Sequence](start-sequence.md).</span></span> <span data-ttu-id="17542-106">L'interazione tra il servizio e l'oggetto [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) rappresenta l'handshake delle licenze per il client.</span><span class="sxs-lookup"><span data-stu-id="17542-106">The interaction between the service and the [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection) object represents the licensing handshake for the client.</span></span>

![sequenza di connessione client](images/protocol-connectionsequence.png)

## <a name="related-topics"></a><span data-ttu-id="17542-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="17542-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17542-109">Sequenza di chiamate al metodo</span><span class="sxs-lookup"><span data-stu-id="17542-109">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="17542-110">Riconnetti sequenza</span><span class="sxs-lookup"><span data-stu-id="17542-110">Reconnect Sequence</span></span>](reconnect-sequence.md)
</dt> <dt>

[<span data-ttu-id="17542-111">Sequenza di avvio</span><span class="sxs-lookup"><span data-stu-id="17542-111">Start Sequence</span></span>](start-sequence.md)
</dt> </dl>

 

 





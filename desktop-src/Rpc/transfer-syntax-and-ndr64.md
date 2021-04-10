---
title: Sintassi transfer e NDR64
description: Il protocollo di collegamento NDR, noto anche come sintassi di trasferimento, consente alle chiamate RPC di attraversare la rete.
ms.assetid: 30b3843a-172c-4d08-beed-c68bcb68daaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dfec9bc1569ef9a42d0bc844c3b098736f714ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046781"
---
# <a name="transfer-syntax-and-ndr64"></a><span data-ttu-id="571b7-103">Sintassi transfer e NDR64</span><span class="sxs-lookup"><span data-stu-id="571b7-103">Transfer Syntax and NDR64</span></span>

<span data-ttu-id="571b7-104">Il protocollo di collegamento NDR, noto anche come sintassi di trasferimento, consente alle chiamate RPC di attraversare la rete.</span><span class="sxs-lookup"><span data-stu-id="571b7-104">The NDR wire protocol, also referred to as transfer syntax, enables RPC calls to traverse the network.</span></span> <span data-ttu-id="571b7-105">Il protocollo wire definisce la rappresentazione in transito di una chiamata RPC, ad esempio l'ordine in cui i membri dati vengono sottoposti a marshalling, l'allineamento dei dati in transito, informazioni aggiuntive incluse con i dati e altri problemi.</span><span class="sxs-lookup"><span data-stu-id="571b7-105">The wire protocol defines the wire representation of an RPC call, such as the order in which data members are marshaled, alignment of data on the wire, additional information included with the data, and other issues.</span></span> <span data-ttu-id="571b7-106">Il protocollo NDR64 è un'estensione della sintassi di trasferimento NDR basato su 32 bit, creata appositamente per consentire agli sviluppatori di utilizzare sistemi a 64 bit per ottenere prestazioni ottimizzate.</span><span class="sxs-lookup"><span data-stu-id="571b7-106">The NDR64 protocol is an extension to the 32-bit based NDR transfer syntax, created specifically to enable developers targeting 64-bit systems to achieve optimized performance.</span></span>

<span data-ttu-id="571b7-107">Le differenze tra il formato wire NDR e il formato wire NDR64 sono le diverse dimensioni dei puntatori in un ambiente a 64 bit, oltre ad altri problemi.</span><span class="sxs-lookup"><span data-stu-id="571b7-107">The differences between the NDR wire format and the NDR64 wire format addresses the different size of pointers in a 64-bit environment, as well as other issues.</span></span> <span data-ttu-id="571b7-108">Il meccanismo di NDR64 è gestito da RPC.</span><span class="sxs-lookup"><span data-stu-id="571b7-108">The mechanics of NDR64 is handled by RPC.</span></span> <span data-ttu-id="571b7-109">Gli sviluppatori devono usare solo l'opzione della riga di comando per **tutti** i [**protocolli**](/windows/desktop/Midl/-protocol)MIDL per ottenere i vantaggi di NDR64 su piattaforme a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="571b7-109">Developers need only use the /[**protocol**](/windows/desktop/Midl/-protocol)**all** MIDL command line switch to obtain the benefits of NDR64 on 64-bit platforms.</span></span> <span data-ttu-id="571b7-110">NDR64 è disponibile solo su piattaforme a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="571b7-110">NDR64 is available only on 64-bit platforms.</span></span>

 

 
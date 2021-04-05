---
title: Annullamento della ritrasmissione
description: Se non è presente alcuna risposta a una richiesta di comunicazione entro il periodo di timeout specificato per un'entità di destinazione e se vengono specificate ritrasmissioni per l'entità, l'implementazione di Microsoft WinSNMP ritrasmette la richiesta.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7346ee6e1e336b4f8fe56df3dce602fe65a0b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044708"
---
# <a name="canceling-retransmission"></a><span data-ttu-id="5ed49-103">Annullamento della ritrasmissione</span><span class="sxs-lookup"><span data-stu-id="5ed49-103">Canceling Retransmission</span></span>

<span data-ttu-id="5ed49-104">Se non è presente alcuna risposta a una richiesta di comunicazione entro il periodo di timeout specificato per un'entità di destinazione e se vengono specificate ritrasmissioni per l'entità, l'implementazione di Microsoft WinSNMP ritrasmette la richiesta.</span><span class="sxs-lookup"><span data-stu-id="5ed49-104">If there is no response to a communication request within the time-out period specified for a destination entity, and if retransmissions are specified for the entity, the Microsoft WinSNMP implementation retransmits the request.</span></span> <span data-ttu-id="5ed49-105">Una chiamata alla funzione [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) può annullare questo ciclo di ritrasmissione e rilasciare le strutture di dati interne associate alla richiesta del messaggio.</span><span class="sxs-lookup"><span data-stu-id="5ed49-105">A call to the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function can cancel this retransmission cycle and release internal data structures associated with the message request.</span></span>

<span data-ttu-id="5ed49-106">Si noti che è possibile che un'entità di destinazione riceva un messaggio SNMP che è stato annullato da una chiamata alla funzione [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) .</span><span class="sxs-lookup"><span data-stu-id="5ed49-106">Note that it is possible for a destination entity to receive an SNMP message that has been canceled by a call to the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function.</span></span> <span data-ttu-id="5ed49-107">È inoltre possibile che un'entità di destinazione possa rispondere a un messaggio SNMP annullato.</span><span class="sxs-lookup"><span data-stu-id="5ed49-107">It is also possible that a destination entity can respond to a canceled SNMP message.</span></span> <span data-ttu-id="5ed49-108">Questo perché l'accodamento delle transazioni avviene a più livelli.</span><span class="sxs-lookup"><span data-stu-id="5ed49-108">This is because transaction queuing occurs at multiple levels.</span></span> <span data-ttu-id="5ed49-109">Tuttavia, dopo che un messaggio è stato annullato da una chiamata a [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), l'implementazione di Microsoft WinSNMP non ritrasmette il messaggio, invierà una risposta PDU o invierà una notifica di timeout all'applicazione per quel messaggio.</span><span class="sxs-lookup"><span data-stu-id="5ed49-109">However, once a message has been canceled by a call to [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg), the Microsoft WinSNMP implementation will not retransmit the message, submit a response PDU, or send a time-out notification to the application for that message.</span></span>

 

 





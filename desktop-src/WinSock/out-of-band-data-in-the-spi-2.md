---
description: I provider di servizi che supportano l'astrazione dei dati fuori banda (OOB) per i socket di tipo flusso devono rispettare la semantica in questa sezione.
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: Dati fuori banda in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9808fa301073bcbb06be23a9487c2a1fa4f14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049479"
---
# <a name="out-of-band-data-in-the-spi"></a><span data-ttu-id="f9168-103">Dati fuori banda in SPI</span><span class="sxs-lookup"><span data-stu-id="f9168-103">Out-of-Band Data in the SPI</span></span>

<span data-ttu-id="f9168-104">I provider di servizi che supportano l'astrazione dei dati fuori banda (OOB) per i socket di tipo flusso devono rispettare la semantica in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="f9168-104">The service providers which support the out-of-band data (OOB) abstraction for the stream-style sockets must adhere to the semantics in this section.</span></span> <span data-ttu-id="f9168-105">Viene descritta la gestione dei dati di OOB in modo indipendente dal protocollo.</span><span class="sxs-lookup"><span data-stu-id="f9168-105">We will describe OOB data handling in a protocol-independent manner.</span></span> <span data-ttu-id="f9168-106">Per una descrizione dei dati di OOB implementati con i dati urgenti nei provider di servizi TCP/IP, vedere gli [allegati di Winsock](winsock-annexes.md) .</span><span class="sxs-lookup"><span data-stu-id="f9168-106">Please refer to the [Winsock Annexes](winsock-annexes.md) for a discussion of OOB data implemented using urgent data in TCP/IP service providers.</span></span> <span data-ttu-id="f9168-107">Nell'esempio seguente l'uso di [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) si applica anche a [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f9168-107">In the following, the use of [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) also applies to [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).</span></span>

 

 

---
description: Prima che un Socket possa essere usato per configurare una connessione o ricevere una richiesta di connessione, deve essere associato a un indirizzo locale.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Associazione a un indirizzo locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa022d17a8862e6092c52b18edd1539f2d95ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307044"
---
# <a name="binding-to-a-local-address"></a><span data-ttu-id="7c38d-103">Associazione a un indirizzo locale</span><span class="sxs-lookup"><span data-stu-id="7c38d-103">Binding to a Local Address</span></span>

<span data-ttu-id="7c38d-104">Prima che un Socket possa essere usato per configurare una connessione o ricevere una richiesta di connessione, deve essere associato a un indirizzo locale.</span><span class="sxs-lookup"><span data-stu-id="7c38d-104">Before a socket can be used to set up a connection or receive a connection request, it needs to be bound to a local address.</span></span> <span data-ttu-id="7c38d-105">Questa operazione può essere eseguita in modo esplicito chiamando [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))oppure in modo implicito da [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) se il socket non è associato quando viene chiamata questa funzione.</span><span class="sxs-lookup"><span data-stu-id="7c38d-105">This could be done explicitly by calling [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)), or implicitly by [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) if the socket is unbound when this function is called.</span></span>

 

 

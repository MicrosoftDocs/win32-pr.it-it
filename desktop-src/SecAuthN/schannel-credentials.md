---
description: I protocolli Schannel richiedono credenziali per autenticare i server e, facoltativamente, i client.
ms.assetid: 8295b1bd-6ae1-4f7e-926d-a9da7ec6a524
title: Credenziali Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91556a7e3bfca67aa386f0264e78ae67052f02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967388"
---
# <a name="schannel-credentials"></a><span data-ttu-id="e6e2d-103">Credenziali Schannel</span><span class="sxs-lookup"><span data-stu-id="e6e2d-103">Schannel Credentials</span></span>

<span data-ttu-id="e6e2d-104">I protocolli Schannel richiedono credenziali per autenticare i server e, facoltativamente, i client.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-104">Schannel protocols require credentials to authenticate servers and optionally, clients.</span></span> <span data-ttu-id="e6e2d-105">L'autenticazione server, in cui il server fornisce la prova dell'identità al client, è richiesta dai [*protocolli di sicurezza*](../secgloss/s-gly.md)Schannel.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-105">Server authentication, where the server provides proof of its identity to the client, is required by the Schannel [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="e6e2d-106">L'autenticazione client può essere richiesta dal server in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-106">Client authentication may be requested by the server at any time.</span></span>

<span data-ttu-id="e6e2d-107">Le credenziali Schannel sono certificati [*X. 509*](../secgloss/x-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e6e2d-107">Schannel credentials are [*X.509*](../secgloss/x-gly.md) certificates.</span></span> <span data-ttu-id="e6e2d-108">Le informazioni sulle chiavi [*pubbliche*](../secgloss/p-gly.md) e [*private*](../secgloss/p-gly.md) dei certificati vengono usate per autenticare il server e, facoltativamente, il client.</span><span class="sxs-lookup"><span data-stu-id="e6e2d-108">[*Public*](../secgloss/p-gly.md) and [*private key*](../secgloss/p-gly.md) information from certificates is used to authenticate the server and optionally, the client.</span></span> <span data-ttu-id="e6e2d-109">Queste chiavi vengono usate anche per fornire l' [*integrità*](../secgloss/i-gly.md) dei messaggi, mentre client e server scambiano le informazioni necessarie per generare e scambiare le [*chiavi della sessione*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e6e2d-109">These keys are also used to provide message [*integrity*](../secgloss/i-gly.md) while client and server exchange the information required to generate and exchange [*session keys*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="e6e2d-110">Per informazioni sulla programmazione, vedere [ottenere le credenziali Schannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="e6e2d-110">For programming information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

 

 

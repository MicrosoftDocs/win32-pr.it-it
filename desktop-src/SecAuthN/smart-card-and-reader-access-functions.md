---
description: Connettersi e comunicare con una smart card specifica.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Funzioni di accesso con smart card e lettore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7202b2d6165b49bfe80e55f15c4d69cb4a6909a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316232"
---
# <a name="smart-card-and-reader-access-functions"></a><span data-ttu-id="cc5a2-103">Funzioni di accesso con smart card e lettore</span><span class="sxs-lookup"><span data-stu-id="cc5a2-103">Smart Card and Reader Access Functions</span></span>

<span data-ttu-id="cc5a2-104">Le funzioni seguenti si connettono e comunicano con una [*Smart Card*](../secgloss/s-gly.md)specifica.</span><span class="sxs-lookup"><span data-stu-id="cc5a2-104">The following functions connect to and communicate with a specific [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="cc5a2-105">Le operazioni di i/O nella scheda utilizzano un buffer per l'invio o la ricezione di dati e una struttura contenente informazioni sul controllo del protocollo.</span><span class="sxs-lookup"><span data-stu-id="cc5a2-105">I/O operations to the card use a buffer for sending or receiving data and a structure that contains protocol control information.</span></span> <span data-ttu-id="cc5a2-106">La struttura delle informazioni di controllo del protocollo inizia sempre con una struttura di [**\_ \_ richiesta**](scard-io-request.md) di i/o spaventata.</span><span class="sxs-lookup"><span data-stu-id="cc5a2-106">The protocol control information structure always begins with an [**SCARD\_IO\_REQUEST**](scard-io-request.md) structure.</span></span>



| <span data-ttu-id="cc5a2-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="cc5a2-107">Topic</span></span>                                                  | <span data-ttu-id="cc5a2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc5a2-108">Description</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc5a2-109">**SCardConnect**</span><span class="sxs-lookup"><span data-stu-id="cc5a2-109">**SCardConnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | <span data-ttu-id="cc5a2-110">Connettersi a una scheda.</span><span class="sxs-lookup"><span data-stu-id="cc5a2-110">Connect to a card.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="cc5a2-111">**SCardReconnect**</span><span class="sxs-lookup"><span data-stu-id="cc5a2-111">**SCardReconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | <span data-ttu-id="cc5a2-112">Ristabilire una connessione.</span><span class="sxs-lookup"><span data-stu-id="cc5a2-112">Reestablish a connection.</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="cc5a2-113">**SCardDisconnect**</span><span class="sxs-lookup"><span data-stu-id="cc5a2-113">**SCardDisconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | <span data-ttu-id="cc5a2-114">Terminare una connessione.</span><span class="sxs-lookup"><span data-stu-id="cc5a2-114">Terminate a connection.</span></span>                                                                                                                                                                                                                    |
| [<span data-ttu-id="cc5a2-115">**SCardBeginTransaction**</span><span class="sxs-lookup"><span data-stu-id="cc5a2-115">**SCardBeginTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | <span data-ttu-id="cc5a2-116">Avviare una [*transazione*](../secgloss/t-gly.md), impedendo ad altre applicazioni di accedere a una scheda.</span><span class="sxs-lookup"><span data-stu-id="cc5a2-116">Start a [*transaction*](../secgloss/t-gly.md), blocking other applications from accessing a card.</span></span>                                                                                            |
| [<span data-ttu-id="cc5a2-117">**SCardEndTransaction**</span><span class="sxs-lookup"><span data-stu-id="cc5a2-117">**SCardEndTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | <span data-ttu-id="cc5a2-118">Terminare una transazione, consentendo ad altre applicazioni di accedere a una scheda.</span><span class="sxs-lookup"><span data-stu-id="cc5a2-118">End a transaction, allowing other applications to access a card.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="cc5a2-119">**SCardStatus**</span><span class="sxs-lookup"><span data-stu-id="cc5a2-119">**SCardStatus**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | <span data-ttu-id="cc5a2-120">Consente di specificare lo stato corrente del lettore.</span><span class="sxs-lookup"><span data-stu-id="cc5a2-120">Provide the current status of the reader.</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="cc5a2-121">**SCardTransmit**</span><span class="sxs-lookup"><span data-stu-id="cc5a2-121">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | <span data-ttu-id="cc5a2-122">Richiede il servizio e riceve i dati da una scheda usando [*T = 0*](../secgloss/t-gly.md), [*T = 1*](../secgloss/t-gly.md)e i protocolli non elaborati.</span><span class="sxs-lookup"><span data-stu-id="cc5a2-122">Requests service and receives data back from a card using [*T=0*](../secgloss/t-gly.md), [*T=1*](../secgloss/t-gly.md), and raw protocols.</span></span> |



 

 

 

---
title: Pubblicazione in un oggetto computer
description: In genere, i servizi basati su host creano convergenza nell'oggetto computer per il computer host. I servizi basati su host sono strettamente legati a un singolo computer host.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fe382001910f3b78b4461c622e94b14c54fb59
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872266"
---
# <a name="publishing-under-a-computer-object"></a><span data-ttu-id="081a1-104">Pubblicazione in un oggetto computer</span><span class="sxs-lookup"><span data-stu-id="081a1-104">Publishing Under a Computer Object</span></span>

<span data-ttu-id="081a1-105">In genere, i servizi basati su host creano convergenza nell'oggetto computer per il computer host.</span><span class="sxs-lookup"><span data-stu-id="081a1-105">Typically, host-based services create SCPs under the computer object for the host computer.</span></span> <span data-ttu-id="081a1-106">I servizi basati su host sono strettamente legati a un singolo computer host.</span><span class="sxs-lookup"><span data-stu-id="081a1-106">Host-based services are services closely tied to a single host computer.</span></span>

<span data-ttu-id="081a1-107">**Per creare convergenza in un oggetto computer**</span><span class="sxs-lookup"><span data-stu-id="081a1-107">**To create SCPs under a computer object**</span></span>

1.  <span data-ttu-id="081a1-108">Chiamare la funzione [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) per ottenere il nome distinto (DN) nella directory dell'oggetto computer per il computer locale.</span><span class="sxs-lookup"><span data-stu-id="081a1-108">Call the [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) function to get the distinguished name (DN) in the directory of the computer object for the local computer.</span></span>
2.  <span data-ttu-id="081a1-109">Usare tale DN per eseguire l'associazione all'oggetto computer e creare SCP.</span><span class="sxs-lookup"><span data-stu-id="081a1-109">Use that DN to bind to the computer object and create the SCP.</span></span>

<span data-ttu-id="081a1-110">Per ulteriori informazioni e un esempio di codice, vedere [modalità di individuazione e utilizzo di un punto di connessione del servizio](how-clients-find-and-use-a-service-connection-point.md)da parte dei client.</span><span class="sxs-lookup"><span data-stu-id="081a1-110">For more information and a code example, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="081a1-111">Tenere presente che nella directory solo i computer membri del dominio dispongono di oggetti computer validi.</span><span class="sxs-lookup"><span data-stu-id="081a1-111">Be aware that only domain-member computers have valid computer objects in the directory.</span></span>

<span data-ttu-id="081a1-112">Per ottenere il nome DNS o NetBIOS del computer locale, chiamare la funzione [**presunto GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .</span><span class="sxs-lookup"><span data-stu-id="081a1-112">To get the DNS or NetBIOS name of the local computer, call the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function.</span></span>

 

 
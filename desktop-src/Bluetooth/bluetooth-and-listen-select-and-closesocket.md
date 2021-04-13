---
title: Bluetooth e ascolto, selezione e chiamata closesocket
description: Bluetooth usa le funzioni Listen, Select e chiamata closesocket senza alcuna modifica dalla programmazione standard di Windows Sockets.
ms.assetid: b64440de-bc63-4e3b-bfd9-5cf783f36c23
keywords:
- Bluetooth
- chiamata closesocket
- ascolto
- Proprietà
- Bluetooth e ascolto
- Bluetooth e ascolto, selezionare
- Bluetooth e ascolto, selezione e chiamata closesocket
- ascolto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e442cfc0593ab5be297902487c7c3ccdf056b4e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473502"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a><span data-ttu-id="709fb-111">Bluetooth e ascolto, selezione e chiamata closesocket</span><span class="sxs-lookup"><span data-stu-id="709fb-111">Bluetooth and listen, select, and closesocket</span></span>

<span data-ttu-id="709fb-112">Bluetooth usa le funzioni [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**SELECT**](/windows/desktop/api/winsock2/nf-winsock2-select)e [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) senza alcuna modifica dalla programmazione standard di Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="709fb-112">Bluetooth uses the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select), and [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) functions without any modification from standard Windows Sockets programming.</span></span>

<span data-ttu-id="709fb-113">Come per i socket di Windows, la funzione [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) libera le risorse associate al socket.</span><span class="sxs-lookup"><span data-stu-id="709fb-113">As with Windows Sockets, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function frees resources associated with the socket.</span></span>

<span data-ttu-id="709fb-114">Quando si chiama la funzione [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) , è consigliabile usare un valore basso per il parametro *backlog* (in genere da 2 a 4), perché vengono accettate solo alcune connessioni client.</span><span class="sxs-lookup"><span data-stu-id="709fb-114">When calling the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) function, it is strongly recommended that a low value is used for the *backlog* parameter (typically 2 to 4), since only a few client connections are accepted.</span></span> <span data-ttu-id="709fb-115">In questo modo si riducono le risorse di sistema allocate per l'utilizzo da parte del socket di ascolto.</span><span class="sxs-lookup"><span data-stu-id="709fb-115">This reduces the system resources that are allocated for use by the listening socket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="709fb-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="709fb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="709fb-117">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="709fb-117">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="709fb-118">**chiamata closesocket**</span><span class="sxs-lookup"><span data-stu-id="709fb-118">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="709fb-119">**ascoltare**</span><span class="sxs-lookup"><span data-stu-id="709fb-119">**listen**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[<span data-ttu-id="709fb-120">**Selezionare**</span><span class="sxs-lookup"><span data-stu-id="709fb-120">**select**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 
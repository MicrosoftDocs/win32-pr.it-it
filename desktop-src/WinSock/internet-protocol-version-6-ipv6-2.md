---
description: È importante assicurarsi che le nuove applicazioni Winsock e le applicazioni esistenti siano completamente compatibili con IPv6.
ms.assetid: 48aa6be8-e8a2-48a5-aa71-3e5ed7032551
title: Protocollo IP versione 6 (IPv6)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9647b70571b0bc81cbea508cf2e3bb55662efdf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879209"
---
# <a name="internet-protocol-version-6-ipv6"></a><span data-ttu-id="3b3d7-103">Protocollo IP versione 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="3b3d7-103">Internet Protocol Version 6 (IPv6)</span></span>

<span data-ttu-id="3b3d7-104">È importante assicurarsi che le nuove applicazioni Winsock e le applicazioni esistenti siano completamente compatibili con IPv6.</span><span class="sxs-lookup"><span data-stu-id="3b3d7-104">It is important to ensure that new Winsock applications as well as existing applications are fully compatible with IPv6.</span></span> <span data-ttu-id="3b3d7-105">La disponibilità dello spazio degli indirizzi IPv4 per le nuove allocazioni di indirizzi IPv4 è stata esaurita per Asia e Pacifico in 2011.</span><span class="sxs-lookup"><span data-stu-id="3b3d7-105">The availability of the IPv4 address space for new IPv4 address allocations was exhausted for Asia and the Pacific in 2011.</span></span> <span data-ttu-id="3b3d7-106">Si prevede che altre parti del mondo vengano esaurite tra qualche anno.</span><span class="sxs-lookup"><span data-stu-id="3b3d7-106">Other parts of the world are expected to be exhausted in a few years.</span></span>

<span data-ttu-id="3b3d7-107">È disponibile una percentuale crescente di nuovi siti Web e servizi usando indirizzi IPv6.</span><span class="sxs-lookup"><span data-stu-id="3b3d7-107">A growing percentage of new websites and services are available using IPv6 addresses.</span></span> <span data-ttu-id="3b3d7-108">Molti utenti Internet nei mercati emergenti dipendono da IPv6 per l'accesso a Internet.</span><span class="sxs-lookup"><span data-stu-id="3b3d7-108">Many Internet users in emerging markets are dependent on IPv6 for Internet access.</span></span>

<span data-ttu-id="3b3d7-109">Microsoft ha un impegno lungo per supportare IPv6.</span><span class="sxs-lookup"><span data-stu-id="3b3d7-109">Microsoft has a long commitment of supporting IPv6.</span></span> <span data-ttu-id="3b3d7-110">Il supporto IPv6 completo è disponibile in Windows XP con Service Pack 1 (SP1) e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3b3d7-110">Full IPv6 support is provided on Windows XP with Service Pack 1 (SP1) and later.</span></span>

<span data-ttu-id="3b3d7-111">In questo documento vengono fornite informazioni sul supporto Winsock per IPv6:</span><span class="sxs-lookup"><span data-stu-id="3b3d7-111">This document provides information about the Winsock support for IPv6:</span></span>

-   [<span data-ttu-id="3b3d7-112">Utilizzo di IPv6</span><span class="sxs-lookup"><span data-stu-id="3b3d7-112">Using IPv6</span></span>](using-ipv6-2.md)
-   [<span data-ttu-id="3b3d7-113">Utilizzo di Internet Explorer per accedere ai siti Web IPv6</span><span class="sxs-lookup"><span data-stu-id="3b3d7-113">Using Internet Explorer to Access IPv6 Websites</span></span>](using-internet-explorer-to-access-ipv6-web-sites-2.md)
-   [<span data-ttu-id="3b3d7-114">Configurazioni consigliate per IPv6</span><span class="sxs-lookup"><span data-stu-id="3b3d7-114">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
-   [<span data-ttu-id="3b3d7-115">Argomenti aggiuntivi su IPv6</span><span class="sxs-lookup"><span data-stu-id="3b3d7-115">Additional IPv6 Topics</span></span>](additional-topics-2.md)

<span data-ttu-id="3b3d7-116">Per ulteriori informazioni sull'aggiunta di funzionalità IPv6 alle applicazioni Windows Sockets, vedere la [Guida a IPv6 per le applicazioni Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md).</span><span class="sxs-lookup"><span data-stu-id="3b3d7-116">For additional information on adding IPv6 capability to your Windows Sockets applications, see [IPv6 Guide for Windows Sockets Applications](ipv6-guide-for-windows-sockets-applications-2.md).</span></span>

<span data-ttu-id="3b3d7-117">Un'introduzione al protocollo IPv6, oltre a panoramiche sulle tecnologie di distribuzione e di transizione IPv6, è disponibile su TechNet in [Microsoft Internet Protocol versione 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="3b3d7-117">An introduction to the IPv6 protocol along with overviews on deployment and IPv6 transitioning technologies is available on Technet at [Microsoft Internet Protocol Version 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b3d7-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b3d7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b3d7-119">Guida a IPv6 per le applicazioni Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="3b3d7-119">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="3b3d7-120">Supporto IPv6</span><span class="sxs-lookup"><span data-stu-id="3b3d7-120">IPv6 Support</span></span>](ipv6-support-2.md)
</dt> <dt>

[<span data-ttu-id="3b3d7-121">Anteprima della tecnologia IPv6 per Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3b3d7-121">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

<span data-ttu-id="3b3d7-122">[Microsoft Internet Protocol versione 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="3b3d7-122">[Microsoft Internet Protocol Version 6 (IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd379473(v=ws.10))</span></span>
</dt> </dl>

 

 

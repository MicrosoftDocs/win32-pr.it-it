---
title: Funzioni IKE/AuthIP
description: Funzioni (WFP) utilizzate per interagire con i moduli di chiave \ 8212; protocollo IKE (IKE), protocollo IKE v2 (IKEv2) e Authenticated Internet Protocol (AuthIP).
ms.assetid: df36b6cc-a304-4426-8f16-1bf92fd721e1
keywords:
- Funzioni protocollo IKE API della piattaforma filtro Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cce5d3e2393bb1a83ebf816375f537318bb4b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331028"
---
# <a name="ikeauthip-functions"></a><span data-ttu-id="92b16-104">Funzioni IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="92b16-104">IKE/AuthIP Functions</span></span>

<span data-ttu-id="92b16-105">Le funzioni Windows Filtering Platform (WFP) utilizzate per interagire con i moduli di chiave (protocollo IKE (IKE), protocollo IKE v2 (IKEv2) e Authenticated Internet Protocol (AuthIP) sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="92b16-105">The Windows Filtering Platform (WFP) functions used to interact with keying modules—Internet Key Exchange (IKE), Internet Key Exchange v2 (IKEv2), and Authenticated Internet Protocol (AuthIP)—are as follows.</span></span>

-   <span data-ttu-id="92b16-106">IkeextGetStatistics:</span><span class="sxs-lookup"><span data-stu-id="92b16-106">IkeextGetStatistics:</span></span>
    -   <span data-ttu-id="92b16-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="92b16-107">[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0) (Windows Vista)</span></span>
    -   <span data-ttu-id="92b16-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="92b16-108">[**IkeextGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="92b16-109">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="92b16-109">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)
-   [<span data-ttu-id="92b16-110">**IkeextSaDbGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="92b16-110">**IkeextSaDbGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbgetsecurityinfo0)
-   [<span data-ttu-id="92b16-111">**IkeextSaDbSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="92b16-111">**IkeextSaDbSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadbsetsecurityinfo0)
-   [<span data-ttu-id="92b16-112">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="92b16-112">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)
-   [<span data-ttu-id="92b16-113">**IkeextSaDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="92b16-113">**IkeextSaDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadestroyenumhandle0)
-   <span data-ttu-id="92b16-114">IkeextSaEnum:</span><span class="sxs-lookup"><span data-stu-id="92b16-114">IkeextSaEnum:</span></span>
    -   <span data-ttu-id="92b16-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="92b16-115">[**IkeextSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="92b16-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="92b16-116">[**IkeextSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum1) (Windows 7)</span></span>
    -   <span data-ttu-id="92b16-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="92b16-117">[**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2) (Windows 8)</span></span>
-   <span data-ttu-id="92b16-118">IkeextSaGetById:</span><span class="sxs-lookup"><span data-stu-id="92b16-118">IkeextSaGetById:</span></span>
    -   <span data-ttu-id="92b16-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="92b16-119">[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0) (Windows Vista)</span></span>
    -   <span data-ttu-id="92b16-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="92b16-120">[**IkeextSaGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid1) (Windows 7)</span></span>
    -   <span data-ttu-id="92b16-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8)</span><span class="sxs-lookup"><span data-stu-id="92b16-121">[**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2) (Windows 8)</span></span>

 

 





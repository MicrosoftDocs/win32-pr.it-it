---
description: L'helper IP fornisce informazioni sulla configurazione di rete del computer locale.
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: Recupero di informazioni sulla configurazione di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a6860b329ba7c69575be1dfeaaa2e19c57558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968397"
---
# <a name="retrieving-information-about-network-configuration"></a><span data-ttu-id="b7109-103">Recupero di informazioni sulla configurazione di rete</span><span class="sxs-lookup"><span data-stu-id="b7109-103">Retrieving Information About Network Configuration</span></span>

<span data-ttu-id="b7109-104">L'helper IP fornisce informazioni sulla configurazione di rete del computer locale.</span><span class="sxs-lookup"><span data-stu-id="b7109-104">IP Helper provides information about the network configuration of the local computer.</span></span> <span data-ttu-id="b7109-105">Per recuperare le informazioni di configurazione generali, utilizzare la funzione [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) .</span><span class="sxs-lookup"><span data-stu-id="b7109-105">To retrieve general configuration information, use the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function.</span></span> <span data-ttu-id="b7109-106">Questa funzione restituisce informazioni non specifiche di una particolare scheda o interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b7109-106">This function returns information that is not specific to a particular adapter or interface.</span></span> <span data-ttu-id="b7109-107">Ad esempio, **GetNetworkParams** restituisce un elenco dei server DNS utilizzati dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="b7109-107">For example, **GetNetworkParams** returns a list of the DNS servers that are used by the local computer.</span></span>

-   <span data-ttu-id="b7109-108">Per esempi di codice che coinvolgono [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , vedere [recupero di informazioni con GetNetworkParams](retrieving-information-using-getnetworkparams.md).</span><span class="sxs-lookup"><span data-stu-id="b7109-108">For code samples involving [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) see [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md).</span></span>

 

 




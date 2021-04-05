---
description: Il provider di visualizzazione è un'istanza e un provider di metodi che creano nuove classi basate su istanze di altre classi.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Visualizza provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883506"
---
# <a name="view-provider"></a><span data-ttu-id="d59cc-103">Visualizza provider</span><span class="sxs-lookup"><span data-stu-id="d59cc-103">View Provider</span></span>

<span data-ttu-id="d59cc-104">Il provider di visualizzazione è un'istanza e un provider di metodi che creano nuove classi basate su istanze di altre classi.</span><span class="sxs-lookup"><span data-stu-id="d59cc-104">The View provider is an instance and method provider that creates new classes based on instances of other classes.</span></span> <span data-ttu-id="d59cc-105">È possibile utilizzare il provider di visualizzazione per eseguire proprietà da classi di origine diverse, spazi dei nomi diversi o computer diversi e combinare le proprietà come una singola classe.</span><span class="sxs-lookup"><span data-stu-id="d59cc-105">You can use the View provider to take properties from different source classes, different namespaces, or different computers and combine the properties as a single class.</span></span>

<span data-ttu-id="d59cc-106">Come provider di istanze e di metodi, il provider di visualizzazione supporta l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard e i metodi [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) seguenti:</span><span class="sxs-lookup"><span data-stu-id="d59cc-106">As an instance and method provider, the View provider supports the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface and the following [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="d59cc-107">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="d59cc-107">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="d59cc-108">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="d59cc-108">**ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="d59cc-109">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="d59cc-109">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="d59cc-110">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="d59cc-110">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="d59cc-111">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="d59cc-111">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="d59cc-112">Per ulteriori informazioni sui qualificatori utilizzati per definire le classi del provider di visualizzazione, vedere [qualificatori specifici del provider di visualizzazione](qualifiers-specific-to-the-view-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d59cc-112">For more information about the qualifiers use to define View provider classes, see [Qualifiers Specific to the View Provider](qualifiers-specific-to-the-view-provider.md).</span></span>

<span data-ttu-id="d59cc-113">Per ulteriori informazioni sulle visualizzazioni, vedere [collegamento di classi](linking-classes-together.md).</span><span class="sxs-lookup"><span data-stu-id="d59cc-113">For more information about views, see [Linking Classes Together](linking-classes-together.md).</span></span>

<span data-ttu-id="d59cc-114">Sulle piattaforme a 64 bit sono disponibili due versioni del provider di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d59cc-114">Two versions of the View provider are available on 64-bit platforms.</span></span> <span data-ttu-id="d59cc-115">Per altre informazioni, vedere [ottenere e fornire dati in un computer a 64 bit](getting-and-providing-data-on-a-64-bit-computer.md).</span><span class="sxs-lookup"><span data-stu-id="d59cc-115">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="d59cc-116">Il provider di visualizzazione viene implementato in ViewProv.dll.</span><span class="sxs-lookup"><span data-stu-id="d59cc-116">The View provider is implemented in ViewProv.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d59cc-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d59cc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d59cc-118">Provider WMI</span><span class="sxs-lookup"><span data-stu-id="d59cc-118">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 




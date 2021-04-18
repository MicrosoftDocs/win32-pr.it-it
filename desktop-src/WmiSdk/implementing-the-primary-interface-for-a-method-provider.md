---
description: "Un provider di metodi deve implementare IWbemServices come interfaccia primaria. Tuttavia, un provider di metodi puri richiede solo l'implementazione del metodo IWbemServices:: ExecMethodAsync."
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Implementazione dell'interfaccia primaria per un provider di metodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 196f87a6520d92bf18362be88f8cc40e5133dabe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315216"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a><span data-ttu-id="38bec-104">Implementazione dell'interfaccia primaria per un provider di metodi</span><span class="sxs-lookup"><span data-stu-id="38bec-104">Implementing the Primary Interface for a Method Provider</span></span>

<span data-ttu-id="38bec-105">Un provider di metodi deve implementare [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) come interfaccia primaria.</span><span class="sxs-lookup"><span data-stu-id="38bec-105">A method provider should implement [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface.</span></span> <span data-ttu-id="38bec-106">Tuttavia, un provider di metodi puri richiede solo l'implementazione del metodo [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) .</span><span class="sxs-lookup"><span data-stu-id="38bec-106">However, a pure method provider requires only that you implement the [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) method.</span></span>

<span data-ttu-id="38bec-107">Poiché gli altri provider utilizzano [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), l'interfaccia contiene molti metodi irrilevanti per un provider di metodi puri.</span><span class="sxs-lookup"><span data-stu-id="38bec-107">Because other providers use [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), the interface contains many methods that are irrelevant to a pure method provider.</span></span> <span data-ttu-id="38bec-108">Il provider di metodi puri deve fornire un'implementazione stub che restituisce \_ il \_ provider WBEM E \_ non \_ idoneo per tutti gli altri metodi **IWbemServices** oltre a [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span><span class="sxs-lookup"><span data-stu-id="38bec-108">Your pure method provider should supply a stub implementation that returns WBEM\_E\_PROVIDER\_NOT\_CAPABLE for all of other **IWbemServices** methods besides [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span></span> <span data-ttu-id="38bec-109">Tuttavia, molti provider di metodi vengono utilizzati anche come provider di classi o di istanza.</span><span class="sxs-lookup"><span data-stu-id="38bec-109">However, many method providers also serve as instance or class providers.</span></span> <span data-ttu-id="38bec-110">Il metodo combinato e i provider di istanze devono supportare più metodi **IWbemServices** .</span><span class="sxs-lookup"><span data-stu-id="38bec-110">Combination method and instance providers must support more of the **IWbemServices** methods.</span></span>

 

 




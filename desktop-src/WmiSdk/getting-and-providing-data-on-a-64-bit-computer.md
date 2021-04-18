---
description: Le applicazioni e gli script client che accedono a provider WMI 32 bit standard continuano a funzionare normalmente in caso di esecuzione in un sistema operativo a 64 bit.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Ottenere e fornire dati in un computer a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d8ff5430a7c47b652bfbcca05d2f53ba857d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555815"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a><span data-ttu-id="fe032-103">Ottenere e fornire dati in un computer a 64 bit</span><span class="sxs-lookup"><span data-stu-id="fe032-103">Getting and Providing Data on a 64-bit Computer</span></span>

<span data-ttu-id="fe032-104">Le applicazioni e gli script client che accedono a provider WMI 32 bit standard continuano a funzionare normalmente in caso di esecuzione in un sistema operativo a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="fe032-104">Client applications and scripts that access standard WMI 32-bit providers continue to operate normally when running on a 64-bit operating system.</span></span> <span data-ttu-id="fe032-105">Solo due provider preinstallati, il [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) e il [provider di visualizzazione](view-provider.md), hanno versioni a 64 bit che vengono eseguite side-by-side con le versioni a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="fe032-105">Only two preinstalled providers, the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) and the [View provider](view-provider.md), have 64-bit versions which run side-by-side with the 32-bit versions.</span></span> <span data-ttu-id="fe032-106">Tuttavia, un'applicazione a 32 bit che richiede istanze di Windows Driver Model WDM (32 bit) riceve le istanze della classe WDM a 64 bit predefinite in un sistema operativo a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="fe032-106">However, a 32-bit application that requests 32-bit Windows Driver Model (WDM) instances receives the default 64-bit WDM class instances on a 64-bit operating system.</span></span>

## <a name="accessing-default-and-nondefault-provider-data"></a><span data-ttu-id="fe032-107">Accesso ai dati del provider predefiniti e non predefiniti</span><span class="sxs-lookup"><span data-stu-id="fe032-107">Accessing Default and Nondefault Provider Data</span></span>

<span data-ttu-id="fe032-108">In genere, i writer del provider non includono le versioni a 32 bit e a 64 bit di un provider nello stesso sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fe032-108">Generally, provider writers do not include both 32-bit and 64-bit versions of a provider in the same operating system.</span></span> <span data-ttu-id="fe032-109">Se non esiste alcun provider a 64 bit, un provider a 32 bit può continuare a eseguire le funzionalità di WOW64.</span><span class="sxs-lookup"><span data-stu-id="fe032-109">If no 64-bit provider exists, a 32-bit provider can continue to run through the facilities of WOW64.</span></span> <span data-ttu-id="fe032-110">Un provider a 64 bit può fornire dati in modo analogo a un'applicazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="fe032-110">A 64-bit provider can likewise supply data to a 32-bit application.</span></span> <span data-ttu-id="fe032-111">Per ulteriori informazioni, vedere [la pagina relativa alla fornitura di dati WMI in una piattaforma a 64 bit](providing-wmi-data-on-a-64-bit-platform.md).</span><span class="sxs-lookup"><span data-stu-id="fe032-111">For more information, see [Providing WMI Data on a 64-bit Platform](providing-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="fe032-112">Se esistono due versioni, le applicazioni e gli script client possono usare i parametri di contesto disponibili nell' [API com](com-api-for-wmi.md) e l' [API di scripting](scripting-api-for-wmi.md) per connettersi in modo esplicito a un provider WMI non predefinito specifico, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="fe032-112">If two versions exist, client applications and scripts can use the context parameters available in the [COM API](com-api-for-wmi.md) and the [Scripting API](scripting-api-for-wmi.md) to connect explicitly to a specific nondefault WMI provider, if it is available.</span></span> <span data-ttu-id="fe032-113">Per ulteriori informazioni, vedere la pagina relativa alla [richiesta di dati WMI in una piattaforma a 64 bit](requesting-wmi-data-on-a-64-bit-platform.md).</span><span class="sxs-lookup"><span data-stu-id="fe032-113">For more information, see [Requesting WMI Data on a 64-bit Platform](requesting-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="fe032-114">Il diagramma seguente illustra le connessioni predefinite e non predefinite, usando il registro di sistema come esempio per cui due provider possono esistere side-by-side in una piattaforma a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="fe032-114">The following diagram shows the default and nondefault connections, using the registry as an example for which two providers can exist side-by-side on a 64-bit platform.</span></span>

![connessioni predefinite e non predefinite in una piattaforma a 64 bit](images/32-64bit-registry.png)

## <a name="related-topics"></a><span data-ttu-id="fe032-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe032-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe032-117">Richiesta di dati WMI in una piattaforma a 64 bit</span><span class="sxs-lookup"><span data-stu-id="fe032-117">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="fe032-118">Fornire dati WMI in una piattaforma a 64 bit</span><span class="sxs-lookup"><span data-stu-id="fe032-118">Providing WMI Data on a 64-bit Platform</span></span>](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 

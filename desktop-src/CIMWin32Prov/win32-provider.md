---
description: Microsoft&\# 160; Il provider Win32 recupera e aggiorna i dati rilevanti per i sistemi Windows&\# 8212, dati quali le impostazioni correnti delle variabili di ambiente e gli attributi di un disco logico.
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Provider Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dfb29b6f80ed833de0f4185070d46770c6cd2f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747903"
---
# <a name="win32-provider"></a><span data-ttu-id="a0ec3-103">Provider Win32</span><span class="sxs-lookup"><span data-stu-id="a0ec3-103">Win32 Provider</span></span>

<span data-ttu-id="a0ec3-104">Il provider Microsoft Win32 recupera e aggiorna i dati rilevanti per i sistemi Windows: dati quali le impostazioni correnti delle variabili di ambiente e gli attributi di un disco logico.</span><span class="sxs-lookup"><span data-stu-id="a0ec3-104">The Microsoft Win32 provider retrieves and updates data relevant to Windows systems—data such as the current settings of environment variables and the attributes of a logical disk.</span></span> <span data-ttu-id="a0ec3-105">Con il provider Win32, le applicazioni di gestione possono utilizzare WMI per accedere facilmente a questi dati.</span><span class="sxs-lookup"><span data-stu-id="a0ec3-105">With the Win32 provider, management applications can use WMI to easily access this data.</span></span> <span data-ttu-id="a0ec3-106">Il provider Win32 recupera le informazioni effettuando chiamate di funzioni Windows ed eseguendo query sul Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a0ec3-106">The Win32 provider retrieves its information by making Windows function calls and querying the system registry.</span></span>

<span data-ttu-id="a0ec3-107">Il provider Win32 definisce le classi utilizzate per descrivere l'hardware o il software disponibile nei sistemi Windows e le relazioni tra di essi.</span><span class="sxs-lookup"><span data-stu-id="a0ec3-107">The Win32 provider defines the classes used to describe hardware or software available on Windows systems and the relationships between them.</span></span>

<span data-ttu-id="a0ec3-108">Come provider di istanze e di metodi, il provider Win32 implementa l'interfaccia [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) standard, oltre ai metodi [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0ec3-108">As an instance and method provider, the Win32 provider implements the standard [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface as well as the following [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="a0ec3-109">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="a0ec3-109">**CreateInstanceEnumAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="a0ec3-110">**DeleteInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="a0ec3-110">**DeleteInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [<span data-ttu-id="a0ec3-111">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="a0ec3-111">**ExecMethodAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="a0ec3-112">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="a0ec3-112">**ExecQueryAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="a0ec3-113">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="a0ec3-113">**GetObjectAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="a0ec3-114">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="a0ec3-114">**PutInstanceAsync**</span></span>](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="a0ec3-115">Nella tabella seguente sono elencate le categorie di classi del provider Win32.</span><span class="sxs-lookup"><span data-stu-id="a0ec3-115">The following table lists the Win32 provider class categories.</span></span>



| <span data-ttu-id="a0ec3-116">Classi</span><span class="sxs-lookup"><span data-stu-id="a0ec3-116">Classes</span></span>                                                                             | <span data-ttu-id="a0ec3-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0ec3-117">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="a0ec3-118">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="a0ec3-118">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)<br/> | <span data-ttu-id="a0ec3-119">Oggetti correlati all'hardware.</span><span class="sxs-lookup"><span data-stu-id="a0ec3-119">Hardware-related objects.</span></span><br/>                                      |
| [<span data-ttu-id="a0ec3-120">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a0ec3-120">Operating System Classes</span></span>](operating-system-classes.md)<br/>                 | <span data-ttu-id="a0ec3-121">Oggetti correlati al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a0ec3-121">Operating system related objects.</span></span><br/>                              |
| [<span data-ttu-id="a0ec3-122">Classi del contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="a0ec3-122">Performance Counter Classes</span></span>](performance-counter-classes.md)<br/>           | <span data-ttu-id="a0ec3-123">Dati sulle prestazioni non elaborati e calcolati dai contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a0ec3-123">Raw and calculated performance data from performance counters.</span></span><br/> |
| [<span data-ttu-id="a0ec3-124">Classi di gestione del servizio WMI</span><span class="sxs-lookup"><span data-stu-id="a0ec3-124">WMI Service Management Classes</span></span>](wmi-service-management-classes.md)<br/>     | <span data-ttu-id="a0ec3-125">Gestione per WMI.</span><span class="sxs-lookup"><span data-stu-id="a0ec3-125">Management for WMI.</span></span><br/>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="a0ec3-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0ec3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0ec3-127">Provider WMI CIMWin32</span><span class="sxs-lookup"><span data-stu-id="a0ec3-127">CIMWin32 WMI Provider</span></span>](cimwin32-wmi-providers.md)
</dt> </dl>

 

 

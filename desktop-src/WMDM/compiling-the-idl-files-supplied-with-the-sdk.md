---
title: Compilazione dei file IDL forniti con l'SDK
description: Compilazione dei file IDL forniti con l'SDK
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Gestione dispositivi Windows Media, file IDL
- Gestione dispositivi, file IDL
- applicazioni desktop, file IDL
- provider di servizi, file IDL
- guida per programmatori,file IDL
- IDL (file)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e3d4ecd7f4f9df7b884cf70de3ba3ad62c7939
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444012"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a><span data-ttu-id="55e6c-109">Compilazione dei file IDL forniti con l'SDK</span><span class="sxs-lookup"><span data-stu-id="55e6c-109">Compiling the IDL Files Supplied with the SDK</span></span>

<span data-ttu-id="55e6c-110">Windows Media Device Manager SDK include sia i file di intestazione che i file IDL di origine per la maggior parte di questi file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="55e6c-110">The Windows Media Device Manager SDK includes both header files and the source IDL files for most of these header files.</span></span> <span data-ttu-id="55e6c-111">I file di intestazione si trovano nella cartella \\ inc nel percorso di installazione \\ dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="55e6c-111">The header files are located in the \\inc\\ folder in the SDK installation path.</span></span> <span data-ttu-id="55e6c-112">I file IDL si trovano nella \\ cartella \\ idl.</span><span class="sxs-lookup"><span data-stu-id="55e6c-112">The IDL files are located in the \\idl\\ folder.</span></span>

<span data-ttu-id="55e6c-113">Le intestazioni precompilate sono molto più semplici da usare e diversi file IDL vengono combinati in una singola intestazione fornita.</span><span class="sxs-lookup"><span data-stu-id="55e6c-113">The precompiled headers are much simpler to use, and several of the IDL files are combined into a single provided header.</span></span> <span data-ttu-id="55e6c-114">Tuttavia, se si decide di elaborare i propri file di intestazione dai file IDL forniti, questo argomento descrive quali file IDL creano i file di intestazione e descrive anche le dipendenze di ogni file IDL.</span><span class="sxs-lookup"><span data-stu-id="55e6c-114">However, if you decide to process your own header files from the provided IDL files, this topic describes which IDL files create which header files, and also describes the dependencies of each IDL file.</span></span>

<span data-ttu-id="55e6c-115">**File IDL e file di intestazione forniti equivalenti**</span><span class="sxs-lookup"><span data-stu-id="55e6c-115">**Equivalent IDL and Provided Header Files**</span></span>



| <span data-ttu-id="55e6c-116">**Idl**</span><span class="sxs-lookup"><span data-stu-id="55e6c-116">**IDL**</span></span>                                                                                            | <span data-ttu-id="55e6c-117">**Intestazione fornita equivalente**</span><span class="sxs-lookup"><span data-stu-id="55e6c-117">**Equivalent supplied header**</span></span>               | <span data-ttu-id="55e6c-118">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="55e6c-118">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55e6c-119">WMDM.idl</span><span class="sxs-lookup"><span data-stu-id="55e6c-119">WMDM.idl</span></span><br/> <span data-ttu-id="55e6c-120">WMSP.idl</span><span class="sxs-lookup"><span data-stu-id="55e6c-120">WMSP.idl</span></span><br/> <span data-ttu-id="55e6c-121">WMSCP.idl</span><span class="sxs-lookup"><span data-stu-id="55e6c-121">WMSCP.idl</span></span><br/> <span data-ttu-id="55e6c-122">icomponentauthenticate.idl</span><span class="sxs-lookup"><span data-stu-id="55e6c-122">icomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="55e6c-123">Mswmdm.h</span><span class="sxs-lookup"><span data-stu-id="55e6c-123">Mswmdm.h</span></span>                                     | <span data-ttu-id="55e6c-124">Tutti e quattro i file IDL sono inclusi in questa singola intestazione fornita.</span><span class="sxs-lookup"><span data-stu-id="55e6c-124">All four IDL files are included in this single provided header.</span></span><br/> <span data-ttu-id="55e6c-125">**WMDM.idl** definisce tutte le interfacce dell'applicazione e le strutture, le costanti e i codici di errore necessari.</span><span class="sxs-lookup"><span data-stu-id="55e6c-125">**WMDM.idl** Defines all the application interfaces and required structures, constants, and error codes.</span></span><br/> <span data-ttu-id="55e6c-126">**WMSP.idl** definisce tutte le interfacce del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="55e6c-126">**WMSP.idl** Defines all the service provider interfaces.</span></span><br/> <span data-ttu-id="55e6c-127">**WMSCP.idl** definisce tutte le interfacce, i valori GUID e le costanti richieste dai provider di contenuto sicuri.</span><span class="sxs-lookup"><span data-stu-id="55e6c-127">**WMSCP.idl** Defines all the interfaces, GUID values, and constants required by secure content providers.</span></span><br/> <span data-ttu-id="55e6c-128">**icomponentauthenticate.idl** Definisce [**l'interfaccia IComponentAuthenticate.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)</span><span class="sxs-lookup"><span data-stu-id="55e6c-128">**icomponentauthenticate.idl** Defines the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span><br/> |
| <span data-ttu-id="55e6c-129">Wmdmlog.idl</span><span class="sxs-lookup"><span data-stu-id="55e6c-129">Wmdmlog.idl</span></span>                                                                                        | <span data-ttu-id="55e6c-130">Wmdmlog.h</span><span class="sxs-lookup"><span data-stu-id="55e6c-130">Wmdmlog.h</span></span><br/> <span data-ttu-id="55e6c-131">wmdmlog \_ i.c</span><span class="sxs-lookup"><span data-stu-id="55e6c-131">wmdmlog\_i.c</span></span><br/> | <span data-ttu-id="55e6c-132">Definisce le interfacce di registrazione.</span><span class="sxs-lookup"><span data-stu-id="55e6c-132">Defines the logging interfaces.</span></span><br/> <span data-ttu-id="55e6c-133">Entrambi i file di intestazione forniti devono essere usati, anziché solo il file con estensione h, a causa di un problema con il file IDL.</span><span class="sxs-lookup"><span data-stu-id="55e6c-133">Both supplied header files must be used, rather than just the .h file, because of a problem with the IDL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="55e6c-134">WMDRMDeviceApp.idl</span><span class="sxs-lookup"><span data-stu-id="55e6c-134">WMDRMDeviceApp.idl</span></span>                                                                                 | <span data-ttu-id="55e6c-135">Wmdrmdeviceapp.h</span><span class="sxs-lookup"><span data-stu-id="55e6c-135">Wmdrmdeviceapp.h</span></span>                             | <span data-ttu-id="55e6c-136">Definisce le [**interfacce IWMDRMDeviceApp**](iwmdrmdeviceapp.md) e [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) usate dalle applicazioni che aggiornano DRM nei dispositivi o nei conteggi di riproduzione dei contatori nei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="55e6c-136">Defines the [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) and [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) interfaces used by applications that update DRM on devices or meter play counts on devices.</span></span>                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="55e6c-137">**Dipendenze IDL**</span><span class="sxs-lookup"><span data-stu-id="55e6c-137">**IDL Dependencies**</span></span>

<span data-ttu-id="55e6c-138">Molti dei file IDL forniti hanno dipendenze di compilazione.</span><span class="sxs-lookup"><span data-stu-id="55e6c-138">Several of the provided IDL files have build dependencies.</span></span> <span data-ttu-id="55e6c-139">Se si prevede di compilare i file IDL manualmente, è necessario elaborare queste dipendenze esterne nell'ordine illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="55e6c-139">If you plan to compile the IDL files yourself, you must process these external dependencies in the order shown in the following table.</span></span>



|   <span data-ttu-id="55e6c-140">Idl</span><span class="sxs-lookup"><span data-stu-id="55e6c-140">IDL</span></span>                      |   <span data-ttu-id="55e6c-141">Dipendenze</span><span class="sxs-lookup"><span data-stu-id="55e6c-141">Dependencies</span></span>                                                                   |
|----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="55e6c-142">icomponentauthenticate.idl</span><span class="sxs-lookup"><span data-stu-id="55e6c-142">icomponentauthenticate.idl</span></span> | <span data-ttu-id="55e6c-143">importare "oaidl.idl";</span><span class="sxs-lookup"><span data-stu-id="55e6c-143">import "oaidl.idl";</span></span><br/> <span data-ttu-id="55e6c-144">\#include "icomponentauthenticate.idl"</span><span class="sxs-lookup"><span data-stu-id="55e6c-144">\#include "icomponentauthenticate.idl"</span></span><br/> |
| <span data-ttu-id="55e6c-145">WMDM.idl</span><span class="sxs-lookup"><span data-stu-id="55e6c-145">WMDM.idl</span></span>                   | <span data-ttu-id="55e6c-146">Nessuna dipendenza esterna</span><span class="sxs-lookup"><span data-stu-id="55e6c-146">No external dependencies</span></span>                                                         |
| <span data-ttu-id="55e6c-147">WmdmLog.idl</span><span class="sxs-lookup"><span data-stu-id="55e6c-147">WmdmLog.idl</span></span>                | <span data-ttu-id="55e6c-148">Nessuna dipendenza esterna</span><span class="sxs-lookup"><span data-stu-id="55e6c-148">No external dependencies</span></span>                                                         |
| <span data-ttu-id="55e6c-149">WMDRMDeviceApp.idl</span><span class="sxs-lookup"><span data-stu-id="55e6c-149">WMDRMDeviceApp.idl</span></span>         | <span data-ttu-id="55e6c-150">Nessuna dipendenza esterna</span><span class="sxs-lookup"><span data-stu-id="55e6c-150">No external dependencies</span></span>                                                         |
| <span data-ttu-id="55e6c-151">WMSCP.idl</span><span class="sxs-lookup"><span data-stu-id="55e6c-151">WMSCP.idl</span></span>                  | <span data-ttu-id="55e6c-152">\#includere "WMDRMDeviceApp.idl"</span><span class="sxs-lookup"><span data-stu-id="55e6c-152">\#include "WMDRMDeviceApp.idl"</span></span><br/> <span data-ttu-id="55e6c-153">\#includere "WMSP.idl"</span><span class="sxs-lookup"><span data-stu-id="55e6c-153">\#include "WMSP.idl"</span></span><br/>        |
| <span data-ttu-id="55e6c-154">WMSP.idl</span><span class="sxs-lookup"><span data-stu-id="55e6c-154">WMSP.idl</span></span>                   | <span data-ttu-id="55e6c-155">\#includere "WMDM.idl"</span><span class="sxs-lookup"><span data-stu-id="55e6c-155">\#include "WMDM.idl"</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="55e6c-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="55e6c-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55e6c-157">**Attività comuni ad applicazioni e provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="55e6c-157">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 






---
title: Compilazione dei file IDL forniti con l'SDK
description: Compilazione dei file IDL forniti con l'SDK
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Windows Media Gestione dispositivi, file IDL
- Gestione dispositivi, file IDL
- applicazioni desktop, file IDL
- provider di servizi, file IDL
- Guida per programmatori, file IDL
- IDL (file)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e24eec21a481de4603392942b40013ec55086c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298505"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a><span data-ttu-id="067f7-109">Compilazione dei file IDL forniti con l'SDK</span><span class="sxs-lookup"><span data-stu-id="067f7-109">Compiling the IDL Files Supplied with the SDK</span></span>

<span data-ttu-id="067f7-110">Windows Media Gestione dispositivi SDK include sia i file di intestazione che i file IDL di origine per la maggior parte di questi file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="067f7-110">The Windows Media Device Manager SDK includes both header files and the source IDL files for most of these header files.</span></span> <span data-ttu-id="067f7-111">I file di intestazione si trovano nella \\ \\ cartella Inc nel percorso di installazione di SDK.</span><span class="sxs-lookup"><span data-stu-id="067f7-111">The header files are located in the \\inc\\ folder in the SDK installation path.</span></span> <span data-ttu-id="067f7-112">I file IDL si trovano nella \\ cartella IDL \\ .</span><span class="sxs-lookup"><span data-stu-id="067f7-112">The IDL files are located in the \\idl\\ folder.</span></span>

<span data-ttu-id="067f7-113">Le intestazioni precompilate sono molto più semplici da utilizzare e molti dei file IDL vengono combinati in un'unica intestazione fornita.</span><span class="sxs-lookup"><span data-stu-id="067f7-113">The precompiled headers are much simpler to use, and several of the IDL files are combined into a single provided header.</span></span> <span data-ttu-id="067f7-114">Tuttavia, se si decide di elaborare i file di intestazione dai file IDL forniti, in questo argomento vengono descritti i file IDL che consentono di creare i file di intestazione, oltre a descrivere le dipendenze di ogni file IDL.</span><span class="sxs-lookup"><span data-stu-id="067f7-114">However, if you decide to process your own header files from the provided IDL files, this topic describes which IDL files create which header files, and also describes the dependencies of each IDL file.</span></span>

<span data-ttu-id="067f7-115">**IDL equivalente e file di intestazione forniti**</span><span class="sxs-lookup"><span data-stu-id="067f7-115">**Equivalent IDL and Provided Header Files**</span></span>



| <span data-ttu-id="067f7-116">**IDL**</span><span class="sxs-lookup"><span data-stu-id="067f7-116">**IDL**</span></span>                                                                                            | <span data-ttu-id="067f7-117">**Intestazione fornita equivalente**</span><span class="sxs-lookup"><span data-stu-id="067f7-117">**Equivalent supplied header**</span></span>               | <span data-ttu-id="067f7-118">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="067f7-118">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="067f7-119">WMDM. idl</span><span class="sxs-lookup"><span data-stu-id="067f7-119">WMDM.idl</span></span><br/> <span data-ttu-id="067f7-120">WMSP. idl</span><span class="sxs-lookup"><span data-stu-id="067f7-120">WMSP.idl</span></span><br/> <span data-ttu-id="067f7-121">WMSCP. idl</span><span class="sxs-lookup"><span data-stu-id="067f7-121">WMSCP.idl</span></span><br/> <span data-ttu-id="067f7-122">IComponentAuthenticate. idl</span><span class="sxs-lookup"><span data-stu-id="067f7-122">icomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="067f7-123">Mswmdm. h</span><span class="sxs-lookup"><span data-stu-id="067f7-123">Mswmdm.h</span></span>                                     | <span data-ttu-id="067f7-124">In questa singola intestazione fornita sono inclusi tutti e quattro i file IDL.</span><span class="sxs-lookup"><span data-stu-id="067f7-124">All four IDL files are included in this single provided header.</span></span><br/> <span data-ttu-id="067f7-125">**WMDM. idl** definisce tutte le interfacce dell'applicazione e le strutture, le costanti e i codici di errore richiesti.</span><span class="sxs-lookup"><span data-stu-id="067f7-125">**WMDM.idl** Defines all the application interfaces and required structures, constants, and error codes.</span></span><br/> <span data-ttu-id="067f7-126">**WMSP. idl** definisce tutte le interfacce del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="067f7-126">**WMSP.idl** Defines all the service provider interfaces.</span></span><br/> <span data-ttu-id="067f7-127">**WMSCP. idl** definisce tutte le interfacce, i valori GUID e le costanti richiesti dai provider di contenuti protetti.</span><span class="sxs-lookup"><span data-stu-id="067f7-127">**WMSCP.idl** Defines all the interfaces, GUID values, and constants required by secure content providers.</span></span><br/> <span data-ttu-id="067f7-128">**IComponentAuthenticate. idl** definisce l'interfaccia [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="067f7-128">**icomponentauthenticate.idl** Defines the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span><br/> |
| <span data-ttu-id="067f7-129">Wmdmlog. idl</span><span class="sxs-lookup"><span data-stu-id="067f7-129">Wmdmlog.idl</span></span>                                                                                        | <span data-ttu-id="067f7-130">Wmdmlog. h</span><span class="sxs-lookup"><span data-stu-id="067f7-130">Wmdmlog.h</span></span><br/> <span data-ttu-id="067f7-131">wmdmlog \_ i. c</span><span class="sxs-lookup"><span data-stu-id="067f7-131">wmdmlog\_i.c</span></span><br/> | <span data-ttu-id="067f7-132">Definisce le interfacce di registrazione.</span><span class="sxs-lookup"><span data-stu-id="067f7-132">Defines the logging interfaces.</span></span><br/> <span data-ttu-id="067f7-133">È necessario utilizzare entrambi i file di intestazione specificati, anziché solo il file con estensione h, a causa di un problema con il file IDL.</span><span class="sxs-lookup"><span data-stu-id="067f7-133">Both supplied header files must be used, rather than just the .h file, because of a problem with the IDL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="067f7-134">WMDRMDeviceApp. idl</span><span class="sxs-lookup"><span data-stu-id="067f7-134">WMDRMDeviceApp.idl</span></span>                                                                                 | <span data-ttu-id="067f7-135">Wmdrmdeviceapp. h</span><span class="sxs-lookup"><span data-stu-id="067f7-135">Wmdrmdeviceapp.h</span></span>                             | <span data-ttu-id="067f7-136">Definisce le interfacce [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) e [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) usate dalle applicazioni che aggiornano i DRM nei dispositivi o i conteggi di riproduzione dei contatori nei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="067f7-136">Defines the [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) and [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) interfaces used by applications that update DRM on devices or meter play counts on devices.</span></span>                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="067f7-137">**Dipendenze IDL**</span><span class="sxs-lookup"><span data-stu-id="067f7-137">**IDL Dependencies**</span></span>

<span data-ttu-id="067f7-138">Molti dei file IDL forniti hanno dipendenze di compilazione.</span><span class="sxs-lookup"><span data-stu-id="067f7-138">Several of the provided IDL files have build dependencies.</span></span> <span data-ttu-id="067f7-139">Se si prevede di compilare manualmente i file IDL, è necessario elaborare le dipendenze esterne nell'ordine indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="067f7-139">If you plan to compile the IDL files yourself, you must process these external dependencies in the order shown in the following table.</span></span>



|                            |                                                                                  |
|----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="067f7-140">**IDL**</span><span class="sxs-lookup"><span data-stu-id="067f7-140">**IDL**</span></span>                    | <span data-ttu-id="067f7-141">**Dipendenze**</span><span class="sxs-lookup"><span data-stu-id="067f7-141">**Dependencies**</span></span>                                                                 |
| <span data-ttu-id="067f7-142">IComponentAuthenticate. idl</span><span class="sxs-lookup"><span data-stu-id="067f7-142">icomponentauthenticate.idl</span></span> | <span data-ttu-id="067f7-143">Importa "OAIDL. idl";</span><span class="sxs-lookup"><span data-stu-id="067f7-143">import "oaidl.idl";</span></span><br/> <span data-ttu-id="067f7-144">\#Includi "IComponentAuthenticate. idl"</span><span class="sxs-lookup"><span data-stu-id="067f7-144">\#include "icomponentauthenticate.idl"</span></span><br/> |
| <span data-ttu-id="067f7-145">WMDM. idl</span><span class="sxs-lookup"><span data-stu-id="067f7-145">WMDM.idl</span></span>                   | <span data-ttu-id="067f7-146">Nessuna dipendenza esterna</span><span class="sxs-lookup"><span data-stu-id="067f7-146">No external dependencies</span></span>                                                         |
| <span data-ttu-id="067f7-147">WmdmLog. idl</span><span class="sxs-lookup"><span data-stu-id="067f7-147">WmdmLog.idl</span></span>                | <span data-ttu-id="067f7-148">Nessuna dipendenza esterna</span><span class="sxs-lookup"><span data-stu-id="067f7-148">No external dependencies</span></span>                                                         |
| <span data-ttu-id="067f7-149">WMDRMDeviceApp. idl</span><span class="sxs-lookup"><span data-stu-id="067f7-149">WMDRMDeviceApp.idl</span></span>         | <span data-ttu-id="067f7-150">Nessuna dipendenza esterna</span><span class="sxs-lookup"><span data-stu-id="067f7-150">No external dependencies</span></span>                                                         |
| <span data-ttu-id="067f7-151">WMSCP. idl</span><span class="sxs-lookup"><span data-stu-id="067f7-151">WMSCP.idl</span></span>                  | <span data-ttu-id="067f7-152">\#Includi "WMDRMDeviceApp. idl"</span><span class="sxs-lookup"><span data-stu-id="067f7-152">\#include "WMDRMDeviceApp.idl"</span></span><br/> <span data-ttu-id="067f7-153">\#Includi "WMSP. idl"</span><span class="sxs-lookup"><span data-stu-id="067f7-153">\#include "WMSP.idl"</span></span><br/>        |
| <span data-ttu-id="067f7-154">WMSP. idl</span><span class="sxs-lookup"><span data-stu-id="067f7-154">WMSP.idl</span></span>                   | <span data-ttu-id="067f7-155">\#Includi "WMDM. idl"</span><span class="sxs-lookup"><span data-stu-id="067f7-155">\#include "WMDM.idl"</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="067f7-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="067f7-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="067f7-157">**Attività comuni per le applicazioni e i provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="067f7-157">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 






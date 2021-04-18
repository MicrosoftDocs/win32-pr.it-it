---
description: Compilazione di applicazioni DirectShow
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: Compilazione di applicazioni DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c6ab8a0731e93eece734abd4380b092414ff5f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303693"
---
# <a name="building-directshow-applications"></a><span data-ttu-id="2a789-103">Compilazione di applicazioni DirectShow</span><span class="sxs-lookup"><span data-stu-id="2a789-103">Building DirectShow Applications</span></span>

<span data-ttu-id="2a789-104">Questo argomento descrive le intestazioni e le librerie necessarie per compilare applicazioni DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2a789-104">This topic describes the headers and libraries needed to build DirectShow applications.</span></span>

<span data-ttu-id="2a789-105">Le intestazioni e le librerie DirectShow più recenti sono disponibili nell' [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx).</span><span class="sxs-lookup"><span data-stu-id="2a789-105">The latest DirectShow headers and libraries are available in the [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx).</span></span>

## <a name="header-files"></a><span data-ttu-id="2a789-106">File di intestazione</span><span class="sxs-lookup"><span data-stu-id="2a789-106">Header Files</span></span>

<span data-ttu-id="2a789-107">Tutte le applicazioni DirectShow utilizzano il file di intestazione illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2a789-107">All DirectShow applications use the header file shown in the following table.</span></span>



| <span data-ttu-id="2a789-108">File di intestazione</span><span class="sxs-lookup"><span data-stu-id="2a789-108">Header File</span></span> | <span data-ttu-id="2a789-109">Obbligatorio per</span><span class="sxs-lookup"><span data-stu-id="2a789-109">Required For</span></span>                 |
|-------------|------------------------------|
| <span data-ttu-id="2a789-110">Dshow. h</span><span class="sxs-lookup"><span data-stu-id="2a789-110">Dshow.h</span></span>     | <span data-ttu-id="2a789-111">Tutte le applicazioni DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2a789-111">All DirectShow applications.</span></span> |



 

<span data-ttu-id="2a789-112">Per alcune interfacce DirectShow sono necessari file di intestazione aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="2a789-112">Some DirectShow interfaces require additional header files.</span></span> <span data-ttu-id="2a789-113">Questi requisiti sono indicati nella Guida di riferimento all'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2a789-113">These requirements are noted in the interface reference.</span></span>

## <a name="library-files"></a><span data-ttu-id="2a789-114">File di libreria</span><span class="sxs-lookup"><span data-stu-id="2a789-114">Library Files</span></span>

<span data-ttu-id="2a789-115">DirectShow usa i file di libreria statici indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2a789-115">DirectShow uses the static library files shown in the following table.</span></span>



| <span data-ttu-id="2a789-116">File di libreria</span><span class="sxs-lookup"><span data-stu-id="2a789-116">Library File</span></span> | <span data-ttu-id="2a789-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a789-117">Description</span></span>                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a789-118">Strmiids. lib</span><span class="sxs-lookup"><span data-stu-id="2a789-118">Strmiids.lib</span></span> | <span data-ttu-id="2a789-119">Esporta gli identificatori di classe (CLSID) e gli identificatori di interfaccia (IID).</span><span class="sxs-lookup"><span data-stu-id="2a789-119">Exports class identifiers (CLSIDs) and interface identifiers (IIDs).</span></span>                                                           |
| <span data-ttu-id="2a789-120">Quartz. lib</span><span class="sxs-lookup"><span data-stu-id="2a789-120">Quartz.lib</span></span>   | <span data-ttu-id="2a789-121">Esporta la funzione [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) .</span><span class="sxs-lookup"><span data-stu-id="2a789-121">Exports the [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) function.</span></span> <span data-ttu-id="2a789-122">Se non si chiama questa funzione, questa libreria non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="2a789-122">If you do not call this function, this library is not required.</span></span> |



 

<span data-ttu-id="2a789-123">Utilizzare gli stessi file con estensione LIB per le compilazioni di debug e di rilascio.</span><span class="sxs-lookup"><span data-stu-id="2a789-123">Use the same .lib files for debug and release builds.</span></span>

## <a name="filter-base-classes"></a><span data-ttu-id="2a789-124">Filtrare le classi base</span><span class="sxs-lookup"><span data-stu-id="2a789-124">Filter Base Classes</span></span>

<span data-ttu-id="2a789-125">Il Windows SDK fornisce un set di classi C++ consigliate Se si sta scrivendo un filtro DirectShow personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2a789-125">The Windows SDK provides a set of C++ classes that are recommended if you are writing a custom DirectShow filter.</span></span> <span data-ttu-id="2a789-126">Queste classi vengono fornite come codice di esempio, che è possibile compilare in una libreria statica.</span><span class="sxs-lookup"><span data-stu-id="2a789-126">These classes are provided as sample code, which you can compile to a static library.</span></span> <span data-ttu-id="2a789-127">Per altre informazioni, vedere [classi base di DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="2a789-127">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="redistributable-dlls"></a><span data-ttu-id="2a789-128">DLL ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="2a789-128">Redistributable DLLs</span></span>

<span data-ttu-id="2a789-129">Per le applicazioni DirectShow scritte per Windows XP con Service Pack 2 (SP2) e versioni successive non è necessario ridistribuire le dll DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2a789-129">DirectShow applications written for Windows XP with Service Pack 2 (SP2) and later do not need to redistribute any DirectShow DLLs.</span></span>

<span data-ttu-id="2a789-130">Per Windows XP con Service Pack 1 (SP1) e versioni precedenti, le dll DirectShow ridistribuibili sono disponibili in Microsoft DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="2a789-130">For Windows XP with Service Pack 1 (SP1) and earlier, redistributable DirectShow DLLs are available from the Microsoft DirectX SDK.</span></span> <span data-ttu-id="2a789-131">La versione più recente di queste dll è la versione 9.0 c.</span><span class="sxs-lookup"><span data-stu-id="2a789-131">The latest version of these DLLs is version 9.0c.</span></span> <span data-ttu-id="2a789-132">Non è pianificato alcun ulteriore sviluppo di queste DLL ridistribuibili.</span><span class="sxs-lookup"><span data-stu-id="2a789-132">No further development of these redistributable DLLs is planned.</span></span> <span data-ttu-id="2a789-133">Windows XP con Service Pack 2 (SP2) contiene le dll della versione 9.0 c.</span><span class="sxs-lookup"><span data-stu-id="2a789-133">Windows XP with Service Pack 2 (SP2) contains the version 9.0c DLLs.</span></span>

<span data-ttu-id="2a789-134">I pacchetti Redstributable contengono le DLL seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a789-134">The redstributable packages contain the following DLLs:</span></span>

-   <span data-ttu-id="2a789-135">dxnt.cab</span><span class="sxs-lookup"><span data-stu-id="2a789-135">dxnt.cab</span></span>
    -   <span data-ttu-id="2a789-136">amstream.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-136">amstream.dll</span></span>
    -   <span data-ttu-id="2a789-137">devenum.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-137">devenum.dll</span></span>
    -   <span data-ttu-id="2a789-138">encapi.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-138">encapi.dll</span></span>
    -   <span data-ttu-id="2a789-139">ks.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-139">ks.sys</span></span>
    -   <span data-ttu-id="2a789-140">ksolay.ax</span><span class="sxs-lookup"><span data-stu-id="2a789-140">ksolay.ax</span></span>
    -   <span data-ttu-id="2a789-141">ksproxy.ax</span><span class="sxs-lookup"><span data-stu-id="2a789-141">ksproxy.ax</span></span>
    -   <span data-ttu-id="2a789-142">ksuser.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-142">ksuser.dll</span></span>
    -   <span data-ttu-id="2a789-143">l3codecx.ax</span><span class="sxs-lookup"><span data-stu-id="2a789-143">l3codecx.ax</span></span>
    -   <span data-ttu-id="2a789-144">mciqtz32.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-144">mciqtz32.dll</span></span>
    -   <span data-ttu-id="2a789-145">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="2a789-145">mpg2splt.ax</span></span>
    -   <span data-ttu-id="2a789-146">msdmo.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-146">msdmo.dll</span></span>
    -   <span data-ttu-id="2a789-147">mskssrv.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-147">mskssrv.sys</span></span>
    -   <span data-ttu-id="2a789-148">mspclock.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-148">mspclock.sys</span></span>
    -   <span data-ttu-id="2a789-149">mspqm.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-149">mspqm.sys</span></span>
    -   <span data-ttu-id="2a789-150">mstee.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-150">mstee.sys</span></span>
    -   <span data-ttu-id="2a789-151">mswebdvd.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-151">mswebdvd.dll</span></span>
    -   <span data-ttu-id="2a789-152">qasf.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-152">qasf.dll</span></span>
    -   <span data-ttu-id="2a789-153">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-153">qcap.dll</span></span>
    -   <span data-ttu-id="2a789-154">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-154">qdv.dll</span></span>
    -   <span data-ttu-id="2a789-155">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-155">qdvd.dll</span></span>
    -   <span data-ttu-id="2a789-156">qedit.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-156">qedit.dll</span></span>
    -   <span data-ttu-id="2a789-157">qedwipes.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-157">qedwipes.dll</span></span>
    -   <span data-ttu-id="2a789-158">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-158">quartz.dll</span></span>
    -   <span data-ttu-id="2a789-159">stream.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-159">stream.sys</span></span>
    -   <span data-ttu-id="2a789-160">swenum.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-160">swenum.sys</span></span>
-   <span data-ttu-id="2a789-161">bda.cab</span><span class="sxs-lookup"><span data-stu-id="2a789-161">bda.cab</span></span>
    -   <span data-ttu-id="2a789-162">bdaplgin.ax</span><span class="sxs-lookup"><span data-stu-id="2a789-162">bdaplgin.ax</span></span>
    -   <span data-ttu-id="2a789-163">bdasup.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-163">bdasup.sys</span></span>
    -   <span data-ttu-id="2a789-164">ccdecode.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-164">ccdecode.sys</span></span>
    -   <span data-ttu-id="2a789-165">ipsink.ax</span><span class="sxs-lookup"><span data-stu-id="2a789-165">ipsink.ax</span></span>
    -   <span data-ttu-id="2a789-166">kstvtune.ax</span><span class="sxs-lookup"><span data-stu-id="2a789-166">kstvtune.ax</span></span>
    -   <span data-ttu-id="2a789-167">kswdmcap.ax</span><span class="sxs-lookup"><span data-stu-id="2a789-167">kswdmcap.ax</span></span>
    -   <span data-ttu-id="2a789-168">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="2a789-168">ksxbar.ax</span></span>
    -   <span data-ttu-id="2a789-169">mpe.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-169">mpe.sys</span></span>
    -   <span data-ttu-id="2a789-170">mpeg2data.ax</span><span class="sxs-lookup"><span data-stu-id="2a789-170">mpeg2data.ax</span></span>
    -   <span data-ttu-id="2a789-171">msdv.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-171">msdv.sys</span></span>
    -   <span data-ttu-id="2a789-172">msdvbnp.ax</span><span class="sxs-lookup"><span data-stu-id="2a789-172">msdvbnp.ax</span></span>
    -   <span data-ttu-id="2a789-173">msvidctl.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-173">msvidctl.dll</span></span>
    -   <span data-ttu-id="2a789-174">msyuv.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-174">msyuv.dll</span></span>
    -   <span data-ttu-id="2a789-175">nabtsfec.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-175">nabtsfec.sys</span></span>
    -   <span data-ttu-id="2a789-176">ndisip.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-176">ndisip.sys</span></span>
    -   <span data-ttu-id="2a789-177">psisdecd.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-177">psisdecd.dll</span></span>
    -   <span data-ttu-id="2a789-178">psisrndr.ax</span><span class="sxs-lookup"><span data-stu-id="2a789-178">psisrndr.ax</span></span>
    -   <span data-ttu-id="2a789-179">slip.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-179">slip.sys</span></span>
    -   <span data-ttu-id="2a789-180">streamip.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-180">streamip.sys</span></span>
    -   <span data-ttu-id="2a789-181">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="2a789-181">vbisurf.ax</span></span>
    -   <span data-ttu-id="2a789-182">wstcodec.sys</span><span class="sxs-lookup"><span data-stu-id="2a789-182">wstcodec.sys</span></span>
    -   <span data-ttu-id="2a789-183">wstdecod.dll</span><span class="sxs-lookup"><span data-stu-id="2a789-183">wstdecod.dll</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a789-184">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a789-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a789-185">Creazione di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="2a789-185">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> </dl>

 

 

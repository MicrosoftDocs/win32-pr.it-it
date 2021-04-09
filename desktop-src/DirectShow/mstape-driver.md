---
description: Driver MSTape
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Driver MSTape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f37e22c26866fca9519219d358e9733fb56151
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875982"
---
# <a name="mstape-driver"></a><span data-ttu-id="a34b5-103">Driver MSTape</span><span class="sxs-lookup"><span data-stu-id="a34b5-103">MSTape Driver</span></span>

<span data-ttu-id="a34b5-104">Questo argomento si applica a Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="a34b5-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="a34b5-105">Il driver MSTape supporta i dispositivi con videocamera D-VHS e MPEG.</span><span class="sxs-lookup"><span data-stu-id="a34b5-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="a34b5-106">Viene esposto alle applicazioni come filtro di [acquisizione video WDM](wdm-video-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="a34b5-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="a34b5-107">La relativa funzionalità è simile a quella di [Msdv](msdv-driver.md), il driver della videocamera DV:</span><span class="sxs-lookup"><span data-stu-id="a34b5-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="a34b5-108">Viene visualizzato nelle categorie di filtri "video Capture Sources" (CLSID \_ VideoInputDeviceCategory) e "WDM Streaming rendering Devices" ( \_ KSCATEGORY \_ Render).</span><span class="sxs-lookup"><span data-stu-id="a34b5-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="a34b5-109">Un'applicazione può creare un'istanza del filtro usando l'interfaccia [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .</span><span class="sxs-lookup"><span data-stu-id="a34b5-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="a34b5-110">Include un pin di output per l'acquisizione e il trasporto dal dispositivo e un pin di input per il trasporto al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a34b5-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="a34b5-111">È possibile connettere un solo pin alla volta.</span><span class="sxs-lookup"><span data-stu-id="a34b5-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="a34b5-112">**Tipi di supporto**</span><span class="sxs-lookup"><span data-stu-id="a34b5-112">**Media Types**</span></span>

<span data-ttu-id="a34b5-113">Il pin di input supporta un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="a34b5-113">The input pin supports one media type.</span></span>



|              |                                                            |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="a34b5-114">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="a34b5-114">Major Type</span></span>   | <span data-ttu-id="a34b5-115">\_Flusso MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="a34b5-115">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="a34b5-116">Subtype</span><span class="sxs-lookup"><span data-stu-id="a34b5-116">Subtype</span></span>      | <span data-ttu-id="a34b5-117">\_ \_ Stride trasporto MPEG2 \_ MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="a34b5-117">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="a34b5-118">Dimensione del campione</span><span class="sxs-lookup"><span data-stu-id="a34b5-118">Sample Size</span></span>  | <span data-ttu-id="a34b5-119">192 x 256</span><span class="sxs-lookup"><span data-stu-id="a34b5-119">192 x 256</span></span>                                                  |
| <span data-ttu-id="a34b5-120">Formato blocco</span><span class="sxs-lookup"><span data-stu-id="a34b5-120">Format Block</span></span> | [<span data-ttu-id="a34b5-121">**\_Stride trasporto \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="a34b5-121">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="a34b5-122">Il pin di output supporta due tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="a34b5-122">The output pin supports two media types.</span></span>



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="a34b5-123">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="a34b5-123">Major Type</span></span>   | <span data-ttu-id="a34b5-124">\_Flusso MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="a34b5-124">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="a34b5-125">Subtype</span><span class="sxs-lookup"><span data-stu-id="a34b5-125">Subtype</span></span>      | <span data-ttu-id="a34b5-126">\_ \_ Stride trasporto MPEG2 \_ MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="a34b5-126">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="a34b5-127">Dimensione del campione</span><span class="sxs-lookup"><span data-stu-id="a34b5-127">Sample Size</span></span>  | <span data-ttu-id="a34b5-128">192 x 256</span><span class="sxs-lookup"><span data-stu-id="a34b5-128">192 x 256</span></span>                              |
| <span data-ttu-id="a34b5-129">Formato blocco</span><span class="sxs-lookup"><span data-stu-id="a34b5-129">Format Block</span></span> | <span data-ttu-id="a34b5-130">\_Stride trasporto \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="a34b5-130">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="a34b5-131">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="a34b5-131">Major Type</span></span>   | <span data-ttu-id="a34b5-132">\_Flusso MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="a34b5-132">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="a34b5-133">Subtype</span><span class="sxs-lookup"><span data-stu-id="a34b5-133">Subtype</span></span>      | <span data-ttu-id="a34b5-134">\_ \_ Stride trasporto MPEG2 \_ MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="a34b5-134">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="a34b5-135">Dimensione del campione</span><span class="sxs-lookup"><span data-stu-id="a34b5-135">Sample Size</span></span>  | <span data-ttu-id="a34b5-136">188 x 256</span><span class="sxs-lookup"><span data-stu-id="a34b5-136">188 x 256</span></span>                              |
| <span data-ttu-id="a34b5-137">Formato blocco</span><span class="sxs-lookup"><span data-stu-id="a34b5-137">Format Block</span></span> | <span data-ttu-id="a34b5-138">**NULL**</span><span class="sxs-lookup"><span data-stu-id="a34b5-138">**NULL**</span></span>                               |



 

<span data-ttu-id="a34b5-139">**Informazioni sul dispositivo**</span><span class="sxs-lookup"><span data-stu-id="a34b5-139">**Device Information**</span></span>

<span data-ttu-id="a34b5-140">Il driver legge dinamicamente le informazioni dalla ROM di configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a34b5-140">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="a34b5-141">L'applicazione può recuperare queste informazioni associando il moniker del dispositivo a un contenitore delle proprietà e chiamando il metodo **IPropertyBag:: Read** .</span><span class="sxs-lookup"><span data-stu-id="a34b5-141">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="a34b5-142">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a34b5-142">Property</span></span>            | <span data-ttu-id="a34b5-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a34b5-143">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="a34b5-144">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a34b5-144">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="a34b5-145">UniqueID \_ basso</span><span class="sxs-lookup"><span data-stu-id="a34b5-145">UniqueID\_Low</span></span>       | <span data-ttu-id="a34b5-146">ID univoco del dispositivo ( **DWORD** basso).</span><span class="sxs-lookup"><span data-stu-id="a34b5-146">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="a34b5-147">**Long** (VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="a34b5-147">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="a34b5-148">UniqueID \_ alto</span><span class="sxs-lookup"><span data-stu-id="a34b5-148">UniqueID\_High</span></span>      | <span data-ttu-id="a34b5-149">ID univoco del dispositivo ( **DWORD** alto)</span><span class="sxs-lookup"><span data-stu-id="a34b5-149">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="a34b5-150">**long**</span><span class="sxs-lookup"><span data-stu-id="a34b5-150">**long**</span></span>            |
| <span data-ttu-id="a34b5-151">VendorID</span><span class="sxs-lookup"><span data-stu-id="a34b5-151">VendorID</span></span>            | <span data-ttu-id="a34b5-152">ID fornitore.</span><span class="sxs-lookup"><span data-stu-id="a34b5-152">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="a34b5-153">**long**</span><span class="sxs-lookup"><span data-stu-id="a34b5-153">**long**</span></span>            |
| <span data-ttu-id="a34b5-154">ModelID</span><span class="sxs-lookup"><span data-stu-id="a34b5-154">ModelID</span></span>             | <span data-ttu-id="a34b5-155">ID modello.</span><span class="sxs-lookup"><span data-stu-id="a34b5-155">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="a34b5-156">**long**</span><span class="sxs-lookup"><span data-stu-id="a34b5-156">**long**</span></span>            |
| <span data-ttu-id="a34b5-157">VendorText</span><span class="sxs-lookup"><span data-stu-id="a34b5-157">VendorText</span></span>          | <span data-ttu-id="a34b5-158">Nome del fornitore.</span><span class="sxs-lookup"><span data-stu-id="a34b5-158">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="a34b5-159">**BSTR** (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="a34b5-159">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="a34b5-160">ModelText</span><span class="sxs-lookup"><span data-stu-id="a34b5-160">ModelText</span></span>           | <span data-ttu-id="a34b5-161">Nome del modello del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a34b5-161">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="a34b5-162">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="a34b5-162">**BSTR**</span></span>            |
| <span data-ttu-id="a34b5-163">UnitModelText</span><span class="sxs-lookup"><span data-stu-id="a34b5-163">UnitModelText</span></span>       | <span data-ttu-id="a34b5-164">Nome del modello di unità; può corrispondere a ModelText.</span><span class="sxs-lookup"><span data-stu-id="a34b5-164">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="a34b5-165">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="a34b5-165">**BSTR**</span></span>            |
| <span data-ttu-id="a34b5-166">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="a34b5-166">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="a34b5-167">payload oPCR (controllo plug di output).</span><span class="sxs-lookup"><span data-stu-id="a34b5-167">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="a34b5-168">Esempio: 146 quadlets.</span><span class="sxs-lookup"><span data-stu-id="a34b5-168">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="a34b5-169">**long**</span><span class="sxs-lookup"><span data-stu-id="a34b5-169">**long**</span></span>            |
| <span data-ttu-id="a34b5-170">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="a34b5-170">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="a34b5-171">velocità dati oPCR.</span><span class="sxs-lookup"><span data-stu-id="a34b5-171">oPCR data rate.</span></span> <span data-ttu-id="a34b5-172">Esempi: 0 (S100), 1 (S200) o 2 (S400).</span><span class="sxs-lookup"><span data-stu-id="a34b5-172">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="a34b5-173">**long**</span><span class="sxs-lookup"><span data-stu-id="a34b5-173">**long**</span></span>            |
| <span data-ttu-id="a34b5-174">DeviceClassGUID</span><span class="sxs-lookup"><span data-stu-id="a34b5-174">DeviceClassGUID</span></span>     | <span data-ttu-id="a34b5-175">GUID che identifica il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a34b5-175">GUID that identifies the device driver.</span></span> <span data-ttu-id="a34b5-176">Per MSTape, questo valore è `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` .</span><span class="sxs-lookup"><span data-stu-id="a34b5-176">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="a34b5-177">Questo GUID viene definito come MSTapeDeviceGUID nel file di intestazione Xprtdefs. h.</span><span class="sxs-lookup"><span data-stu-id="a34b5-177">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="a34b5-178">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="a34b5-178">**BSTR**</span></span>            |
| <span data-ttu-id="a34b5-179">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a34b5-179">Description</span></span>         | <span data-ttu-id="a34b5-180">Una descrizione del dispositivo, ricavata dal file INF.</span><span class="sxs-lookup"><span data-stu-id="a34b5-180">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="a34b5-181">Questa stringa contiene in genere il nome del marchio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a34b5-181">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="a34b5-182">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="a34b5-182">**BSTR**</span></span>            |



 

<span data-ttu-id="a34b5-183">L'ID del dispositivo è un Integer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="a34b5-183">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="a34b5-184">Il **valore DWORD** basso viene archiviato nella proprietà con valore UniqueID \_ basso e il **valore DWORD** elevato viene archiviato nella \_ Proprietà alta UniqueId.</span><span class="sxs-lookup"><span data-stu-id="a34b5-184">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="a34b5-185">Per ulteriori informazioni sui moniker dei dispositivi, vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="a34b5-185">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a34b5-186">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a34b5-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a34b5-187">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="a34b5-187">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="a34b5-188">Controllo di una videocamera DV</span><span class="sxs-lookup"><span data-stu-id="a34b5-188">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




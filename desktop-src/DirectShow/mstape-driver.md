---
description: MSTape Driver
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: MSTape Driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951084f8827f925bba43028c0792736883d5ff0f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909399"
---
# <a name="mstape-driver"></a><span data-ttu-id="222b7-103">MSTape Driver</span><span class="sxs-lookup"><span data-stu-id="222b7-103">MSTape Driver</span></span>

<span data-ttu-id="222b7-104">Questo argomento si applica a Windows XP o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="222b7-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="222b7-105">Il driver MSTape supporta i dispositivi videocamere D-VHS e MPEG.</span><span class="sxs-lookup"><span data-stu-id="222b7-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="222b7-106">Viene esposto alle applicazioni come filtro [di acquisizione video WDM.](wdm-video-capture-filter.md)</span><span class="sxs-lookup"><span data-stu-id="222b7-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="222b7-107">La sua funzionalità è simile a quella di [MSDV,](msdv-driver.md)il driver del videocamere DV:</span><span class="sxs-lookup"><span data-stu-id="222b7-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="222b7-108">Viene visualizzato nelle categorie di filtro "Video Capture Sources" (CLSID \_ VideoInputDeviceCategory) e "WDM Streaming Rendering Devices" (AM \_ KSCATEGORY \_ RENDER).</span><span class="sxs-lookup"><span data-stu-id="222b7-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="222b7-109">Un'applicazione può creare un'istanza del filtro usando [**l'interfaccia ICreateDevEnum.**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)</span><span class="sxs-lookup"><span data-stu-id="222b7-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="222b7-110">Include un pin di output per l'acquisizione e il trasporto dal dispositivo e un pin di input per il trasporto al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="222b7-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="222b7-111">È possibile collegare un solo pin alla volta.</span><span class="sxs-lookup"><span data-stu-id="222b7-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="222b7-112">**Tipi di supporti**</span><span class="sxs-lookup"><span data-stu-id="222b7-112">**Media Types**</span></span>

<span data-ttu-id="222b7-113">Il pin di input supporta un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="222b7-113">The input pin supports one media type.</span></span>



| <span data-ttu-id="222b7-114">Label</span><span class="sxs-lookup"><span data-stu-id="222b7-114">Label</span></span> | <span data-ttu-id="222b7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="222b7-115">Value</span></span> |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="222b7-116">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="222b7-116">Major Type</span></span>   | <span data-ttu-id="222b7-117">Flusso \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="222b7-117">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="222b7-118">Subtype</span><span class="sxs-lookup"><span data-stu-id="222b7-118">Subtype</span></span>      | <span data-ttu-id="222b7-119">MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="222b7-119">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="222b7-120">Dimensione del campione</span><span class="sxs-lookup"><span data-stu-id="222b7-120">Sample Size</span></span>  | <span data-ttu-id="222b7-121">192 x 256</span><span class="sxs-lookup"><span data-stu-id="222b7-121">192 x 256</span></span>                                                  |
| <span data-ttu-id="222b7-122">Formatta blocco</span><span class="sxs-lookup"><span data-stu-id="222b7-122">Format Block</span></span> | [<span data-ttu-id="222b7-123">**MPEG2 \_ TRANSPORT \_ STRIDE**</span><span class="sxs-lookup"><span data-stu-id="222b7-123">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="222b7-124">Il pin di output supporta due tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="222b7-124">The output pin supports two media types.</span></span>



| <span data-ttu-id="222b7-125">Label</span><span class="sxs-lookup"><span data-stu-id="222b7-125">Label</span></span> | <span data-ttu-id="222b7-126">Valore</span><span class="sxs-lookup"><span data-stu-id="222b7-126">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="222b7-127">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="222b7-127">Major Type</span></span>   | <span data-ttu-id="222b7-128">Flusso \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="222b7-128">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="222b7-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="222b7-129">Subtype</span></span>      | <span data-ttu-id="222b7-130">MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="222b7-130">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="222b7-131">Dimensione del campione</span><span class="sxs-lookup"><span data-stu-id="222b7-131">Sample Size</span></span>  | <span data-ttu-id="222b7-132">192 x 256</span><span class="sxs-lookup"><span data-stu-id="222b7-132">192 x 256</span></span>                              |
| <span data-ttu-id="222b7-133">Blocco di formato</span><span class="sxs-lookup"><span data-stu-id="222b7-133">Format Block</span></span> | <span data-ttu-id="222b7-134">MPEG2 \_ TRANSPORT \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="222b7-134">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



| <span data-ttu-id="222b7-135">Label</span><span class="sxs-lookup"><span data-stu-id="222b7-135">Label</span></span> | <span data-ttu-id="222b7-136">Valore</span><span class="sxs-lookup"><span data-stu-id="222b7-136">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="222b7-137">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="222b7-137">Major Type</span></span>   | <span data-ttu-id="222b7-138">Flusso \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="222b7-138">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="222b7-139">Subtype</span><span class="sxs-lookup"><span data-stu-id="222b7-139">Subtype</span></span>      | <span data-ttu-id="222b7-140">MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="222b7-140">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="222b7-141">Dimensione del campione</span><span class="sxs-lookup"><span data-stu-id="222b7-141">Sample Size</span></span>  | <span data-ttu-id="222b7-142">188 x 256</span><span class="sxs-lookup"><span data-stu-id="222b7-142">188 x 256</span></span>                              |
| <span data-ttu-id="222b7-143">Blocco di formato</span><span class="sxs-lookup"><span data-stu-id="222b7-143">Format Block</span></span> | <span data-ttu-id="222b7-144">**NULL**</span><span class="sxs-lookup"><span data-stu-id="222b7-144">**NULL**</span></span>                               |



 

<span data-ttu-id="222b7-145">**Informazioni sul dispositivo**</span><span class="sxs-lookup"><span data-stu-id="222b7-145">**Device Information**</span></span>

<span data-ttu-id="222b7-146">Il driver legge dinamicamente le informazioni dalla ROM di configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="222b7-146">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="222b7-147">L'applicazione può recuperare queste informazioni associando il moniker del dispositivo a un contenitore di proprietà e chiamando il **metodo IPropertyBag::Read.**</span><span class="sxs-lookup"><span data-stu-id="222b7-147">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="222b7-148">Proprietà</span><span class="sxs-lookup"><span data-stu-id="222b7-148">Property</span></span>            | <span data-ttu-id="222b7-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="222b7-149">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="222b7-150">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="222b7-150">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="222b7-151">UniqueID \_ Low</span><span class="sxs-lookup"><span data-stu-id="222b7-151">UniqueID\_Low</span></span>       | <span data-ttu-id="222b7-152">ID univoco del dispositivo **(DWORD basso).**</span><span class="sxs-lookup"><span data-stu-id="222b7-152">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="222b7-153">**long** (VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="222b7-153">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="222b7-154">UniqueID \_ High</span><span class="sxs-lookup"><span data-stu-id="222b7-154">UniqueID\_High</span></span>      | <span data-ttu-id="222b7-155">ID univoco del dispositivo **(DWORD alto)**</span><span class="sxs-lookup"><span data-stu-id="222b7-155">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="222b7-156">**long**</span><span class="sxs-lookup"><span data-stu-id="222b7-156">**long**</span></span>            |
| <span data-ttu-id="222b7-157">VendorID</span><span class="sxs-lookup"><span data-stu-id="222b7-157">VendorID</span></span>            | <span data-ttu-id="222b7-158">ID fornitore.</span><span class="sxs-lookup"><span data-stu-id="222b7-158">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="222b7-159">**long**</span><span class="sxs-lookup"><span data-stu-id="222b7-159">**long**</span></span>            |
| <span data-ttu-id="222b7-160">ModelID</span><span class="sxs-lookup"><span data-stu-id="222b7-160">ModelID</span></span>             | <span data-ttu-id="222b7-161">ID modello.</span><span class="sxs-lookup"><span data-stu-id="222b7-161">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="222b7-162">**long**</span><span class="sxs-lookup"><span data-stu-id="222b7-162">**long**</span></span>            |
| <span data-ttu-id="222b7-163">Testo fornitore</span><span class="sxs-lookup"><span data-stu-id="222b7-163">VendorText</span></span>          | <span data-ttu-id="222b7-164">Nome del fornitore.</span><span class="sxs-lookup"><span data-stu-id="222b7-164">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="222b7-165">**BSTR** (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="222b7-165">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="222b7-166">Testo modello</span><span class="sxs-lookup"><span data-stu-id="222b7-166">ModelText</span></span>           | <span data-ttu-id="222b7-167">Nome del modello di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="222b7-167">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="222b7-168">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="222b7-168">**BSTR**</span></span>            |
| <span data-ttu-id="222b7-169">UnitModelText</span><span class="sxs-lookup"><span data-stu-id="222b7-169">UnitModelText</span></span>       | <span data-ttu-id="222b7-170">Nome del modello di unità; può essere uguale a ModelText.</span><span class="sxs-lookup"><span data-stu-id="222b7-170">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="222b7-171">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="222b7-171">**BSTR**</span></span>            |
| <span data-ttu-id="222b7-172">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="222b7-172">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="222b7-173">Payload oPCR (Output Plug Control).</span><span class="sxs-lookup"><span data-stu-id="222b7-173">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="222b7-174">Esempio: 146 quadlet.</span><span class="sxs-lookup"><span data-stu-id="222b7-174">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="222b7-175">**long**</span><span class="sxs-lookup"><span data-stu-id="222b7-175">**long**</span></span>            |
| <span data-ttu-id="222b7-176">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="222b7-176">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="222b7-177">Frequenza dei dati oPCR.</span><span class="sxs-lookup"><span data-stu-id="222b7-177">oPCR data rate.</span></span> <span data-ttu-id="222b7-178">Esempi: 0 (S100), 1 (S200) o 2 (S400).</span><span class="sxs-lookup"><span data-stu-id="222b7-178">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="222b7-179">**long**</span><span class="sxs-lookup"><span data-stu-id="222b7-179">**long**</span></span>            |
| <span data-ttu-id="222b7-180">DeviceClassGUID</span><span class="sxs-lookup"><span data-stu-id="222b7-180">DeviceClassGUID</span></span>     | <span data-ttu-id="222b7-181">GUID che identifica il driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="222b7-181">GUID that identifies the device driver.</span></span> <span data-ttu-id="222b7-182">Per MSTape, questo valore è `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` .</span><span class="sxs-lookup"><span data-stu-id="222b7-182">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="222b7-183">Questo GUID è definito come MSTapeDeviceGUID nel file di intestazione Xprtdefs.h.</span><span class="sxs-lookup"><span data-stu-id="222b7-183">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="222b7-184">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="222b7-184">**BSTR**</span></span>            |
| <span data-ttu-id="222b7-185">Descrizione</span><span class="sxs-lookup"><span data-stu-id="222b7-185">Description</span></span>         | <span data-ttu-id="222b7-186">Descrizione del dispositivo, tratto dal file INF.</span><span class="sxs-lookup"><span data-stu-id="222b7-186">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="222b7-187">Questa stringa contiene in genere il nome del marchio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="222b7-187">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="222b7-188">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="222b7-188">**BSTR**</span></span>            |



 

<span data-ttu-id="222b7-189">L'ID dispositivo è un intero a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="222b7-189">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="222b7-190">Il **valore DWORD basso** viene archiviato nella proprietà UniqueID Low e il valore DWORD alto viene archiviato \_ nella proprietà UniqueID  \_ High.</span><span class="sxs-lookup"><span data-stu-id="222b7-190">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="222b7-191">Per altre informazioni sui moniker dei dispositivi, vedere [Uso dell'enumeratore dispositivo di sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="222b7-191">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="222b7-192">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="222b7-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="222b7-193">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="222b7-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="222b7-194">Controllo di un camcorder DV</span><span class="sxs-lookup"><span data-stu-id="222b7-194">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 




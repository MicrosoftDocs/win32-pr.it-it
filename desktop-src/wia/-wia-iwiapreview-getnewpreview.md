---
description: Memorizza nella cache internamente l'immagine non filtrata restituita dal driver.
ms.assetid: 09cb242d-d1d6-4130-8b49-0770940471d8
title: 'Metodo IWiaPreview:: GetNewPreview (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.GetNewPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c3f1251e7ec1b98d43e616c1ff6f2b3b2aacd8b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307358"
---
# <a name="iwiapreviewgetnewpreview-method"></a><span data-ttu-id="06341-103">Metodo IWiaPreview:: GetNewPreview</span><span class="sxs-lookup"><span data-stu-id="06341-103">IWiaPreview::GetNewPreview method</span></span>

<span data-ttu-id="06341-104">Memorizza nella cache internamente l'immagine non filtrata restituita dal driver.</span><span class="sxs-lookup"><span data-stu-id="06341-104">Caches internally the unfiltered image returned from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="06341-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06341-105">Syntax</span></span>


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="06341-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="06341-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06341-107">*pWiaItem2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06341-107">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06341-108">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="06341-108">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="06341-109">Specifica un puntatore all'elemento [_ *IWiaItem2* \*](-wia-iwiaitem2.md) per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="06341-109">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for the image.</span></span>

</dd> <dt>

<span data-ttu-id="06341-110">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06341-110">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06341-111">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="06341-111">Type: **LONG**</span></span>

<span data-ttu-id="06341-112">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="06341-112">Currently unused.</span></span> <span data-ttu-id="06341-113">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="06341-113">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="06341-114">*pWiaTransferCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06341-114">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06341-115">Tipo: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="06341-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="06341-116">Specifica un puntatore all'interfaccia [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) dell'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="06341-116">Specifies a pointer to the calling application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06341-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06341-117">Return value</span></span>

<span data-ttu-id="06341-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="06341-118">Type: **HRESULT**</span></span>

<span data-ttu-id="06341-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="06341-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06341-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06341-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="06341-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="06341-121">Remarks</span></span>

<span data-ttu-id="06341-122">Un'applicazione deve chiamare **IWiaPreview:: GetNewPreview** prima di chiamare [**IWiaPreview::D etectregions**](-wia-iwiapreview-detectregions.md).</span><span class="sxs-lookup"><span data-stu-id="06341-122">An application must call **IWiaPreview::GetNewPreview** before it calls [**IWiaPreview::DetectRegions**](-wia-iwiapreview-detectregions.md).</span></span>

<span data-ttu-id="06341-123">**IWiaPreview:: GetNewPreview** imposta la proprietà di [**\_ \_ Anteprima WIA DPS**](-wia-wiaitempropscannerdevice.md) (e la Reimposta prima della restituzione, a meno che non sia stata impostata in precedenza).</span><span class="sxs-lookup"><span data-stu-id="06341-123">**IWiaPreview::GetNewPreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="06341-124">Ciò consente al driver e all'hardware, nonché al filtro di elaborazione delle immagini, di tenere presente che l'elemento è un'analisi di anteprima.</span><span class="sxs-lookup"><span data-stu-id="06341-124">This lets the driver and hardware, as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="06341-125">Internamente, il componente di anteprima Windows Image Acquisition (WIA) 2,0 crea un'istanza del filtro di elaborazione delle immagini del driver chiamando [**GetExtension**](-wia-iwiaitem2-getextension.md) in *pWiaItem2*.</span><span class="sxs-lookup"><span data-stu-id="06341-125">Internally, the Windows Image Acquisition (WIA) 2.0 preview component creates an instance of the driver's image processing filter by calling [**GetExtension**](-wia-iwiaitem2-getextension.md) on *pWiaItem2*.</span></span> <span data-ttu-id="06341-126">Il componente WIA 2,0 Preview esegue questa operazione quando l'applicazione chiama **IWiaPreview:: GetNewPreview**.</span><span class="sxs-lookup"><span data-stu-id="06341-126">The WIA 2.0 preview component does this when the application calls **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="06341-127">Il componente WIA 2,0 Preview Inizializza anche il filtro in **IWiaPreview:: GetNewPreview**.</span><span class="sxs-lookup"><span data-stu-id="06341-127">The WIA 2.0 preview component also initializes the filter in **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="06341-128">La stessa istanza di filtro viene utilizzata dal componente WIA 2,0 Preview durante una chiamata a [**IWiaPreview:: UpdatePreview**](-wia-iwiapreview-updatepreview.md).</span><span class="sxs-lookup"><span data-stu-id="06341-128">The same filter instance is used by the WIA 2.0 preview component during a call to [**IWiaPreview::UpdatePreview**](-wia-iwiapreview-updatepreview.md).</span></span>

<span data-ttu-id="06341-129">Prima di chiamare il componente WIA 2,0 Preview, un'applicazione deve chiamare [**CheckExtension**](-wia-iwiaitem2-checkextension.md) per verificare che il driver sia dotato di un filtro di elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="06341-129">Before calling into the WIA 2.0 preview component, an application should call [**CheckExtension**](-wia-iwiaitem2-checkextension.md) to make sure that the driver comes with an image processing filter.</span></span> <span data-ttu-id="06341-130">Deve chiamare **CheckExtension** sull'elemento che passerà a **IWiaPreview:: GetNewPreview**.</span><span class="sxs-lookup"><span data-stu-id="06341-130">It should call **CheckExtension** on the item that it would pass to **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="06341-131">È inutile fornire anteprime in tempo reale senza un filtro di elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="06341-131">It is useless to provide live previews without an image processing filter.</span></span> <span data-ttu-id="06341-132">Se un'applicazione chiama **IWiaPreview:: GetNewPreview** per un driver senza un filtro di elaborazione dell'immagine, la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="06341-132">If an application calls **IWiaPreview::GetNewPreview** for a driver without an image processing filter, the call will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="06341-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="06341-133">Examples</span></span>

<span data-ttu-id="06341-134">CheckImgFilter controlla se il driver ha un filtro di elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="06341-134">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="06341-135">Prima di chiamare il componente di anteprima, un'applicazione deve verificare che il driver disponga di un filtro di elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="06341-135">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



<span data-ttu-id="06341-136">DownloadPreviewImage Scarica i dati dell'immagine dallo scanner chiamando il metodo **IWiaPreview:: GetNewPreview** del componente di anteprima.</span><span class="sxs-lookup"><span data-stu-id="06341-136">DownloadPreviewImage downloads image data from the scanner by calling the preview component's **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="06341-137">Chiama quindi DetectSubregions se l'utente dell'applicazione desidera richiamare il filtro di segmentazione, che crea un elemento figlio in pWiaItem2 per ogni area rilevata.</span><span class="sxs-lookup"><span data-stu-id="06341-137">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="06341-138">Vedere [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) per il metodo DetectSubregions usato in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="06341-138">See [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="06341-139">In questo esempio, l'utente dell'applicazione imposta facendo `m_bUseSegmentationFilter` clic su una casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="06341-139">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="06341-140">Se l'applicazione supporta questa operazione, è necessario innanzitutto verificare che il driver disponga di un filtro di segmentazione chiamando [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span><span class="sxs-lookup"><span data-stu-id="06341-140">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="06341-141">Vedere **IWiaPreview:: GetNewPreview** per l'esempio di metodo CheckImgFilter che illustra il modo in cui è possibile eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="06341-141">See **IWiaPreview::GetNewPreview** for the CheckImgFilter method example that shows how this can be done.</span></span>


```C++
HRESULT
DownloadPreviewImage(
   IN IWiaItem2 *pWiaFlatbedItem2)
{
   HRESULT hr              = S_OK;
   BOOL    bHasImgFilter   = FALSE;

   IWiaTransferCallback *pAppWiaTransferCallback = NULL;

   hr = CheckImgFilter(pWiaFlatbedItem2, &bHasImgFilter)

   if (SUCCEEDED(hr))
   {
      if (bHasImgFilter)
      {
         IWiaPreview *pWiaPreview = NULL;

         // In this example, the AppWiaTransferCallback class implements 
         // the IWiaTransferCallback interface.  
         // The constructor of AppWiaTransferCallback sets the reference count to 1.
         pAppWiaTransferCallback = new AppWiaTransferCallback();

         hr = pAppWiaTransferCallback ? S_OK : E_OUTOFMEMORY;

         if (SUCCEEDED(hr))
         {
            // Acquire image from scanner
            hr = m_pWiaPreview->GetNewPreview(pWiaFlatbedItem2,
                                              0,
                                              pAppWiaTransferCallback);    
         }

         //
         // Check the application UI for whether the user wants
         // to use the segmentation filter indicated by the value 
         // of m_bUseSegmentationFilter.
         //
         // m_FlatbedPreviewStream is the stream that
         // AppWiaTransferCallback::GetNextStream returned for the
         // flatbed item.
         // This stream is where the image data is stored after
         // the successful return of GetNewPreview.
         // The stream is passed into the segmentation filter
         // for region detection.
         if (SUCCEEDED(hr) && m_bUseSegmentationFilter)
         {
            DetectSubregions(m_FlatbedPreviewStream, pWiaFlatbedItem2);
         }

         if (pAppWiaTransferCallback)
         {
            // If the call to GetNewPreview was successful, the
            // preview component calls AddRef on the callback so
            // this call doesn't delete the object.

            pAppWiaTransferCallback->Release();
         }

      }
      else
      {
         // Do not create an instance of preview component if the driver does
         // not come with an image processing filter.
         // You can use segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="06341-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06341-142">Requirements</span></span>



| <span data-ttu-id="06341-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="06341-143">Requirement</span></span> | <span data-ttu-id="06341-144">Valore</span><span class="sxs-lookup"><span data-stu-id="06341-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="06341-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06341-145">Minimum supported client</span></span><br/> | <span data-ttu-id="06341-146">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06341-146">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="06341-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06341-147">Minimum supported server</span></span><br/> | <span data-ttu-id="06341-148">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06341-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="06341-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06341-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="06341-150"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="06341-150"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="06341-151">IDL</span><span class="sxs-lookup"><span data-stu-id="06341-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06341-152"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="06341-152"><dt>Wia.idl</dt></span></span> </dl> |



 

 





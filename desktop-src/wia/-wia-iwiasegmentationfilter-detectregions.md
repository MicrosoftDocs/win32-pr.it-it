---
description: Determina le aree secondarie di un'immagine disposte sulla piastra piana, in modo che ogni area secondaria possa essere acquisita in un elemento immagine separato.
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: Metodo IWiaSegmentationFilter::D etectRegions (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 94fe2f5076e9ff7cc0de0f7c916f6edacf2d03fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129415"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a><span data-ttu-id="95201-103">IWiaSegmentationFilter::D Metodo etectRegions</span><span class="sxs-lookup"><span data-stu-id="95201-103">IWiaSegmentationFilter::DetectRegions method</span></span>

<span data-ttu-id="95201-104">Determina le aree secondarie di un'immagine disposte sulla piastra piana, in modo che ogni area secondaria possa essere acquisita in un elemento immagine separato.</span><span class="sxs-lookup"><span data-stu-id="95201-104">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span>

## <a name="syntax"></a><span data-ttu-id="95201-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95201-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="95201-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="95201-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95201-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95201-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95201-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="95201-108">Type: **LONG**</span></span>

<span data-ttu-id="95201-109">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="95201-109">Currently unused.</span></span> <span data-ttu-id="95201-110">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="95201-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="95201-111">*pInputStream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95201-111">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95201-112">Tipo: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="95201-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="95201-113">Specifica un puntatore all'immagine di anteprima di [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="95201-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) preview image.</span></span>

</dd> <dt>

<span data-ttu-id="95201-114">_pWiaItem2 \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95201-114">_pWiaItem2\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95201-115">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="95201-115">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="95201-116">Specifica un puntatore all'elemento [_ *IWiaItem2* \*](-wia-iwiaitem2.md) per il quale è stato acquisito *pInputStream* .</span><span class="sxs-lookup"><span data-stu-id="95201-116">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for which *pInputStream* was acquired.</span></span> <span data-ttu-id="95201-117">Il filtro di segmentazione crea elementi figlio per questo elemento.</span><span class="sxs-lookup"><span data-stu-id="95201-117">The segmentation filter creates child items for this item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95201-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95201-118">Return value</span></span>

<span data-ttu-id="95201-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="95201-119">Type: **HRESULT**</span></span>

<span data-ttu-id="95201-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="95201-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="95201-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="95201-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="95201-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="95201-122">Remarks</span></span>

<span data-ttu-id="95201-123">Questo metodo determina le aree secondarie dell'immagine rappresentata da pInputStream.</span><span class="sxs-lookup"><span data-stu-id="95201-123">This method determines the sub-regions of the image represented by pInputStream.</span></span> <span data-ttu-id="95201-124">Per ogni area secondaria rilevata, viene creato un elemento figlio per l'elemento [**IWiaItem2**](-wia-iwiaitem2.md) specificato nel parametro *pWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="95201-124">For each sub-region that it detects, it creates a child item for the [**IWiaItem2**](-wia-iwiaitem2.md) item specified in the *pWiaItem2* parameter.</span></span> <span data-ttu-id="95201-125">Per ogni elemento figlio, il filtro di segmentazione deve impostare i valori per il rettangolo di delimitazione dell'area da analizzare, usando le [**costanti della proprietà elemento WIA dello scanner**](-wia-wiaitempropscanneritem.md)seguenti.</span><span class="sxs-lookup"><span data-stu-id="95201-125">For each child item, the segmentation filter must set values for the bounding rectangle of the area to scan, using the following [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

-   [<span data-ttu-id="95201-126">**\_indirizzi IP WIA \_ XPos**</span><span class="sxs-lookup"><span data-stu-id="95201-126">**WIA\_IPS\_XPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="95201-127">**\_indirizzi IP WIA \_ YPos**</span><span class="sxs-lookup"><span data-stu-id="95201-127">**WIA\_IPS\_YPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="95201-128">**\_indirizzi IP WIA \_ stampa**</span><span class="sxs-lookup"><span data-stu-id="95201-128">**WIA\_IPS\_XEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="95201-129">**\_indirizzi IP WIA \_ YEXTENT**</span><span class="sxs-lookup"><span data-stu-id="95201-129">**WIA\_IPS\_YEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)

<span data-ttu-id="95201-130">Un filtro più avanzato può anche richiedere che altre [**costanti di proprietà degli elementi WIA dello scanner**](-wia-wiaitempropscanneritem.md) , ad esempio gli **IP WIA, \_ \_ deasimmetria \_ X** e gli **IP WIA, \_ \_ desfasamento \_ Y**, se il driver supporta la deasimmetria.</span><span class="sxs-lookup"><span data-stu-id="95201-130">A more advanced filter may also require other [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md) such as **WIA\_IPS\_DESKEW\_X** and **WIA\_IPS\_DESKEW\_Y**, if the driver supports de-skewing.</span></span>

<span data-ttu-id="95201-131">Se l'applicazione chiama **IWiaSegmentationFilter::D etectregions** più di una volta, l'applicazione deve prima eliminare gli elementi figlio creati dall'ultima chiamata a **IWiaSegmentationFilter::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="95201-131">If the application calls **IWiaSegmentationFilter::DetectRegions** more than once, the application must first delete the child items created by the last call to **IWiaSegmentationFilter::DetectRegions**.</span></span>

<span data-ttu-id="95201-132">Se un'applicazione modifica le proprietà in *pWiaItem2*, tra l'acquisizione dell'immagine in *pInputStream* e la chiamata a **IWiaSegmentationFilter::D etectregions**, le proprietà originali, ovvero le proprietà che l'elemento aveva quando il flusso è stato acquisito, devono essere ripristinate.</span><span class="sxs-lookup"><span data-stu-id="95201-132">If an application changes any properties into *pWiaItem2*, between acquiring the image into *pInputStream* and its call to **IWiaSegmentationFilter::DetectRegions**, the original properties (that is, the properties the item had when the stream was acquired) must be restored.</span></span> <span data-ttu-id="95201-133">Questa operazione può essere eseguita da [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) e [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).</span><span class="sxs-lookup"><span data-stu-id="95201-133">This can be done by [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).</span></span>

<span data-ttu-id="95201-134">L'applicazione deve reimpostare [IStream](/windows/win32/api/objidl/nn-objidl-istream) se la chiamata passa lo stesso flusso al filtro di segmentazione più di una volta.</span><span class="sxs-lookup"><span data-stu-id="95201-134">The application must reset the [IStream](/windows/win32/api/objidl/nn-objidl-istream) if its call passes the same stream into the segmentation filter more than once.</span></span> <span data-ttu-id="95201-135">L'applicazione deve inoltre reimpostare il flusso dopo il download iniziale e prima di chiamare **IWiaSegmentationFilter::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="95201-135">The application must also reset the stream after the initial download and before calling **IWiaSegmentationFilter::DetectRegions**.</span></span>

## <a name="examples"></a><span data-ttu-id="95201-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="95201-136">Examples</span></span>

<span data-ttu-id="95201-137">La segmentazione esegue il rilevamento dell'area nel flusso ( `pImageStream` ) passato a DetectSubregions.</span><span class="sxs-lookup"><span data-stu-id="95201-137">The segmentation performs region detection on the stream (`pImageStream`) passed into DetectSubregions.</span></span> <span data-ttu-id="95201-138">Vedere il metodo [**GetExtension**](-wia-iwiaitem2-getextension.md) per CreateSegmentationFilter usato in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="95201-138">See the [**GetExtension**](-wia-iwiaitem2-getextension.md) for CreateSegmentationFilter method used in this example.</span></span>


```C++
HRESULT
DetectSubregions(
   IN IStream   *pImageStream,
   IN IWiaItem2 *pWiaItem2)
{
   HRESULT                 hr                  = S_OK;
   IWiaSegmentationFilter* pSegmentationFilter = NULL;

   if (!pWiaItem2 || !pImageStream)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      hr = CreateSegmentationFilter(pWiaItem2, &pSegmentationFilter);
   }

   if (SUCCEEDED(hr))
   {
      hr = pSegmentationFilter->DetectRegions(0,pImageStream, pWiaItem2); 
   }

   if (pSegmentationFilter)
   {
      pSegmentationFilter->Release();
      pSegmentationFilter = NULL;
   }

   return hr;
}
```



<span data-ttu-id="95201-139">DownloadPreviewImage Scarica i dati dell'immagine dallo scanner chiamando il metodo [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) del componente di anteprima.</span><span class="sxs-lookup"><span data-stu-id="95201-139">DownloadPreviewImage downloads image data from the scanner by calling the preview component's [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="95201-140">Chiama quindi DetectSubregions se l'utente dell'applicazione desidera richiamare il filtro di segmentazione, che crea un elemento figlio in pWiaItem2 per ogni area rilevata.</span><span class="sxs-lookup"><span data-stu-id="95201-140">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="95201-141">Vedere **IWiaSegmentationFilter::D etectregions** per il metodo DetectSubregions usato in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="95201-141">See **IWiaSegmentationFilter::DetectRegions** for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="95201-142">In questo esempio, l'utente dell'applicazione imposta facendo `m_bUseSegmentationFilter` clic su una casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="95201-142">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="95201-143">Se l'applicazione supporta questa operazione, è necessario innanzitutto verificare che il driver disponga di un filtro di segmentazione chiamando [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span><span class="sxs-lookup"><span data-stu-id="95201-143">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="95201-144">Vedere [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) per l'esempio di metodo CheckImgFilter che illustra come eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="95201-144">See [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) for the CheckImgFilter method example that shows how this can be done.</span></span>


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
         // The constructor of AppWiaTransferCallback sets the reference count 
         // to 1.
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
         // Do not create an instance of preview component if the driver 
         // does not come with an image-processing filter.
         // You can use a segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="95201-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95201-145">Requirements</span></span>



| <span data-ttu-id="95201-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="95201-146">Requirement</span></span> | <span data-ttu-id="95201-147">Valore</span><span class="sxs-lookup"><span data-stu-id="95201-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95201-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95201-148">Minimum supported client</span></span><br/> | <span data-ttu-id="95201-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95201-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="95201-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95201-150">Minimum supported server</span></span><br/> | <span data-ttu-id="95201-151">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="95201-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="95201-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95201-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="95201-153"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="95201-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="95201-154">IDL</span><span class="sxs-lookup"><span data-stu-id="95201-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95201-155"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95201-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 

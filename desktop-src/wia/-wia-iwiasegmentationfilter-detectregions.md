---
description: Determina le sottoaree di un'immagine disposte sul pistoia piana in modo che ognuna delle sottoaree possa essere acquisita in un elemento immagine separato.
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: Metodo IWiaSegmentationFilter::D etectRegions (Wia.h)
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
ms.openlocfilehash: 46496360d7b54bed837ba287d604233a9fac98ee13807744b4adbfb52e9934d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450261"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a>Metodo IWiaSegmentationFilter::D etectRegions

Determina le sottoaree di un'immagine disposte sul pistoia piana in modo che ognuna delle sottoaree possa essere acquisita in un elemento immagine separato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Attualmente inutilizzato. Deve essere impostato su zero.

</dd> <dt>

*pInputStream* \[ Pollici\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Specifica un puntatore [all'immagine di anteprima IStream.](/windows/win32/api/objidl/nn-objidl-istream)

</dd> <dt>

*pWiaItem2* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Specifica un puntatore [**all'elemento IWiaItem2**](-wia-iwiaitem2.md) per il quale *è stato acquisito pInputStream.* Il filtro di segmentazione crea elementi figlio per questo elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo determina le aree secondarie dell'immagine rappresentata da pInputStream. Per ogni area secondaria rilevata, crea un elemento figlio per [**l'elemento IWiaItem2**](-wia-iwiaitem2.md) specificato nel *parametro pWiaItem2.* Per ogni elemento figlio, il filtro di segmentazione deve impostare i valori per il rettangolo di delimitazione dell'area da analizzare, usando le costanti delle proprietà degli elementi [**WIA scanner seguenti.**](-wia-wiaitempropscanneritem.md)

-   [**WIA \_ IPS \_ XPOS**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IPS \_ YPOS**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IPS \_ XEXTENT**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IPS \_ YEXTENT**](-wia-wiaitempropscanneritem.md)

Un filtro più avanzato può anche richiedere altre costanti delle proprietà elemento [**WIA**](-wia-wiaitempropscanneritem.md) dello scanner, ad esempio **WIA \_ IPS \_ DESKEW \_ X** e **WIA \_ IPS \_ DESKEW \_ Y,** se il driver supporta la deviazione.

Se l'applicazione chiama **IWiaSegmentationFilter::D etectRegions** più di una volta, l'applicazione deve prima eliminare gli elementi figlio creati dall'ultima chiamata a **IWiaSegmentationFilter::D etectRegions.**

Se un'applicazione modifica le proprietà in *pWiaItem2,* tra l'acquisizione dell'immagine in *pInputStream* e la chiamata a **IWiaSegmentationFilter::D etectRegions,** è necessario ripristinare le proprietà originali, ovvero le proprietà dell'elemento al momento dell'acquisizione del flusso. Questa operazione può essere eseguita [**da GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) e [**SetPropertyStream.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream)

L'applicazione deve reimpostare [IStream](/windows/win32/api/objidl/nn-objidl-istream) se la chiamata passa lo stesso flusso nel filtro di segmentazione più di una volta. L'applicazione deve anche reimpostare il flusso dopo il download iniziale e prima di chiamare **IWiaSegmentationFilter::D etectRegions**.

## <a name="examples"></a>Esempio

La segmentazione esegue il rilevamento dell'area nel flusso ( `pImageStream` ) passato in DetectSubregions. Vedere il [**metodo GetExtension**](-wia-iwiaitem2-getextension.md) per CreateSegmentationFilter usato in questo esempio.


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



DownloadPreviewImage scarica i dati delle immagini dallo scanner chiamando il metodo [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) del componente di anteprima. Chiama quindi DetectSubregions se l'utente dell'applicazione vuole richiamare il filtro di segmentazione, che crea un elemento figlio in pWiaItem2 per ogni area rilevata. Vedere **IWiaSegmentationFilter::D etectRegions** per il metodo DetectSubregions usato in questo esempio.

In questo esempio l'utente dell'applicazione imposta `m_bUseSegmentationFilter` facendo clic su una casella di controllo. Se l'applicazione supporta questa funzionalità, deve prima verificare che il driver abbia un filtro di segmentazione chiamando [**CheckExtension.**](-wia-iwiaitem2-checkextension.md) Vedere [**GetNewPreview per**](-wia-iwiapreview-getnewpreview.md) l'esempio di metodo CheckImgFilter che illustra come eseguire questa operazione.


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 

---
description: Memorizza nella cache internamente l'immagine non filtrata restituita dal driver.
ms.assetid: 09cb242d-d1d6-4130-8b49-0770940471d8
title: Metodo IWiaPreview::GetNewPreview (Wia.h)
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
ms.openlocfilehash: 2200452fe586a4755a4560f0f68094e5f107e9e7d69a823bafac4d33bc1c6ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965560"
---
# <a name="iwiapreviewgetnewpreview-method"></a>Metodo IWiaPreview::GetNewPreview

Memorizza nella cache internamente l'immagine non filtrata restituita dal driver.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWiaItem2* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Specifica un puntatore [**all'elemento IWiaItem2**](-wia-iwiaitem2.md) per l'immagine.

</dd> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Attualmente inutilizzato. Deve essere impostato su zero.

</dd> <dt>

*pWiaTransferCallback* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Specifica un puntatore all'interfaccia [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) dell'applicazione chiamante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Un'applicazione deve **chiamare IWiaPreview::GetNewPreview** prima di chiamare [**IWiaPreview::D etectRegions**](-wia-iwiapreview-detectregions.md).

**IWiaPreview::GetNewPreview** imposta la proprietà [**\_ \_ WIA DPS PREVIEW**](-wia-wiaitempropscannerdevice.md) (e la reimposta prima che venga restituita, a meno che non sia stata impostata in precedenza). Ciò consente al driver e all'hardware, nonché al filtro di elaborazione delle immagini, di sapere che l'elemento è un'analisi di anteprima.

Internamente, il componente di anteprima di Windows Image Acquisition (WIA) 2.0 crea un'istanza del filtro di elaborazione delle immagini del driver chiamando [**GetExtension**](-wia-iwiaitem2-getextension.md) su *pWiaItem2.* Il componente di anteprima di WIA 2.0 esegue questa operazione quando l'applicazione chiama **IWiaPreview::GetNewPreview**. Il componente di anteprima di WIA 2.0 inizializza anche il filtro in **IWiaPreview::GetNewPreview.** La stessa istanza di filtro viene usata dal componente di anteprima di WIA 2.0 durante una chiamata a [**IWiaPreview::UpdatePreview.**](-wia-iwiapreview-updatepreview.md)

Prima di chiamare il componente di anteprima di WIA 2.0, un'applicazione deve chiamare [**CheckExtension**](-wia-iwiaitem2-checkextension.md) per assicurarsi che il driver venga fornito con un filtro di elaborazione delle immagini. Deve chiamare **CheckExtension sull'elemento** che passerebbe a **IWiaPreview::GetNewPreview.** È inutile fornire anteprime live senza un filtro di elaborazione delle immagini. Se un'applicazione chiama **IWiaPreview::GetNewPreview** per un driver senza un filtro di elaborazione delle immagini, la chiamata avrà esito negativo.

## <a name="examples"></a>Esempio

CheckImgFilter controlla se il driver dispone di un filtro di elaborazione delle immagini. Prima di chiamare il componente di anteprima, un'applicazione deve assicurarsi che il driver abbia un filtro di elaborazione delle immagini.


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



DownloadPreviewImage scarica i dati delle immagini dallo scanner chiamando il metodo **IWiaPreview::GetNewPreview** del componente di anteprima. Chiama quindi DetectSubregions se l'utente dell'applicazione vuole richiamare il filtro di segmentazione, che crea un elemento figlio in pWiaItem2 per ogni area rilevata. Vedere [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) per il metodo DetectSubregions usato in questo esempio.

In questo esempio l'utente dell'applicazione imposta `m_bUseSegmentationFilter` facendo clic su una casella di controllo. Se l'applicazione supporta questa funzionalità, deve prima verificare che il driver abbia un filtro di segmentazione chiamando [**CheckExtension.**](-wia-iwiaitem2-checkextension.md) Vedere **IWiaPreview::GetNewPreview** per l'esempio del metodo CheckImgFilter che illustra come eseguire questa operazione.


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 





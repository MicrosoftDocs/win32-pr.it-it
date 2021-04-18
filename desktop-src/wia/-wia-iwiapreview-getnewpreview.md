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
# <a name="iwiapreviewgetnewpreview-method"></a>Metodo IWiaPreview:: GetNewPreview

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

*pWiaItem2* \[ in\]
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Specifica un puntatore all'elemento [_ *IWiaItem2* *](-wia-iwiaitem2.md) per l'immagine.

</dd> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Attualmente non usato. Deve essere impostato su zero.

</dd> <dt>

*pWiaTransferCallback* \[ in\]
</dt> <dd>

Tipo: **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _

Specifica un puntatore all'interfaccia [_ *IWiaTransferCallback* *](-wia-iwiatransfercallback.md) dell'applicazione chiamante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Un'applicazione deve chiamare **IWiaPreview:: GetNewPreview** prima di chiamare [**IWiaPreview::D etectregions**](-wia-iwiapreview-detectregions.md).

**IWiaPreview:: GetNewPreview** imposta la proprietà di [**\_ \_ Anteprima WIA DPS**](-wia-wiaitempropscannerdevice.md) (e la Reimposta prima della restituzione, a meno che non sia stata impostata in precedenza). Ciò consente al driver e all'hardware, nonché al filtro di elaborazione delle immagini, di tenere presente che l'elemento è un'analisi di anteprima.

Internamente, il componente di anteprima Windows Image Acquisition (WIA) 2,0 crea un'istanza del filtro di elaborazione delle immagini del driver chiamando [**GetExtension**](-wia-iwiaitem2-getextension.md) in *pWiaItem2*. Il componente WIA 2,0 Preview esegue questa operazione quando l'applicazione chiama **IWiaPreview:: GetNewPreview**. Il componente WIA 2,0 Preview Inizializza anche il filtro in **IWiaPreview:: GetNewPreview**. La stessa istanza di filtro viene utilizzata dal componente WIA 2,0 Preview durante una chiamata a [**IWiaPreview:: UpdatePreview**](-wia-iwiapreview-updatepreview.md).

Prima di chiamare il componente WIA 2,0 Preview, un'applicazione deve chiamare [**CheckExtension**](-wia-iwiaitem2-checkextension.md) per verificare che il driver sia dotato di un filtro di elaborazione delle immagini. Deve chiamare **CheckExtension** sull'elemento che passerà a **IWiaPreview:: GetNewPreview**. È inutile fornire anteprime in tempo reale senza un filtro di elaborazione delle immagini. Se un'applicazione chiama **IWiaPreview:: GetNewPreview** per un driver senza un filtro di elaborazione dell'immagine, la chiamata avrà esito negativo.

## <a name="examples"></a>Esempio

CheckImgFilter controlla se il driver ha un filtro di elaborazione delle immagini. Prima di chiamare il componente di anteprima, un'applicazione deve verificare che il driver disponga di un filtro di elaborazione delle immagini.


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



DownloadPreviewImage Scarica i dati dell'immagine dallo scanner chiamando il metodo **IWiaPreview:: GetNewPreview** del componente di anteprima. Chiama quindi DetectSubregions se l'utente dell'applicazione desidera richiamare il filtro di segmentazione, che crea un elemento figlio in pWiaItem2 per ogni area rilevata. Vedere [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) per il metodo DetectSubregions usato in questo esempio.

In questo esempio, l'utente dell'applicazione imposta facendo `m_bUseSegmentationFilter` clic su una casella di controllo. Se l'applicazione supporta questa operazione, è necessario innanzitutto verificare che il driver disponga di un filtro di segmentazione chiamando [**CheckExtension**](-wia-iwiaitem2-checkextension.md). Vedere **IWiaPreview:: GetNewPreview** per l'esempio di metodo CheckImgFilter che illustra il modo in cui è possibile eseguire questa operazione.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 





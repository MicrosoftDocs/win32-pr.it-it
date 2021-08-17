---
description: Ottiene le interfacce di estensione che possono essere associate a un driver Windows image acquisition (WIA) 2.0.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: Metodo IWiaItem2::GetExtension (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 4c9738afe60d79b73149c9dd7dda8c3bbd1017c3b41d023b47160b624bcd7c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450416"
---
# <a name="iwiaitem2getextension-method"></a>Metodo IWiaItem2::GetExtension

Ottiene le interfacce di estensione che possono essere associate a un driver Windows image acquisition (WIA) 2.0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Attualmente inutilizzato. Deve essere impostato su zero.

</dd> <dt>

*bstrName* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome dell'estensione a cui l'applicazione chiamante richiede un puntatore.

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**


</dt> <dd>

Estensione del filtro di segmentazione. Questo è attualmente l'unico valore valido per questo parametro.

</dd> </dl> </dd> <dt>

*riidExtensionInterface* \[ Pollici\]
</dt> <dd>

Tipo: **REFIID**

Specifica l'identificatore dell'interfaccia di estensione.

</dd> <dt>

*ppOut* \[ Cambio\]
</dt> <dd>

Tipo: **\* \* VOID**

Riceve l'indirizzo di un puntatore all'interfaccia di estensione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Un'applicazione richiama questo metodo per creare un oggetto di estensione che implementa una delle interfacce di estensione del driver WIA 2.0. **IWiaItem2::GetExtension** archivia l'indirizzo dell'interfaccia di estensione dell'oggetto estensione nel *parametro riidExtensionInterface.* L'applicazione usa quindi il puntatore a interfaccia per chiamare i relativi metodi.

Le applicazioni devono chiamare [il metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori a interfaccia ricevuti tramite il *parametro riidExtensionInterface.*

## <a name="examples"></a>Esempio

CreateSegmentationFilter crea un'istanza del filtro di segmentazione del driver ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) chiamando **IWiaItem2::GetExtension** sull'interfaccia [**IWiaItem2 passata.**](-wia-iwiaitem2.md)


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
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



 

 

---
description: Ottiene le interfacce di estensione che possono essere dotate di un driver di dispositivo Windows Image Acquisition (WIA) 2,0.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: 'Metodo IWiaItem2:: GetExtension (WIA. h)'
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
ms.openlocfilehash: 2fea4c4b9a2dd909b7ec49097ee94664b47f7e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049515"
---
# <a name="iwiaitem2getextension-method"></a>Metodo IWiaItem2:: GetExtension

Ottiene le interfacce di estensione che possono essere dotate di un driver di dispositivo Windows Image Acquisition (WIA) 2,0.

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

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Attualmente non usato. Deve essere impostato su zero.

</dd> <dt>

*bstrName* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome dell'estensione a cui l'applicazione chiamante richiede un puntatore.

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**


</dt> <dd>

Estensione del filtro di segmentazione. Si tratta attualmente dell'unico valore valido per questo parametro.

</dd> </dl> </dd> <dt>

*riidExtensionInterface* \[ in\]
</dt> <dd>

Tipo: **REFIID**

Specifica l'identificatore dell'interfaccia di estensione.

</dd> <dt>

*ppOut* \[ out\]
</dt> <dd>

Tipo: **void \* \***

Riceve l'indirizzo di un puntatore all'interfaccia di estensione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Un'applicazione richiama questo metodo per creare un oggetto di estensione che implementa una delle interfacce di estensione del driver WIA 2,0. **IWiaItem2:: GetExtension** archivia l'indirizzo dell'interfaccia di estensione dell'oggetto estensione nel parametro *riidExtensionInterface* . L'applicazione usa quindi il puntatore di interfaccia per chiamare i relativi metodi.

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *riidExtensionInterface* .

## <a name="examples"></a>Esempio

CreateSegmentationFilter crea un'istanza del filtro di segmentazione ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) del driver chiamando **IWiaItem2:: GetExtension** sull'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) passata.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 

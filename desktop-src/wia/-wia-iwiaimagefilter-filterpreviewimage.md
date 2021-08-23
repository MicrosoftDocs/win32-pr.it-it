---
description: Filtra l'immagine di anteprima.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: Metodo IWiaImageFilter::FilterPreviewImage (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 96b1d8ce92a847dcd4ffcebca6b45df2b652ad74c1216fc60b8aac72bb6a12ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659721"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a>Metodo IWiaImageFilter::FilterPreviewImage

Filtra l'immagine di anteprima.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Non usato. Impostare su 0.

</dd> <dt>

*pWiaChildItem2* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Elemento elaborato.

</dd> <dt>

*InputImageExtents* \[ Pollici\]
</dt> <dd>

Tipo: **RECT**

Coordinate (nell'area di acquisizione fisica) dell'immagine memorizzata internamente nella cache del componente di anteprima.

</dd> <dt>

*pInputStream* \[ Pollici\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Puntatore [all'interfaccia IStream](/windows/win32/api/objidl/nn-objidl-istream) per i dati dell'immagine memorizzati nella cache filtrati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Non chiamare questo metodo direttamente dall'applicazione.

*pWiaChildItem2* deve essere un elemento figlio di *pWiaItem2* passato a [**IWiaImageFilter::InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).

*InputImageExtents* è necessario perché il filtro di elaborazione delle immagini è responsabile del taglio dell'area dell'immagine che *pWiaChildItem2 rappresenta* dai dati dell'immagine passati tramite *pInputStream*.

Un'applicazione deve garantire che *pWiaChildItem2* abbia lo stesso formato di immagine (FORMATO IPA WIA), risoluzione \_ \_ (WIA \_ IPS \_ XRES e WIA IPS YRES) e profondità di bit \_ \_ (WIA \_ IPA DEPTH) di \_ *pWiaItem2* [](-wia-iwiapreview-getnewpreview.md)quando è stato passato a GetNewPreview.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 

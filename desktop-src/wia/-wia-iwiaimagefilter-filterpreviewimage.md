---
description: Filtra l'immagine di anteprima.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: 'Metodo IWiaImageFilter:: FilterPreviewImage (WIA. h)'
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
ms.openlocfilehash: 882aaf0d131ae6fe062c00c0181e2f913a0e1bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308223"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a>Metodo IWiaImageFilter:: FilterPreviewImage

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

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Non usato. Impostare su 0.

</dd> <dt>

*pWiaChildItem2* \[ in\]
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Elemento elaborato.

</dd> <dt>

_InputImageExtents * \[ in\]
</dt> <dd>

Tipo: **Rect**

Coordinate (sull'area di acquisizione fisica) dell'immagine memorizzata internamente dal componente di anteprima.

</dd> <dt>

*pInputStream* \[ in\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _

Puntatore all'interfaccia [IStream](/windows/win32/api/objidl/nn-objidl-istream) per i dati dell'immagine memorizzati nella cache che vengono filtrati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Non chiamare questo metodo direttamente dall'applicazione.

*pWiaChildItem2* deve essere un elemento figlio di *PWiaItem2* passato a [**IWiaImageFilter:: InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).

*InputImageExtents* è necessario perché il filtro di elaborazione delle immagini è responsabile del taglio dell'area immagine che *pWiaChildItem2* rappresenta dai dati dell'immagine passati attraverso *pInputStream*.

Un'applicazione deve garantire che *pWiaChildItem2* abbia lo stesso formato di immagine ( \_ formato ipa WIA \_ ), la risoluzione (WIA \_ IPS \_ XRES e WIA \_ IPS \_ YRES) e la profondità di bit (estensione \_ IPA WIA \_ ) come *pWiaItem2* aveva quando è stato passato in [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 

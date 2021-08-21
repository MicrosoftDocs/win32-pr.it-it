---
description: IWICBitmapDecoder_GetColorContexts_Proxy funzione proxy per il metodo GetColorContexts.
ms.assetid: 2a6db3bd-d3e1-4e87-a04d-0d1c3ea858fb
title: IWICBitmapDecoder_GetColorContexts_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9ffa6aa19cc16e67f19a764034376939c401d4d6cce32e7dafd02afe5c33aed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118034140"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a>Funzione proxy IWICBitmapDecoder \_ GetColorContexts \_

Funzione proxy per il [**metodo GetColorContexts.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***

Puntatore a [**questo oggetto IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)

</dd> <dt>

*cCount* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Numero di contesti di colore da recuperare.

Questo valore deve essere delle dimensioni di o inferiori alle dimensioni disponibili per *ppIColorContexts*.

</dd> <dt>

*ppIColorContexts* \[ in, out\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***

Puntatore che riceve un puntatore a [**IWICColorContext.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)

</dd> <dt>

*pcActualCount* \[ Cambio\]
</dt> <dd>

Tipo: **UINT \***

Puntatore che riceve il numero di contesti di colore contenuti nell'immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo \[ app desktop di Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 





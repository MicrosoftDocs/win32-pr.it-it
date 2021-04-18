---
description: Inizializza un IWICColorTransform con un IWICBitmapSource e lo trasforma da un IWICColorContext a un altro.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: Funzione IWICColorTransform_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorTransform_Initialize_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 29d29bfd925d979897b22711c748083b94673142
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327269"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a>IWICColorTransform \_ Inizializza la \_ funzione proxy

Inizializza un [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) con un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) e lo trasforma da un [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) a un altro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICColorTransform_Initialize_Proxy(
  _In_ IWICColorTransform    *pIColorTransform,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ IWICColorContext      *pIContextSource,
  _In_ IWICColorContext      *pIContextDest,
  _In_ REFWICPixelFormatGUID pixelFmtDest
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pIColorTransform* \[ in\]
</dt> <dd>

Tipo: **[ **IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***

Trasformazione colore da inizializzare.

</dd> <dt>

*pIBitmapSource* \[ in\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Origine della bitmap utilizzata per inizializzare la trasformazione colore.

</dd> <dt>

*pIContextSource* \[ in\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

Origine del contesto del colore.

</dd> <dt>

*pIContextDest* \[ in\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

Destinazione del contesto del colore.

</dd> <dt>

*pixelFmtDest* \[ in\]
</dt> <dd>

Tipo: **REFWICPixelFormatGUID**

GUID del formato pixel desiderato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 





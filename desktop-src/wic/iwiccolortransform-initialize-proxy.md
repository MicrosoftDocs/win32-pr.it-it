---
description: Inizializza un oggetto IWICColorTransform con un oggetto IWICBitmapSource e lo trasforma da un oggetto IWICColorContext a un altro.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: IWICColorTransform_Initialize_Proxy funzione
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
ms.openlocfilehash: fcfe124d03e9ad41edb49554613bc18b2cd15818b3f52db7ca368e27f5c4fcc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841371"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a>Funzione proxy di inizializzazione IWICColorTransform \_ \_

Inizializza un [**oggetto IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) con [**un oggetto IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) e lo trasforma da [**un oggetto IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) a un altro.

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

*pIColorTransform* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***

Trasformazione del colore da inizializzare.

</dd> <dt>

*pIBitmapSource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Origine bitmap utilizzata per inizializzare la trasformazione del colore.

</dd> <dt>

*pIContextSource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

Origine del contesto del colore.

</dd> <dt>

*pIContextDest* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

Destinazione del contesto del colore.

</dd> <dt>

*pixelFmtDest* \[ Pollici\]
</dt> <dd>

Tipo: **REFWICPixelFormatGUID**

GUID del formato pixel desiderato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>WindowsCodecsExt.dll</dt> </dl> |



 

 





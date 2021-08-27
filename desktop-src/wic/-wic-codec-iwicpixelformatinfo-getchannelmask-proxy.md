---
description: Funzione proxy per il metodo GetChannelMask.
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: IWICPixelFormatInfo_GetChannelMask_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ee200dddf0b2cd736ca2ad435b63e774076465ad3d1f6215f1c558f1abb6c194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056601"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a>Funzione proxy IWICPixelFormatInfo \_ GetChannelMask \_

Funzione proxy per il [**metodo GetChannelMask.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\***

Puntatore a [**questo oggetto IWICPixelFormatInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)

</dd> <dt>

*uiChannelIndex* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Indice della channel mask da recuperare.

</dd> <dt>

*cbMaskBuffer* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Dimensioni del buffer *pbMaskBuffer.*

</dd> <dt>

*pbMaskBuffer* \[ in, out\]
</dt> <dd>

Tipo: **\* BYTE**

Puntatore al buffer della maschera.

</dd> <dt>

*pcbActual* \[ Cambio\]
</dt> <dd>

Tipo: **UINT \***

Dimensioni effettive del buffer necessarie per ottenere la maschera del canale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo \[ app desktop vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 





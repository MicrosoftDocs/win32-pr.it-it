---
description: Funzione proxy per il metodo GetDeviceModels.
ms.assetid: de8f91f7-fef7-48bc-94fc-34c43175248b
title: IWICBitmapCodecInfo_GetDeviceModels_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceModels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 659ca401384f907e0bad1a86dd79e61bad55cf2612bb45713246b26711e57d9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711987"
---
# <a name="iwicbitmapcodecinfo_getdevicemodels_proxy-function"></a>Funzione proxy IWICBitmapCodecInfo \_ GetDeviceModels \_

Funzione proxy per il [**metodo GetDeviceModels.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceModels_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceModels,
  _Inout_ WCHAR               *wzDeviceModels,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***

Puntatore a [**questo oggetto IWICBitmapCodecInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)

</dd> <dt>

*cchDeviceModels* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Dimensioni del buffer dei modelli di dispositivo.

</dd> <dt>

*wzDeviceModels* \[ in, out\]
</dt> <dd>

Tipo: **WCHAR \***

Puntatore che riceve un elenco delimitato da virgole dei nomi dei modelli di dispositivo associati al codec.

</dd> <dt>

*pcchActual* \[ in, out\]
</dt> <dd>

Tipo: **UINT \***

Dimensioni effettive del buffer necessarie per recuperare tutti i nomi dei modelli di dispositivo.

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



 

 





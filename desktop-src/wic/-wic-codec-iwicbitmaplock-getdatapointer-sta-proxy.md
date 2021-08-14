---
description: Funzione proxy per il metodo GetDataPointer.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: IWICBitmapLock_GetDataPointer_STA_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetDataPointer_STA_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b693c78ba3a3d7c68c33f68ec1494997536ffb10272cc384d89d9e94ded7145b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206747"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a>Funzione proxy IWICBitmapLock \_ GetDataPointer \_ STA \_

Funzione proxy per il [**metodo GetDataPointer.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\***

Puntatore a [**questo oggetto IWICBitmapLock.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)

</dd> <dt>

*pcbBufferSize* \[ Cambio\]
</dt> <dd>

Tipo: **UINT \***

Puntatore che riceve le dimensioni del buffer.

</dd> <dt>

*ppbData* \[ Cambio\]
</dt> <dd>

Tipo: **\* \* BYTE**

Puntatore che riceve un puntatore al pixel superiore sinistro nel rettangolo bloccato.

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



 

 





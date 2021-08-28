---
description: Windows Funzione proxy WIC (Imaging Component) per IEnumString::Reset.
ms.assetid: 084a3de0-c6de-4ce2-ba78-5d1bacb56cb0
title: IEnumString_Reset_WIC_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Reset_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0fc06a00b5e80befe1e6a69f7c2b402597699c97bf866129ca10175e18fe34a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549621"
---
# <a name="ienumstring_reset_wic_proxy-function"></a>Funzione proxy \_ IEnumString Reset \_ WIC \_

Windows Funzione proxy WIC (Imaging Component) per IEnumString::Reset.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IEnumString_Reset_WIC_Proxy(
  _In_  IEnumString *THIS_PTR,
  _In_  ULONG       celt,
  _Out_ LPOLESTR    *rgelt,
  _Out_ ULONG       *pceltFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **IEnumString \***

PARAMDESC

</dd> <dt>

*celt* \[ Pollici\]
</dt> <dd>

Tipo: **ULONG**

</dd> <dt>

*rgelt* \[ Cambio\]
</dt> <dd>

Tipo: **LPOLESTR \***

</dd> <dt>

*pceltFetched* \[ Cambio\]
</dt> <dd>

Tipo: **ULONG \***

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo app desktop di Vista \[\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 





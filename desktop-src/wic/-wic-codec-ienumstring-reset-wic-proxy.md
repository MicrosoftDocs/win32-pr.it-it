---
description: 'Funzione proxy di Windows Imaging Component (WIC) per IEnumString:: Reset.'
ms.assetid: 084a3de0-c6de-4ce2-ba78-5d1bacb56cb0
title: Funzione IEnumString_Reset_WIC_Proxy
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
ms.openlocfilehash: 64057e0f49b105232f980ac3d73014156e2da732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306687"
---
# <a name="ienumstring_reset_wic_proxy-function"></a>IEnumString \_ Reimposta \_ la \_ funzione proxy WIC

Funzione proxy di Windows Imaging Component (WIC) per IEnumString:: Reset.

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

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **IEnumString \** _

PARAMDESC

</dd> <dt>

_celt * \[ in\]
</dt> <dd>

Tipo: **ULONG**

</dd> <dt>

*rgelt* \[ out\]
</dt> <dd>

Tipo: **LPOLESTR \** _

</dd> <dt>

_pceltFetched * \[ out\]
</dt> <dd>

Tipo: **ULONG \** _

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, \[ solo app desktop di Windows Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 





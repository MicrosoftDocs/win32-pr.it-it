---
description: Funzione proxy per il metodo GetDataPointer.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: Funzione IWICBitmapLock_GetDataPointer_STA_Proxy
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
ms.openlocfilehash: 957ae5974d65430bd39ea41f2e094e9f9c7efb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319128"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a>\_ \_ Funzione proxy sta IWICBitmapLock GetDataPointer \_

Funzione proxy per il metodo [**GetDataPointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) .

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

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _

Puntatore a questo oggetto [_ *IWICBitmapLock* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .

</dd> <dt>

*pcbBufferSize* \[ out\]
</dt> <dd>

Tipo: **uint \** _

Puntatore che riceve le dimensioni del buffer.

</dd> <dt>

_ppbData * \[ out\]
</dt> <dd>

Tipo: **byte \* \***

Puntatore che riceve un puntatore al pixel superiore sinistro nel rettangolo bloccato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, \[ solo app desktop di Windows Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 





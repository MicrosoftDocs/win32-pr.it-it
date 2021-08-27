---
description: Non implementato e non può essere usato.
ms.assetid: b41ba894-5cee-458d-935f-e89363925968
title: Funzione SslChangeNotify (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslChangeNotify
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ff8bd1d23315894a3e858a536d10883f2fedcced792575157de824c02f3217ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907181"
---
# <a name="sslchangenotify-function"></a>Funzione SslChangeNotify

La **funzione SslChangeNotify** non è implementata e non può essere usata.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslChangeNotify(
  _In_ HANDLE hEvent,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hEvent* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **NTE \_ NOT \_ SUPPORTED**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 





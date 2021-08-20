---
description: Specifica se uno stile diverso dal colore ha uno stile di sottolineatura.
ms.assetid: 452dda6e-b12b-457c-9a01-c5363359c9f5
title: Funzione FUlIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c53e48fbf2c607ee8a99c4f952cdb1bf9056826def452c42283dfd615392c4ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956100"
---
# <a name="fulimestyle-function"></a>Funzione FUlIMEStyle

Specifica se uno stile diverso dal colore ha uno stile di sottolineatura.

## <a name="syntax"></a>Sintassi


```C++
BOOL __cdecl FUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pimestyle* \[ Pollici\]
</dt> <dd>

Struttura **IMESTYLE** restituita dalla [**funzione PIMEStyleFromAttr.**](pimestylefromattr.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

TRUE se lo stile ha uno stile di sottolineatura.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 

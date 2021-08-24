---
description: Specifica se uno stile non a colori ha lo stile corsivo.
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: Funzione FItalicIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FItalicIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c8160edf46b97544ef27558bf15a8a58e447e78a0e0709432aea840f4567bc0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076115"
---
# <a name="fitalicimestyle-function"></a>Funzione FItalicIMEStyle

Specifica se uno stile non a colori ha lo stile corsivo.

## <a name="syntax"></a>Sintassi


```C++
BOOL __cdecl FItalicIMEStyle(
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

**TRUE** se lo stile ha lo stile corsivo.

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

 

 

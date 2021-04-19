---
description: Specifica se uno stile non colore presenta lo stile corsivo.
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: FItalicIMEStyle (funzione)
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
ms.openlocfilehash: 828e701773d666830473e92afc73f80ccdae3bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329980"
---
# <a name="fitalicimestyle-function"></a>FItalicIMEStyle (funzione)

Specifica se uno stile non colore presenta lo stile corsivo.

## <a name="syntax"></a>Sintassi


```C++
BOOL __cdecl FItalicIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pimestyle* \[ in\]
</dt> <dd>

Struttura **IMESTYLE** restituita dalla funzione [**PIMEStyleFromAttr**](pimestylefromattr.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**True** se lo stile ha lo stile corsivo.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 

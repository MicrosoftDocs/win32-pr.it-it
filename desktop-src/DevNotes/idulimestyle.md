---
description: Indica se lo stile non colore specificato presenta sottolineatura.
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: IdUlIMEStyle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330964"
---
# <a name="idulimestyle-function"></a>IdUlIMEStyle (funzione)

Indica se lo stile non colore specificato presenta sottolineatura.

## <a name="syntax"></a>Sintassi


```C++
UINT __cdecl IdUlIMEStyle(
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

Questa funzione può restituire uno dei valori seguenti.

<dl> <dt>

**IMESTY \_ UL \_ min** (2002)
</dt> <dt>

**IMESTY \_ UL \_ None** (2002)
</dt> <dt>

**IMESTY \_ UL \_ singolo** (2003)
</dt> <dt>

**IMESTY \_ UL \_ punteggiato** (2005)
</dt> <dt>

**IMESTY \_ \_Spessore UL** (2006)
</dt> <dt>

**IMESTY \_ UL \_ inferiore** (2011)
</dt> <dt>

**IMESTY \_ UL \_ THICKLOWER** (2012)
</dt> <dt>

**IMESTY \_ UL \_ THICKDITHLOWER** (2013)
</dt> <dt>

**IMESTY \_ UL \_ DITHLOWER** (2014)
</dt> <dt>

**IMESTY \_ UL \_ Max** (2014)
</dt> </dl>

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

 

 

---
description: Recupera lo stile del colore del testo dello stile specificato.
ms.assetid: 242c37af-5b39-4b18-9c8f-4e692f41c497
title: Funzione PColorStyleTextFromIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleTextFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 58fb2c2830f016080ac27c48b188bbd1948406a6cb7516b3279c411c87d9c155
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955720"
---
# <a name="pcolorstyletextfromimestyle-function"></a>Funzione PColorStyleTextFromIMEStyle

Recupera lo stile del colore del testo dello stile specificato.

## <a name="syntax"></a>Sintassi


```C++
const IMECOLORSTY* __cdecl PColorStyleTextFromIMEStyle(
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

Puntatore a una **struttura IMECOLORSTY** che rappresenta lo stile del colore del testo.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

La **struttura IMECOLORSTY** è definita come segue:

``` syntax
typedef struct {
    UINT colorId;
    union {
        COLORREF    rgb;
        UINT        colorWin;
        UINT        colorSpec;
        UINT        colorFund;
    };
} IMECOLORSTY;
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 

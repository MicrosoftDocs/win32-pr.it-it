---
description: Specifica se il colore specificato è un colore fondamentale.
ms.assetid: 9a06fadc-9b97-4f7d-9488-688b72d14bc5
title: Funzione FFundamentalIMEColorStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FFundamentalIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 8923da89872b5abbd7849b530bca2e13022247f3633444d0c000cffce017ecd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827482"
---
# <a name="ffundamentalimecolorstyle-function"></a>Funzione FFundamentalIMEColorStyle

Specifica se il colore specificato è un colore fondamentale.

## <a name="syntax"></a>Sintassi


```C++
BOOL __cdecl FFundamentalIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcolorstyle* \[ Pollici\]
</dt> <dd>

Struttura **IMECOLORSTY** restituita dalla [**funzione PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) [**o PColorStyleTextFromIMEStyle.**](pcolorstyletextfromimestyle.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** quando il colore è un colore fondamentale.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md)
</dt> <dt>

[**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 

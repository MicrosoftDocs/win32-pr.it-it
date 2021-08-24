---
description: Specifica se il colore specificato è un colore speciale.
ms.assetid: fda856c4-37b9-444f-9c54-d9eb848a4b05
title: Funzione FSpecialIMEColorStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 7922f60d347a91b461031d1a56cc51b9630389e99fbef778a8f75007b17f1558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795171"
---
# <a name="fspecialimecolorstyle-function"></a>Funzione FSpecialIMEColorStyle

Specifica se il colore specificato è un colore speciale.

## <a name="syntax"></a>Sintassi


```C++
BOOL __cdecl FSpecialIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcolorstyle* \[ Pollici\]
</dt> <dd>

Struttura **IMECOLORSTY** restituita da una [**funzione PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle.**](pcolorstyletextfromimestyle.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** quando il colore è un colore speciale.

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

 

 

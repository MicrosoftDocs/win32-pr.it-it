---
description: Specifica se il colore specificato è un colore RGB.
ms.assetid: 16b48644-c2d5-4383-836a-122f44504638
title: Funzione FRGBIMEColorStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRGBIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 135a53a6c531d14f03aa2bc944e076f51ec28c167bced94cc0675fe2ae7642ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404665"
---
# <a name="frgbimecolorstyle-function"></a>Funzione FRGBIMEColorStyle

Specifica se il colore specificato è un colore RGB.

## <a name="syntax"></a>Sintassi


```C++
BOOL __cdecl FRGBIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcolorstyle* \[ Pollici\]
</dt> <dd>

Struttura **IMECOLORSTY** restituita da una [**funzione PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) [**o PColorStyleTextFromIMEStyle.**](pcolorstyletextfromimestyle.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** quando il colore è un colore RGB.

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

 

 

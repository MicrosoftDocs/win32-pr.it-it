---
description: Specifica se il colore specificato è un colore di testo speciale.
ms.assetid: 527806f5-5046-48b0-a8db-86a5b8c0db08
title: Funzione FSpecialTextIMEColorStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialTextIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 6fa964ba5d1020a5d9ba35b7359d81d965778b8a1e1f546a0a6cac19d2611ebd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017729"
---
# <a name="fspecialtextimecolorstyle-function"></a>Funzione FSpecialTextIMEColorStyle

Specifica se il colore specificato è un colore di testo speciale.

## <a name="syntax"></a>Sintassi


```C++
BOOL __cdecl FSpecialTextIMEColorStyle(
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

Restituisce **TRUE** quando il colore è un colore di testo speciale.

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

 

 

---
description: Specifica se il colore specificato è un colore del testo speciale.
ms.assetid: 527806f5-5046-48b0-a8db-86a5b8c0db08
title: FSpecialTextIMEColorStyle (funzione)
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
ms.openlocfilehash: cfaf83aeb2fcb03ab61c1280ec821174117026fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326580"
---
# <a name="fspecialtextimecolorstyle-function"></a>FSpecialTextIMEColorStyle (funzione)

Specifica se il colore specificato è un colore del testo speciale.

## <a name="syntax"></a>Sintassi


```C++
BOOL __cdecl FSpecialTextIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcolorstyle* \[ in\]
</dt> <dd>

Struttura **IMECOLORSTY** restituita da una funzione [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) o [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** quando il colore è un colore del testo speciale.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

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

 

 

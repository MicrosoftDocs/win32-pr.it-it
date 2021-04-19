---
description: La funzione ValidateBitmapInfoHeader verifica una struttura BITMAPINFOHEADER per determinati errori comuni che possono causare sovraccarichi del buffer o overflow di Integer.
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: Funzione ValidateBitmapInfoHeader (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateBitmapInfoHeader
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: c7242778a2ff16414b07f887dc1e71a1547a88e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333300"
---
# <a name="validatebitmapinfoheader-function"></a>ValidateBitmapInfoHeader (funzione)

La `ValidateBitmapInfoHeader` funzione verifica una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) per determinati errori comuni che possono causare sovraccarichi del buffer o overflow di Integer.

> [!Note]  
> Questa funzione non garantisce che la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) sia valida o che il codice che usa la struttura sia protetto.

 

## <a name="syntax"></a>Sintassi


```C++
BOOL ValidateBitmapInfoHeader(
   const BITMAPINFOHEADER *pbmi,
         DWORD            cbSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbmi* 
</dt> <dd>

Puntatore alla struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) da convalidare.

</dd> <dt>

*cbSize* 
</dt> <dd>

Dimensioni in byte del blocco di memoria che include la struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano. Se il valore è **false**, la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) non è valida.

## <a name="remarks"></a>Commenti

Questa funzione protegge gli errori seguenti:

-   Overflow aritmetico nelle dimensioni della struttura o di una struttura non valida.
-   Valore non valido per il membro **biClrUsed** .
-   Overflow aritmetico nelle dimensioni dell'immagine (**biSizeImage**).
-   Valori non validi per la dimensione dell'immagine (**biSizeImage**) per i formati RGB.

La funzione non controlla se la struttura descrive un formato video valido.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni video e immagine](video-and-image-functions.md)
</dt> </dl>

 

 





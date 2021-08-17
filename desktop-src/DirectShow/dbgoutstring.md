---
description: La funzione DbgOutString invia una stringa al percorso di output di debug. Ignorato nelle build per la vendita al dettaglio.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: Funzione DbgOutString (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6d8b74b5f0643f619a58beeea2dcd5526889d1a65de4815b06d2d6047777d90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821559"
---
# <a name="dbgoutstring-function"></a>Funzione DbgOutString

La **funzione DbgOutString** invia una stringa al percorso di output di debug. Ignorato nelle build per la vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Psz* 
</dt> <dd>

Stringa da visualizzare nell'output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Nelle build di debug questa funzione restituisce sempre la stringa, indipendentemente dal livello di output di debug corrente. Per un controllo più dettagliato sull'output, usare la macro [**DbgLog.**](dbglog.md)

## <a name="examples"></a>Esempio


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 





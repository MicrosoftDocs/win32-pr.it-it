---
description: La funzione DbgSetModuleLevel imposta il livello di registrazione per uno o più tipi di messaggio. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: Funzione DbgSetModuleLevel (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d6623793b150c600eb00f0c0843dd72c68deb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327520"
---
# <a name="dbgsetmodulelevel-function"></a>DbgSetModuleLevel (funzione)

La funzione **DbgSetModuleLevel** imposta il livello di registrazione per uno o più tipi di messaggio. Ignorato nelle compilazioni al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void DbgSetModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tipi* 
</dt> <dd>

Combinazione bit per bit di uno o più tipi di messaggio.

</dd> <dt>

*Level* 
</dt> <dd>

Livello di registrazione per i tipi di messaggio specificati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 





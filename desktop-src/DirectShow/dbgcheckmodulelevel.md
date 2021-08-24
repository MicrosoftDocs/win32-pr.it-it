---
description: La funzione DbgCheckModuleLevel controlla se la registrazione è abilitata per i tipi di messaggio e il livello specificati. Ignorato nelle build di vendita al dettaglio.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: Funzione DbgCheckModuleLevel (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd6d7c61e7989987401c22386054c02f87410ce66dbb98bb6e20a813f2c851be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823701"
---
# <a name="dbgcheckmodulelevel-function"></a>Funzione DbgCheckModuleLevel

La `DbgCheckModuleLevel` funzione controlla se la registrazione è abilitata per i tipi di messaggio e il livello specificati. Ignorato nelle build di vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
BOOL DbgCheckModuleLevel(
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

Livello di registrazione

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se la registrazione per uno dei tipi di messaggio specificati è impostata sul livello specificato o su un livello superiore. In caso contrario, restituisce **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 





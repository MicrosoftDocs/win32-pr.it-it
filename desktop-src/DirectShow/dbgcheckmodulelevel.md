---
description: La funzione DbgCheckModuleLevel controlla se la registrazione è abilitata per i tipi di messaggio e il livello specificati. Ignorato nelle compilazioni al dettaglio.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: Funzione DbgCheckModuleLevel (Wxdebug. h)
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
ms.openlocfilehash: 79df8cd06617cf9b17fa9933d4d7a87954a6e2b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332693"
---
# <a name="dbgcheckmodulelevel-function"></a>DbgCheckModuleLevel (funzione)

La `DbgCheckModuleLevel` funzione controlla se la registrazione è abilitata per i tipi di messaggio e il livello specificati. Ignorato nelle compilazioni al dettaglio.

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

Restituisce **true** se la registrazione per uno dei tipi di messaggio specificati è impostata sul livello specificato o su un valore superiore. In caso contrario, restituisce **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 





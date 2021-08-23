---
description: La macro DbgLog invia una stringa al percorso di output di debug, se la registrazione è abilitata per il tipo e il livello specificati. Questa macro viene ignorata nelle build di vendita al dettaglio.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: Macro DbgLog (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLog
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 619a3cd277425b555bc64139c3e59c959cc6abd19d6da22c2129830c38496a24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953340"
---
# <a name="dbglog-macro"></a>Macro DbgLog

La macro **DbgLog** invia una stringa al percorso di output di debug, se la registrazione è abilitata per il tipo e il livello specificati. Questa macro viene ignorata nelle build di vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void DbgLog(
         DWORD Types,
         DWORD Level,
   const TCHAR *pFormat,
               ...
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

Livello di registrazione per questo messaggio.

</dd> <dt>

*pFormat* 
</dt> <dd>

Stringa di formato di tipo **printf.**

</dd> <dt>

*...* 
</dt> <dd>

Argomenti aggiuntivi per la stringa di formato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="remarks"></a>Commenti

Se la registrazione di debug per uno dei tipi di messaggio è impostata sul livello specificato o su un livello superiore, questa macro invia la stringa formattata al percorso di output del debug.

La macro aggiunge automaticamente un carattere di nuova riga alla stringa di output.

> [!Note]  
> Un set aggiuntivo di parentesi deve includere i parametri della macro:

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 





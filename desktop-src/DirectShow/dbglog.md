---
description: La macro DbgLog invia una stringa al percorso di output di debug, se la registrazione è abilitata per il tipo e il livello specificati. Questa macro viene ignorata nelle compilazioni al dettaglio.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: Macro DbgLog (Wxdebug. h)
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
ms.openlocfilehash: 1cd3f4e53c61fef1f030f654bbb0363cd7c97381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327523"
---
# <a name="dbglog-macro"></a>DbgLog (macro)

La macro **DbgLog** invia una stringa al percorso di output di debug, se la registrazione è abilitata per il tipo e il livello specificati. Questa macro viene ignorata nelle compilazioni al dettaglio.

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

Stringa di formato in stile **printf** .

</dd> <dt>

*...* 
</dt> <dd>

Argomenti aggiuntivi per la stringa di formato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="remarks"></a>Commenti

Se la registrazione del debug per uno dei tipi di messaggio è impostata sul livello specificato o su un valore superiore, questa macro invia la stringa formattata al percorso di output di debug.

La macro aggiunge automaticamente un carattere di nuova riga alla stringa di output.

> [!Note]  
> Un set aggiuntivo di parentesi deve racchiudere i parametri della macro:

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di output di debug](debug-output-functions.md)
</dt> </dl>

 

 





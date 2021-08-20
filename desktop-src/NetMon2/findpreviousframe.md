---
description: La funzione FindPreviousFrame trova il frame precedente nel contesto di acquisizione corrente che corrisponde al filtro.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: Funzione FindPreviousFrame (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPreviousFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a3bd6378691b63fc7f4db2455f713ffd0cf2a0281da2411dc494244ad3f00ba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982528"
---
# <a name="findpreviousframe-function"></a>Funzione FindPreviousFrame

La **funzione FindPreviousFrame** trova il frame precedente nel contesto di acquisizione corrente che corrisponde al filtro.

## <a name="syntax"></a>Sintassi


```C++
HFRAME WINAPI FindPreviousFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     LowestFrame
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCurrentFrame* 
</dt> <dd>

Handle per il frame.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

Nome del protocollo, ad esempio TCP.

</dd> <dt>

*DestinationAddress* 
</dt> <dd>

Indirizzo di destinazione del frame cercato.

</dd> <dt>

*SourceAddress* 
</dt> <dd>

Indirizzo di origine del frame cercato.

</dd> <dt>

*ProtocolOffset* 
</dt> <dd>

Puntatore a **un oggetto WORD** che riceve l'offset del protocollo.

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

Punto di partenza della ricerca. Per impostazione predefinita, questa funzione cerca 1.000 fotogrammi indietro dal *punto di partenza OriginalFrameNumber.* È possibile modificare la distanza di ricerca indietro aggiungendo questa riga al file Nmapi.ini, che si trova nella \\ directory Network Monitor.

MAXLOOKBACK=<new lookback distance>

</dd> <dt>

*LowestFrame* 
</dt> <dd>

Numero di fotogramma più basso nell'acquisizione in cui viene cercata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle per il frame precedente.

Se la funzione non ha esito positivo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

Il filtro di acquisizione viene definito principalmente da *ProtocolName,* che è l'unico input del filtro richiesto. è possibile aggiungere *le informazioni DestinationAddress* e *SourceAddress* per aumentare la velocità di acquisizione.

*ProtocolOffset* viene restituito al parser chiamante, che aggiunge questo **valore DWORD** al puntatore restituito bloccando il frame (con [ParserTemporaryLockFrame](parsertemporarylockframe.md)) per ottenere l'LPBYTE del protocollo cercato. In caso di restituzione, l'HFRAME che ha passato il filtro viene assegnato al parser. Se il parser rileva che il frame non è quello cercato, il parser può tornare alla funzione **FindPreviousFrame** per recuperare il frame successivo. Gli indirizzi di origine e di destinazione, che non sono obbligatori, possono essere passati come **NULL.** Se usati, questi indirizzi possono essere di tipo INDIRIZZO \_ TIPO IP e così \_ via, non solo tipi MAC.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





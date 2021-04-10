---
description: La funzione FindPreviousFrame trova il frame precedente nel contesto di acquisizione corrente che corrisponde al filtro.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: Funzione FindPreviousFrame (Netmon. h)
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
ms.openlocfilehash: deabf10702ca41c23101c5f60c9459e094e567fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966477"
---
# <a name="findpreviousframe-function"></a>FindPreviousFrame (funzione)

La funzione **FindPreviousFrame** trova il frame precedente nel contesto di acquisizione corrente che corrisponde al filtro.

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

Puntatore a una **parola** che riceve l'offset del protocollo.

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

Punto iniziale della ricerca. Per impostazione predefinita, questa funzione esegue la ricerca all'indietro dei frame 1.000 dal punto di partenza del *OriginalFrameNumber* . È possibile modificare la distanza di ricerca aggiungendo questa riga al file Nmapi.ini, che si trova nella \\ directory Network Monitor.

MAXLOOKBACK =<new lookback distance>

</dd> <dt>

*LowestFrame* 
</dt> <dd>

Numero di frame più basso nell'acquisizione in cui viene eseguita la ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle per il frame precedente.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Il filtro di acquisizione è definito principalmente da *ProtocolName*, che è l'unico input di filtro necessario; è possibile aggiungere informazioni su *DestinationAddress* e *sourceAddress* per aumentare la velocità di acquisizione.

*ProtocolOffset* viene restituito al parser chiamante, che aggiunge questo **DWORD** al puntatore restituito bloccando il frame (con [PARSERTEMPORARYLOCKFRAME](parsertemporarylockframe.md)) per ottenere il LPBYTE del protocollo di cui viene eseguita la ricerca. Al ritorno, il HFRAME che ha superato il filtro viene assegnato al parser. Se il parser rileva che il frame non è quello cercato, il parser può restituire questo HFRAME alla funzione **FindPreviousFrame** per recuperare il frame successivo. Gli indirizzi di origine e di destinazione, che non sono obbligatori, possono essere passati come **null**. Se utilizzati, questi indirizzi possono essere di tipo indirizzo \_ \_ IP e così via, non solo i tipi Mac.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





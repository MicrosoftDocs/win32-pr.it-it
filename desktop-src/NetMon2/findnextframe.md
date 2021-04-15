---
description: Trova il frame successivo nel contesto di acquisizione corrente che corrisponde al filtro.
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: Funzione FindNextFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2e303f7f9031ad451ad19be8bc8cbcd3abae3f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525152"
---
# <a name="findnextframe-function"></a>FindNextFrame (funzione)

La funzione **FindNextFrame** trova il frame successivo nel contesto di acquisizione corrente che corrisponde al filtro.

## <a name="syntax"></a>Sintassi


```C++
HFRAME WINAPI FindNextFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     HighestFrame
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

Indirizzo di destinazione.

</dd> <dt>

*SourceAddress* 
</dt> <dd>

Indirizzo di origine.

</dd> <dt>

*ProtocolOffset* 
</dt> <dd>

Puntatore a una **parola** che riceverà l'offset del protocollo.

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

Punto iniziale della ricerca. Per impostazione predefinita, questa funzione Cerca i frame 1.000 dal punto di partenza del *OriginalFrameNumber* . Per modificare la distanza di avanzamento della ricerca, aggiungere questa riga al file Nmapi.ini, che si trova nella \\ directory Network Monitor.

MAXLOOKBACK =<new lookforward distance>

</dd> <dt>

*HighestFrame* 
</dt> <dd>

Numero di frame più elevato nell'acquisizione in cui viene eseguita la ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle per il frame successivo.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Il filtro di acquisizione viene definito principalmente dal parametro *ProtocolName* , che è l'unico input di filtro necessario; è possibile aggiungere i dati *DestinationAddress* e *sourceAddress* per aumentare la velocità di acquisizione.

Il puntatore *ProtocolOffset* viene restituito al parser chiamante, che aggiunge la **parola** al puntatore restituito bloccando il frame (con [ParserTemporaryLockFrame](parsertemporarylockframe.md)) per ottenere l' **LPBYTE** del protocollo cercato. Al ritorno, il HFRAME che ha superato il filtro viene assegnato al parser. Se il parser rileva che questo frame non è quello cercato, il parser può restituire il HFRAME alla funzione **FindNextFrame** per ottenere il frame successivo. Gli indirizzi di origine e di destinazione non sono obbligatori e possono essere passati come **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





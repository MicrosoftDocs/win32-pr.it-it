---
description: La funzione di esportazione RecognizeFrame indica se una parte di dati viene riconosciuta come protocollo rilevato dal parser. La funzione di esportazione RecognizeFrame deve essere implementata per ogni parser che supporta la DLL del parser.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: Funzione di callback RecognizeFrame (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizeFrame
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: b9f8fcbfccdb306038b7b654e947ff1a11654267012c7527799d8633ed8a9410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889701"
---
# <a name="recognizeframe-callback-function"></a>Funzione di callback RecognizeFrame

La funzione di esportazione **RecognizeFrame** indica se una parte di dati viene riconosciuta come protocollo rilevato dal parser. La **funzione di esportazione RecognizeFrame** deve essere implementata per ogni parser che supporta la DLL del parser.

## <a name="syntax"></a>Sintassi


```C++
LPBYTE RecognizeFrame(
  _In_    HFRAME      hFrame,
  _In_    LPBYTE      lpFrame,
  _In_    LPBYTE      lpProtocol,
  _In_    DWORD       MacType,
  _In_    DWORD       BytesLeft,
  _In_    HPROTOCOL   hPreviousProtocol,
  _In_    DWORD       nPreviousProtocolOffset,
  _Out_   LPDWORD     ProtocolStatusCode,
  _Out_   LPHPROTOCOL phNextProtocol,
  _Inout_ PDWORD_PTR  lpInstData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ Pollici\]
</dt> <dd>

Handle per il frame che contiene i dati.

</dd> <dt>

*lpFrame* \[ Pollici\]
</dt> <dd>

Puntatore al primo byte di un frame. Il puntatore consente di visualizzare i dati che altri parser riconoscono.

</dd> <dt>

*lpProtocol* \[ Pollici\]
</dt> <dd>

Puntatore all'inizio dei dati non reclamati. In genere, i dati non dichiarati si trovano al centro di un frame perché un parser precedente ha richiesto i dati prima di questo parser. Il parser deve prima testare i dati non reclamati.

</dd> <dt>

*MacType* \[ Pollici\]
</dt> <dd>

Valore MAC del primo protocollo in un frame. In genere, *il valore MacType* viene usato quando il parser deve identificare il primo protocollo in un frame. Il *valore MacType* può essere uno dei seguenti:



| Valore                                                                                                                                                                         | Significato                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**TIPO \_ MAC \_ ETHERNET**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**TOKENRING \_ DI TIPO MAC \_**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**MAC \_ TYPE \_ FDDI**</dt> </dl>                | ANSI X3T9.5 <br/> |



 

</dd> <dt>

*BytesLeft* \[ Pollici\]
</dt> <dd>

Numero rimanente di byte da una posizione in un frame alla fine del frame.

</dd> <dt>

*hPreviousProtocol* \[ Pollici\]
</dt> <dd>

Handle del protocollo precedente.

</dd> <dt>

*nPreviousProtocolOffset* \[ Pollici\]
</dt> <dd>

Offset dell'inizio precedente del protocollo del frame.

</dd> <dt>

*ProtocolStatusCode* \[ Cambio\]
</dt> <dd>

Indicatore di stato del protocollo. La DLL del parser deve impostare uno dei codici di stato seguenti.



| Valore                                                                                                                                                                                                              | Significato                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <dt>**STATO \_ DEL PROTOCOLLO \_ RICONOSCIUTO**</dt> </dl>              | Il parser riconosce i dati, ma non sa quale protocollo segue. Dopo aver impostato il codice, restituire un puntatore ai dati rimanenti non reclamati che seguono il protocollo riconosciuto. Network Monitor usa il [*set di protocolli*](f.md) seguente per continuare l'analisi. <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <dt>**STATO \_ DEL PROTOCOLLO NON \_ \_ RICONOSCIUTO**</dt> </dl> | Il parser non riconosce i dati. Dopo aver impostato questo codice, restituire il puntatore all'inizio dei dati usando il puntatore passato dal parametro *lpProtocol* alla DLL del parser. Network Monitor usa il *set seguente* del protocollo precedente per continuare l'analisi. <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <dt>**STATO \_ DEL \_ PROTOCOLLO RICHIESTO**</dt> </dl>                       | Il parser riconosce i dati e dichiara i dati rimanenti. Dopo aver impostato il codice, restituire **NULL** per Network Monitor terminare l'analisi di un frame. <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <dt>**PROTOCOLLO \_ STATO \_ PROTOCOLLO \_ SUCCESSIVO**</dt> </dl>    | Il parser riconosce i dati e sa quale protocollo segue. Dopo aver impostato il codice, impostare il *parametro phNextProtocol* e restituire un puntatore ai dati rimanenti non reclamati che seguono il protocollo riconosciuto. Network Monitor continua l'analisi del frame. <br/>                               |



 

</dd> <dt>

*phNextProtocol* \[ Cambio\]
</dt> <dd>

Puntatore all'handle del protocollo successivo. Questo parametro viene impostato quando un protocollo identifica il protocollo che segue un protocollo. Per ottenere l'handle del protocollo successivo, chiamare la [funzione GetProtocolFromTable.](getprotocolfromtable.md)

</dd> <dt>

*lpInstData* \[ in, out\]
</dt> <dd>

Nell'input, puntatore ai dati dell'istanza del protocollo precedente.

Nell'output, puntatore ai dati dell'istanza per il protocollo corrente. La lunghezza dei dati dell'istanza non può essere maggiore di \_ un valore DWORD PTR.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore al primo byte dopo i dati del parser riconosciuti. Se il parser dichiara tutti i dati rimanenti, il valore restituito è **NULL.**

Se la funzione ha esito negativo, il valore restituito è un puntatore iniziale passato dal parametro *lpProtocol.*

## <a name="remarks"></a>Commenti

La **funzione RecognizeFrame** determina se il parser riconosce i dati non elaborati a partire dal puntatore *lpProtocol.*

-   Se il protocollo riconosce i dati, la funzione **RecognizeFrame** restituisce un puntatore ai dati rimanenti o **NULL** se il protocollo corrente è l'ultimo protocollo in un frame.
-   Se il protocollo non riconosce i dati, la funzione **RecognizeFrame** restituisce il puntatore passato alla DLL del parser nel *parametro lpProtocol.*

> [!Note]  
> *È possibile chiamare RecognizeFrame* prima che venga [*chiamata la funzione Register*](register-parser.md) per registrare le proprietà del protocollo. Per questo motivo, l'implementazione della funzione *RecognizeFrame* non si basa su proprietà o strutture create o inizializzate durante l'implementazione della funzione **Register del** protocollo.

 

**Handoff Set e Follow Set**

Un parser può usare un set di handoff o seguire un set per identificare Network Monitor protocollo che segue i dati riconosciuti.

-   Se le informazioni sono disponibili nei dati riconosciuti, il parser usa il relativo set di handoff per ottenere un handle per il protocollo successivo e quindi passa tale handle a Network Monitor.
-   Se le informazioni non sono disponibili, il parser non passa un handle e Network Monitor usa il set di follow del parser per determinare quale protocollo segue.

**Passaggio di informazioni tra protocolli**

Usare il *parametro lpInstData* per passare informazioni tra protocolli. Nell'input è possibile recuperare le informazioni dal protocollo precedente. Nell'output è possibile passare informazioni al protocollo successivo.

I dati dell'istanza possono essere dati di lunghezza minore o uguale a un PTR DWORD oppure puntatore a dati, ad esempio dati di frame non elaborati, che non devono essere allocati o liberati dal \_ parser.



| Per informazioni su                                        | Vedere                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Che cosa sono i parser e come funzionano con Network Monitor. | [Parser](parsers.md)                                                                                                    |
| Punti di ingresso inclusi nella DLL del parser.        | [Architettura della DLL del parser](parser-dll-architecture.md)                                                                    |
| Come implementare **RecognizeFrame**  include un esempio. | [Implementazione di RecognizeFrame](implementing-recognizeframe.md)                                                            |
| Come specificare un set di handoff e seguire il set.              | [Specifica di un set handoff](specifying-a-handoff-set.md)[che specifica un set di follow](specifying-a-follow-set.md)<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> </dl>

 

 





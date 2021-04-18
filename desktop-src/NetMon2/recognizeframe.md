---
description: La funzione di esportazione RecognizeFrame indica se una porzione di dati viene riconosciuta come protocollo rilevato dal parser. La funzione di esportazione RecognizeFrame deve essere implementata per ogni parser supportato dalla DLL del parser.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: Funzione di callback RecognizeFrame (Netmon. h)
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
ms.openlocfilehash: e2660629cecfa279377794749714102077fb6979
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319406"
---
# <a name="recognizeframe-callback-function"></a>Funzione di callback RecognizeFrame

La funzione di esportazione **RecognizeFrame** indica se una porzione di dati viene riconosciuta come protocollo rilevato dal parser. La funzione di esportazione **RecognizeFrame** deve essere implementata per ogni parser supportato dalla dll del parser.

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

*hFrame* \[ in\]
</dt> <dd>

Handle per il frame che contiene i dati.

</dd> <dt>

*lpFrame* \[ in\]
</dt> <dd>

Puntatore al primo byte di un frame. Il puntatore fornisce un modo per visualizzare i dati riconosciuti da altri parser.

</dd> <dt>

*lpProtocol* \[ in\]
</dt> <dd>

Puntatore all'inizio dei dati non recuperati. In genere, i dati non reclamati si trovano al centro di un frame perché un parser precedente ha richiesto i dati prima del parser. Il parser deve prima testare i dati non recuperati.

</dd> <dt>

*MacType* \[ in\]
</dt> <dd>

Valore MAC del primo protocollo in un frame. In genere, il valore *MacType* viene usato quando il parser deve identificare il primo protocollo in un frame. Il valore di *MacType* può essere uno dei seguenti:



| Valore                                                                                                                                                                         | Significato                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**\_Ethernet di tipo Mac \_**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**\_Tokenring di tipo Mac \_**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**\_FDDI di tipo Mac \_**</dt> </dl>                | ANSI X3T 9.5 <br/> |



 

</dd> <dt>

*BytesLeft* \[ in\]
</dt> <dd>

Il numero rimanente di byte da una posizione in un frame alla fine del frame.

</dd> <dt>

*hPreviousProtocol* \[ in\]
</dt> <dd>

Handle del protocollo precedente.

</dd> <dt>

*nPreviousProtocolOffset* \[ in\]
</dt> <dd>

Offset dell'inizio del protocollo precedente del frame.

</dd> <dt>

*ProtocolStatusCode* \[ out\]
</dt> <dd>

Indicatore di stato del protocollo. La DLL del parser deve impostare uno dei seguenti codici di stato.



| Valore                                                                                                                                                                                                              | Significato                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <dt>**stato del protocollo \_ \_ riconosciuto**</dt> </dl>              | Il parser riconosce i dati, ma non sa quale protocollo segue. Dopo aver impostato il codice, restituire un puntatore ai dati non attestati rimanenti che seguono il protocollo riconosciuto. Network Monitor usa il [*set*](f.md) di protocolli seguente per continuare l'analisi. <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <dt>**\_stato protocollo \_ non \_ riconosciuto**</dt> </dl> | Il parser non riconosce i dati. Dopo aver impostato questo codice, restituire il puntatore all'inizio dei dati utilizzando il puntatore passato dal parametro *lpProtocol* alla DLL del parser. Network Monitor usa il *set seguente* del protocollo precedente per continuare l'analisi. <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <dt>**stato del protocollo \_ \_ richiesto**</dt> </dl>                       | Il parser riconosce i dati e dichiara i dati rimanenti. Dopo aver impostato il codice, restituire **null** per Network Monitor per terminare l'analisi di un frame. <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <dt>**\_protocollo stato protocollo \_ successivo \_**</dt> </dl>    | Il parser riconosce i dati e sa quale protocollo segue. Dopo aver impostato il codice, impostare il parametro *phNextProtocol* e restituire un puntatore ai dati non attestati rimanenti che seguono il protocollo riconosciuto. Network Monitor continua ad analizzare il frame. <br/>                               |



 

</dd> <dt>

*phNextProtocol* \[ out\]
</dt> <dd>

Puntatore all'handle del protocollo successivo. Questo parametro viene impostato quando un protocollo identifica il protocollo che segue un protocollo. Per ottenere l'handle del protocollo successivo, chiamare la funzione [GetProtocolFromTable](getprotocolfromtable.md) .

</dd> <dt>

*lpInstData* \[ in uscita\]
</dt> <dd>

In input, puntatore ai dati dell'istanza del protocollo precedente.

Nell'output, un puntatore ai dati dell'istanza per il protocollo corrente. I dati dell'istanza non possono essere più lunghi di un \_ ptr DWORD di lunghezza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore al primo byte dopo i dati del parser riconosciuti. Se il parser reclama tutti i dati rimanenti, il valore restituito è **null**.

Se la funzione ha esito negativo, il valore restituito è un puntatore iniziale passato dal parametro *lpProtocol* .

## <a name="remarks"></a>Commenti

La funzione **RecognizeFrame** determina se il parser riconosce i dati non elaborati a partire dal puntatore *lpProtocol* .

-   Se il protocollo riconosce i dati, la funzione **RecognizeFrame** restituisce un puntatore ai dati rimanenti oppure restituisce **null** se il protocollo corrente è l'ultimo protocollo in un frame.
-   Se il protocollo non riconosce i dati, la funzione **RecognizeFrame** restituisce il puntatore passato alla DLL del parser nel parametro *lpProtocol* .

> [!Note]  
> È possibile chiamare *RecognizeFrame* prima di chiamare la funzione [*Register*](register-parser.md) per registrare le proprietà del protocollo. Per questo motivo, l'implementazione della funzione *RecognizeFrame* non si basa su alcuna proprietà o struttura creata o inizializzata durante l'implementazione della funzione di **Registro** del protocollo.

 

**Set di continuità e set di seguito**

Un parser può usare un set di continuità o un set di istruzioni per identificare per Network Monitor il protocollo che segue i dati riconosciuti.

-   Se le informazioni sono disponibili nei dati riconosciuti, il parser usa il set di continuità per ottenere un handle per il protocollo successivo, quindi passa tale handle a Network Monitor.
-   Se le informazioni non sono disponibili, il parser non passa un handle e Network Monitor usa il set di parser seguente per determinare il protocollo che segue.

**Passaggio di informazioni tra protocolli**

Usare il parametro *lpInstData* per passare le informazioni tra i protocolli. In input è possibile recuperare le informazioni dal protocollo precedente. Nell'output è possibile passare informazioni al protocollo successivo.

I dati dell'istanza possono essere dati di lunghezza minore o uguale a un \_ ptr DWORD o un puntatore ai dati, ad esempio dati di frame non elaborati, che non devono essere allocati o liberati dal parser.



| Per informazioni su                                        | Vedere                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor. | [Parser](parsers.md)                                                                                                    |
| I punti di ingresso inclusi nella DLL del parser.        | [Architettura DLL parser](parser-dll-architecture.md)                                                                    |
| L'implementazione di **RecognizeFrame**  include un esempio. | [Implementazione di RecognizeFrame](implementing-recognizeframe.md)                                                            |
| Come specificare un set di continuità e seguire il set.              | [Specifica di un set di continuità](specifying-a-handoff-set.md)che[specifica un set di seguito](specifying-a-follow-set.md)<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> </dl>

 

 





---
description: Il metodo GetConversationStatistics recupera le informazioni sulla sessione e sulla stazione relative all'acquisizione corrente.
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: 'Metodo IRTC:: GetConversationStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 758488cb3c3f65922bbf6aac4f39774a5430fc92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880714"
---
# <a name="irtcgetconversationstatistics-method"></a>Metodo IRTC:: GetConversationStatistics

Il metodo **GetConversationStatistics** recupera le informazioni sulla [*sessione*](s.md) e sulla [*stazione*](s.md) relative all'acquisizione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nSessions* \[ out\]
</dt> <dd>

Puntatore a un valore DWORD che contiene il numero di [*sessioni*](s.md) registrate per l'acquisizione corrente.

</dd> <dt>

*lpSessionStats* \[ out\]
</dt> <dd>

Puntatore a una struttura [SESSIONSTATS](sessionstats.md) .

</dd> <dt>

*nStations* \[ out\]
</dt> <dd>

Puntatore a un valore DWORD che contiene il numero di [*stazioni*](s.md) registrate per l'acquisizione corrente.

</dd> <dt>

*lpStationStats* \[ out\]
</dt> <dd>

Puntatore a una struttura [STATIONSTATS](stationstats.md) .

</dd> <dt>

*fClearAfterReading* \[ in\]
</dt> <dd>

Flag usato per indicare Network Monitor per cancellare l'archiviazione interna delle strutture [SESSIONSTATS](sessionstats.md) e [STATIONSTATS](stationstats.md) dopo aver recuperato le informazioni correnti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                   | Descrizione                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>          | L'oggetto NPP non è connesso alla rete. Chiamare [IRTC:: Connect](irtc-connect.md) per connettere l'oggetto NPP alla rete.<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ non \_ acquisizione**</dt> </dl>          | L'oggetto NPP non sta acquisendo dati. Chiamare [IRTC:: Start](irtc-start.md) per avviare l'acquisizione.<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ non in \_ tempo reale**</dt> </dl>           | L'oggetto NPP è connesso alla rete, ma non con il metodo [IRTC:: Connect](irtc-connect.md) .<br/>                                                                                                                          |
| <dl> <dt>**NMERR \_ Nessuna \_ statistica di conversazione \_**</dt> </dl> | La configurazione per questa connessione è impostata in modo da non salvare le statistiche di conversazione. Per salvare le statistiche delle conversazioni, arrestare l'acquisizione, impostare NoConversationStats = YES nel BLOB di configurazione, quindi riavviare l'acquisizione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato solo durante l'acquisizione dei dati; Se si chiama questo metodo mentre l'acquisizione corrente viene sospesa, il metodo avrà esito negativo. Per avviare un'acquisizione, chiamare il metodo [IRTC:: Start](irtc-start.md) .

Per recuperare altri tipi di statistiche, chiamare il metodo [IRTC:: GetTotalStatistics](irtc-gettotalstatistics.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: Connect](irtc-connect.md)
</dt> <dt>

[IRTC:: GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IRTC:: Start](irtc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATIONSTATS](stationstats.md)
</dt> </dl>

 

 





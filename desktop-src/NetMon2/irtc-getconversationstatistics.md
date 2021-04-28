---
description: "Metodo IRTC::GetConversationStatistics: il metodo GetConversationStatistics recupera le informazioni di sessione e stazione sull'acquisizione corrente."
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: Metodo IRTC::GetConversationStatistics (Netmon.h)
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
ms.openlocfilehash: 4d2476f4eb33d7e74d0de8363fa88d5e688a2e73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110699"
---
# <a name="irtcgetconversationstatistics-method"></a>Metodo IRTC::GetConversationStatistics

Il **metodo GetConversationStatistics** recupera le [*informazioni di*](s.md) sessione e [*stazione*](s.md) sull'acquisizione corrente.

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

*nSessioni* \[ Cambio\]
</dt> <dd>

Puntatore a un valore DWORD che contiene il numero [*di*](s.md) sessioni registrate per l'acquisizione corrente.

</dd> <dt>

*lpSessionStats* \[ Cambio\]
</dt> <dd>

Puntatore a [una struttura SESSIONSTATS.](sessionstats.md)

</dd> <dt>

*nStations* \[ Cambio\]
</dt> <dd>

Puntatore a un valore DWORD che contiene il numero di [*stazioni*](s.md) registrate per l'acquisizione corrente.

</dd> <dt>

*lpStationStats* \[ Cambio\]
</dt> <dd>

Puntatore a [una struttura STATIONSTATS.](stationstats.md)

</dd> <dt>

*fClearAfterReading* \[ Pollici\]
</dt> <dd>

Flag usato per indicare Network Monitor l'archiviazione interna delle strutture [SESSIONSTATS](sessionstats.md) e [STATIONSTATS](stationstats.md) dopo il recupero delle informazioni correnti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                   | Descrizione                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>          | NPP non è connesso alla rete. Chiamare [IRTC::Connect](irtc-connect.md) per connettere NPP alla rete.<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl>          | Il NPP non acquisisce dati. Chiamare [IRTC::Start](irtc-start.md) per avviare l'acquisizione.<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ NON IN TEMPO \_ REALE**</dt> </dl>           | Il protocollo NPP è connesso alla rete, ma non con [il metodo IRTC::Connect.](irtc-connect.md)<br/>                                                                                                                          |
| <dl> <dt>**NMERR \_ NO \_ CONVERSATION \_ STATS**</dt> </dl> | La configurazione per questa connessione è impostata in modo da non salvare le statistiche della conversazione. Per salvare le statistiche della conversazione, arrestare l'acquisizione, impostare NoConversationStats = YES nel BLOB di configurazione, quindi riavviare l'acquisizione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato solo durante l'acquisizione dei dati. Se si chiama questo metodo mentre l'acquisizione corrente è sospesa, il metodo non avrà esito positivo. Per avviare un'acquisizione, chiamare [il metodo IRTC::Start.](irtc-start.md)

Per recuperare altri tipi di statistiche, chiamare [il metodo IRTC::GetTotalStatistics.](irtc-gettotalstatistics.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Connect](irtc-connect.md)
</dt> <dt>

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATISTICHE DI STAZIONE](stationstats.md)
</dt> </dl>

 

 





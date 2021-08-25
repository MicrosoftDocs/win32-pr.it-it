---
description: Recupera le informazioni di sessione e stazione sull'acquisizione corrente.
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: Metodo IStats::GetConversationStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8e76bad23d79e261a27df5b83a94d4e477b21cde5057bb2587ffb49c93382df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890341"
---
# <a name="istatsgetconversationstatistics-method"></a>Metodo IStats::GetConversationStatistics

Il **metodo GetConversationStatistics** recupera le informazioni di sessione e stazione sull'acquisizione corrente.

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

*nSessions* \[ Cambio\]
</dt> <dd>

Puntatore a un valore DWORD che contiene il [*numero*](s.md) di sessioni registrate per l'acquisizione corrente.

</dd> <dt>

*lpSessionStats* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura SESSIONSTATS.**](sessionstats.md)

</dd> <dt>

*nStations* \[ Cambio\]
</dt> <dd>

Puntatore a un valore DWORD che contiene il numero [*di*](s.md) stazioni registrate per l'acquisizione corrente.

</dd> <dt>

*lpStationStats* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura STATIONSTATS.**](stationstats.md)

</dd> <dt>

*fClearAfterReading* \[ Pollici\]
</dt> <dd>

Flag utilizzato per indicare Network Monitor l'archiviazione interna delle strutture [**SESSIONSTATS**](sessionstats.md) e [**STATIONSTATS**](stationstats.md) dopo il recupero dei dati correnti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                   | Descrizione                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>          | NPP non è connesso alla rete. Chiamare [**IStats::Connessione**](istats-connect.md) per connettere NPP alla rete.<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl>          | NPP non acquisisce dati. Chiamare [**IStats::Start**](istats-start.md) per avviare l'acquisizione.<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ NON \_ STATS \_ ONLY**</dt> </dl>        | NPP è connesso alla rete, ma non con il [**metodo IStats::Connessione.**](istats-connect.md)<br/>                                                                                                                         |
| <dl> <dt>**NO \_ CONVERSATION \_ \_ STATS DI NMERR**</dt> </dl> | La configurazione per questa connessione è impostata in modo da non salvare le statistiche della conversazione. Per salvare le statistiche della conversazione, arrestare l'acquisizione, **impostare NoConversationStats = YES** nel BLOB di configurazione e quindi riavviare l'acquisizione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato solo mentre è in corso Data Capture. Quando l'acquisizione corrente viene sospesa, una chiamata a questo metodo non avrà esito positivo.

Per avviare un'acquisizione, chiamare il [**metodo IStats::Start.**](istats-start.md) Per recuperare altri tipi di statistiche, chiamare [**IStats::GetTotalStatistics**](istats-gettotalstatistics.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IStat**](istats.md)
</dt> <dt>

[**IStats::GetTotalStatistics**](istats-gettotalstatistics.md)
</dt> <dt>

[**IStats::Start**](istats-start.md)
</dt> <dt>

[**IStats::Connessione**](istats-connect.md)
</dt> <dt>

[**SESSIONSTATS**](sessionstats.md)
</dt> <dt>

[**STATIONSTATS**](stationstats.md)
</dt> </dl>

 

 





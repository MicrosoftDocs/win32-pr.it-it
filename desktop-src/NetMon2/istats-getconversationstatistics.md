---
description: Recupera le informazioni sulla sessione e sulla stazione relative all'acquisizione corrente.
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: 'Metodo IStats:: GetConversationStatistics (Netmon. h)'
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
ms.openlocfilehash: 030fafb4ccf041c2804179f8adf0088ca3fba845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319941"
---
# <a name="istatsgetconversationstatistics-method"></a>IStats:: GetConversationStatistics (metodo)

Il metodo **GetConversationStatistics** recupera le informazioni sulla sessione e sulla stazione relative all'acquisizione corrente.

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

Puntatore a una struttura [**SESSIONSTATS**](sessionstats.md) .

</dd> <dt>

*nStations* \[ out\]
</dt> <dd>

Puntatore a un valore DWORD che contiene il numero di [*stazioni*](s.md) registrate per l'acquisizione corrente.

</dd> <dt>

*lpStationStats* \[ out\]
</dt> <dd>

Puntatore a una struttura [**STATIONSTATS**](stationstats.md) .

</dd> <dt>

*fClearAfterReading* \[ in\]
</dt> <dd>

Flag utilizzato per indicare Network Monitor per cancellare l'archiviazione interna delle strutture [**SESSIONSTATS**](sessionstats.md) e [**STATIONSTATS**](stationstats.md) dopo il recupero dei dati correnti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                   | Descrizione                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>          | L'oggetto NPP non è connesso alla rete. Chiamare [**IStats:: Connect**](istats-connect.md) per connettere l'oggetto NPP alla rete.<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ non \_ acquisizione**</dt> </dl>          | L'oggetto NPP non sta acquisendo dati. Chiamare [**IStats:: Start**](istats-start.md) per avviare l'acquisizione.<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ non \_ \_ solo statistiche**</dt> </dl>        | L'oggetto NPP è connesso alla rete, ma non con il metodo [**IStats:: Connect**](istats-connect.md) .<br/>                                                                                                                         |
| <dl> <dt>**NMERR \_ Nessuna \_ statistica di conversazione \_**</dt> </dl> | La configurazione per questa connessione è impostata in modo da non salvare le statistiche di conversazione. Per salvare le statistiche di conversazione, arrestare l'acquisizione, impostare **NoConversationStats = Yes** nel BLOB di configurazione, quindi riavviare l'acquisizione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato solo mentre è in corso l'acquisizione dei dati; Quando l'acquisizione corrente viene sospesa, una chiamata a questo metodo avrà esito negativo.

Per avviare un'acquisizione, chiamare il metodo [**IStats:: Start**](istats-start.md) . Per recuperare altri tipi di statistiche, chiamare [**IStats:: GetTotalStatistics**](istats-gettotalstatistics.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats:: GetTotalStatistics**](istats-gettotalstatistics.md)
</dt> <dt>

[**IStats:: Start**](istats-start.md)
</dt> <dt>

[**IStats:: Connect**](istats-connect.md)
</dt> <dt>

[**SESSIONSTATS**](sessionstats.md)
</dt> <dt>

[**STATIONSTATS**](stationstats.md)
</dt> </dl>

 

 





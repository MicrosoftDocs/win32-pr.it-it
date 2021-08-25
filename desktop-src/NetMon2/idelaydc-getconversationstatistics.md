---
description: "Metodo IDelaydC::GetConversationStatistics: il metodo GetConversationStatistics recupera le informazioni sulla sessione e sulla stazione relative all'acquisizione corrente."
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: Metodo IDelaydC::GetConversationStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 60fc768a1b93a752a91d431e79fb3e875416ac2b82b2bad5603e3d4cddaccbaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910571"
---
# <a name="idelaydcgetconversationstatistics-method"></a>Metodo IDelaydC::GetConversationStatistics

Il **metodo GetConversationStatistics** recupera le [*informazioni sulla*](s.md) sessione e sulla [*stazione*](s.md) relative all'acquisizione corrente.

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

Flag usato per indicare Network Monitor cancellare l'archiviazione interna delle strutture [SESSIONSTATS](sessionstats.md) e [STATIONSTATS](stationstats.md) dopo il recupero delle informazioni correnti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                   | Descrizione                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>          | Il NPP non è connesso alla rete. Chiamare [IDelaydC::Connessione](idelaydc-connect.md) per connettere il NPP alla rete.<br/>                                                                                                  |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl>          | Il NPP non acquisisce dati. Chiamare [IDelaydC::Start](idelaydc-start.md) per avviare l'acquisizione.<br/>                                                                                                                             |
| <dl> <dt>**NMERR \_ NON \_ RITARDATO**</dt> </dl>            | Il NPP è connesso alla rete, ma non con il [metodo IDelaydC::Connessione.](idelaydc-connect.md)<br/>                                                                                                                      |
| <dl> <dt>**NMERR \_ NO \_ CONVERSATION \_ STATS**</dt> </dl> | La configurazione per questa connessione è impostata in modo da non salvare le statistiche di conversazione. Per salvare le statistiche della conversazione, arrestare l'acquisizione, impostare NoConversationStats = YES nel BLOB di configurazione e quindi riavviare l'acquisizione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato solo mentre è in corso l'acquisizione dei dati. Quando l'acquisizione corrente viene sospesa, le chiamate a questo metodo non avranno esito positivo. Per avviare un'acquisizione, chiamare [il metodo IDelaydC::Start.](idelaydc-start.md)

Per recuperare altri tipi di statistiche, chiamare [IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Connessione](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATISTICHE DI STAZIONE](stationstats.md)
</dt> </dl>

 

 





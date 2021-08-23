---
description: "Metodo IRTC::GetTotalStatistics: il metodo GetTotalStatistics recupera le statistiche totali per l'acquisizione corrente."
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: Metodo IRTC::GetTotalStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c2b5187ab0afb432e845c74d29144c02edf94cdb62f291ae69e88ea5a5fdf198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063871"
---
# <a name="irtcgettotalstatistics-method"></a>Metodo IRTC::GetTotalStatistics

Il **metodo GetTotalStatistics** recupera le [*statistiche totali per*](t.md) l'acquisizione [*corrente.*](c.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpStats* \[ Cambio\]
</dt> <dd>

Puntatore a una [struttura STATISTICS](statistics.md) che fornisce le statistiche totali per l'acquisizione. È responsabilità dei chiamanti allocare e liberare la memoria utilizzata dalla **struttura STATISTICS.**

</dd> <dt>

*fClearAfterReading* \[ Pollici\]
</dt> <dd>

Flag usato per indicare Network Monitor come gestire l'archiviazione interna delle statistiche totali. L'impostazione **TRUE** indica Network Monitor cancellare lo spazio di archiviazione interno delle statistiche totali dopo il recupero delle informazioni correnti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                          | Descrizione                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl> | Il NPP non è connesso alla rete. Chiamare [IRTC::Connessione](irtc-connect.md) per connettere il NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON IN TEMPO \_ REALE**</dt> </dl>  | Il NPP è connesso alla rete, ma non con il [metodo IRTC::Connessione.](irtc-connect.md)<br/>                     |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl> | Il NPP non acquisisce dati. Chiamare [IRTC::Start per](irtc-start.md) avviare l'acquisizione dei dati.<br/>                         |



 

## <a name="remarks"></a>Commenti

Questo metodo restituisce i dati solo mentre è in corso un'acquisizione, incluso mentre l'acquisizione è sospesa.

Network Monitor archivia anche le [*statistiche di conversazione*](c.md). Per recuperare le statistiche della conversazione, chiamare [il metodo IRTC::GetConversationStatistics.](irtc-getconversationstatistics.md)

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

[IRTC::Connessione](irtc-connect.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[Statistiche](statistics.md)
</dt> </dl>

 

 





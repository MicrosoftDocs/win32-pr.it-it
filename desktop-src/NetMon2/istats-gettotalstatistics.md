---
description: "Metodo IStats::GetTotalStatistics: il metodo GetTotalStatistics recupera le statistiche totali per l'acquisizione corrente."
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: Metodo IStats::GetTotalStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e6566a58212e8f20d0d999302f41ab97cb9f005e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098409"
---
# <a name="istatsgettotalstatistics-method"></a>Metodo IStats::GetTotalStatistics

Il **metodo GetTotalStatistics** recupera le [*statistiche totali*](t.md) per l'acquisizione [*corrente.*](c.md)

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

Puntatore a una [struttura STATISTICS](statistics.md)che fornisce le statistiche totali per l'acquisizione. È responsabilità del chiamante allocare e liberare la memoria usata dalla **struttura STATISTICS.**

</dd> <dt>

*fClearAfterReading* \[ Pollici\]
</dt> <dd>

Flag usato per indicare Network Monitor come gestire l'archiviazione interna delle statistiche totali. L'impostazione TRUE indica Network Monitor l'archiviazione interna delle statistiche totali dopo il recupero delle informazioni correnti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                            | Descrizione                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>   | NPP non è connesso alla rete. Chiamare il [metodo IStats::Connect](istats-connect.md) per connettere NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON \_ STATS \_ ONLY**</dt> </dl> | NPP è connesso alla rete, ma non con il [metodo IStats::Connect.](istats-connect.md)<br/>                                |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl>   | NPP non acquisisce dati. Chiamare il [metodo IStats::Start](istats-start.md) per avviare l'acquisizione dei dati.<br/>                         |



 

## <a name="remarks"></a>Commenti

Questo metodo restituisce i dati solo mentre è in corso un'acquisizione, incluso mentre l'acquisizione è sospesa.

Network Monitor anche le [*statistiche*](c.md)della conversazione, che possono essere recuperate chiamando il [metodo IStats::GetConversationStatistics.](istats-getconversationstatistics.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IStat](istats.md)
</dt> <dt>

[IStats::Connect](istats-connect.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> <dt>

[IStats::Start,](istats-start.md)
</dt> <dt>

[Statistiche](statistics.md)
</dt> </dl>

 

 





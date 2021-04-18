---
description: Il metodo GetTotalStatistics recupera le statistiche totali per l'acquisizione corrente.
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: 'Metodo IStats:: GetTotalStatistics (Netmon. h)'
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
ms.openlocfilehash: 51cdbfdcc796aa7d8091e8da5837809efaa63379
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315458"
---
# <a name="istatsgettotalstatistics-method"></a>IStats:: GetTotalStatistics (metodo)

Il metodo **GetTotalStatistics** recupera le [*statistiche totali*](t.md) per l' [*acquisizione*](c.md)corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpStats* \[ out\]
</dt> <dd>

Puntatore a una struttura di [statistiche](statistics.md)che fornisce le statistiche totali per l'acquisizione. È responsabilità del chiamante allocare e liberare la memoria usata dalla struttura delle **statistiche** .

</dd> <dt>

*fClearAfterReading* \[ in\]
</dt> <dd>

Flag utilizzato per indicare Network Monitor come gestire l'archiviazione interna delle statistiche totali. Un'impostazione di TRUE indica Network Monitor per cancellare l'archiviazione interna delle statistiche totali dopo che sono state recuperate le informazioni correnti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                            | Descrizione                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>   | L'oggetto NPP non è connesso alla rete. Chiamare il metodo [IStats:: Connect](istats-connect.md) per connettere l'oggetto NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ non \_ \_ solo statistiche**</dt> </dl> | L'oggetto NPP è connesso alla rete, ma non con il metodo [IStats:: Connect](istats-connect.md) .<br/>                                |
| <dl> <dt>**NMERR \_ non \_ acquisizione**</dt> </dl>   | L'oggetto NPP non sta acquisendo dati. Chiamare il metodo [IStats:: Start](istats-start.md) per avviare l'acquisizione dei dati.<br/>                         |



 

## <a name="remarks"></a>Commenti

Questo metodo restituisce i dati solo mentre è in corso un'acquisizione, incluso mentre l'acquisizione viene sospesa.

Network Monitor archivia anche le [*statistiche di conversazione*](c.md), che possono essere recuperate chiamando il metodo [IStats:: GetConversationStatistics](istats-getconversationstatistics.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats:: Connect](istats-connect.md)
</dt> <dt>

[IStats:: GetConversationStatistics](istats-getconversationstatistics.md)
</dt> <dt>

[IStats:: Start,](istats-start.md)
</dt> <dt>

[Statistiche](statistics.md)
</dt> </dl>

 

 





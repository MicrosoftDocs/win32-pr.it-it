---
description: "Metodo IDelaydC::GetTotalStatistics: il metodo GetTotalStatistics recupera le statistiche totali per l'acquisizione corrente."
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: Metodo IDelaydC::GetTotalStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e6b4d76b3035e156da1f1d4decf7a5c59b28bf0ca13bc2bdaa33e319422509af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037551"
---
# <a name="idelaydcgettotalstatistics-method"></a>Metodo IDelaydC::GetTotalStatistics

Il **metodo GetTotalStatistics** recupera le [*statistiche*](t.md) totali per l'acquisizione [*corrente.*](c.md)

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

Flag usato per indicare Network Monitor come gestire l'archiviazione interna delle statistiche totali. L'impostazione **TRUE** indica Network Monitor l'archiviazione interna delle statistiche totali dopo il recupero delle informazioni correnti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                          | Descrizione                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl> | NPP non è connesso alla rete. Chiamare [IDelaydC::Connessione](idelaydc-connect.md) per connettersi alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON \_ RITARDATO**</dt> </dl>   | NPP è connesso alla rete, ma non con il [metodo IDelaydC::Connessione.](idelaydc-connect.md)<br/>             |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl> | NPP non acquisisce dati. Chiamare [IDelaydC::Start](idelaydc-start.md) per avviare l'acquisizione dei dati.<br/>                 |



 

## <a name="remarks"></a>Commenti

Questo metodo restituisce i dati solo mentre è in corso un'acquisizione. Quando l'acquisizione viene sospesa, le chiamate a questo metodo non avranno esito positivo.

Network Monitor archivia anche [*statistiche*](c.md)di conversazione che possono essere recuperate chiamando il metodo [IDelaydC::GetConversationStatistics.](idelaydc-getconversationstatistics.md)

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

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[Statistiche](statistics.md)
</dt> </dl>

 

 





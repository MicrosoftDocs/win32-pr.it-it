---
description: Il metodo GetTotalStatistics recupera le statistiche totali per l'acquisizione corrente.
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: 'Metodo IDelaydC:: GetTotalStatistics (Netmon. h)'
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
ms.openlocfilehash: 0d194426933532fcf7a1965ed59b099489eefcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401604"
---
# <a name="idelaydcgettotalstatistics-method"></a>Metodo IDelaydC:: GetTotalStatistics

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

Flag utilizzato per indicare Network Monitor come gestire l'archiviazione interna delle statistiche totali. Un'impostazione di **true** indica Network Monitor per cancellare l'archiviazione interna delle statistiche totali dopo che sono state recuperate le informazioni correnti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                          | Descrizione                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl> | L'oggetto NPP non è connesso alla rete. Chiamare [IDelaydC:: Connect](idelaydc-connect.md) per connettersi alla rete.<br/> |
| <dl> <dt>**NMERR \_ non \_ ritardato**</dt> </dl>   | L'oggetto NPP è connesso alla rete, ma non con il metodo [IDelaydC:: Connect](idelaydc-connect.md) .<br/>             |
| <dl> <dt>**NMERR \_ non \_ acquisizione**</dt> </dl> | L'oggetto NPP non sta acquisendo dati. Chiamare [IDelaydC:: Start](idelaydc-start.md) per avviare l'acquisizione dei dati.<br/>                 |



 

## <a name="remarks"></a>Commenti

Questo metodo restituisce i dati solo mentre è in corso un'acquisizione. Quando l'acquisizione viene sospesa, le chiamate a questo metodo non riusciranno.

Network Monitor archivia anche le [*statistiche di conversazione*](c.md), che possono essere recuperate chiamando il metodo [IDelaydC:: GetConversationStatistics](idelaydc-getconversationstatistics.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC:: Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IDelaydC:: Start](idelaydc-start.md)
</dt> <dt>

[Statistiche](statistics.md)
</dt> </dl>

 

 





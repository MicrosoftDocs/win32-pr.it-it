---
title: Funzione MpThreatOpen (MpClient.h)
description: Restituisce un handle di enumerazione allo scopo di recuperare le minacce.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- Funzione MpThreatOpen Funzionalità dell'ambiente Windows legacy
topic_type:
- apiref
api_name:
- MpThreatOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 949fd1c8291ecb183cf51cf5385fe356a33cb1288978fda42f37d748f1a162a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746890"
---
# <a name="mpthreatopen-function"></a>Funzione MpThreatOpen

Restituisce un handle di enumerazione allo scopo di recuperare le minacce. Questa funzione può essere usata per aprire le minacce rilevate da un'analisi specifica, tutte le minacce attive nel sistema, la cronologia della disinfezione delle minacce o tutte le minacce presenti nel database di firma.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpThreatOpen(
  _In_  MPHANDLE        hScanHandle,
  _In_  MPTHREAT_SOURCE ThreatSource,
  _In_  MPTHREAT_TYPE   ThreatType,
  _Out_ PMPHANDLE       phThreatEnumHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hScanHandle* \[ Pollici\]
</dt> <dd>

Tipo: **MPHANDLE**

Può essere un handle per un'operazione di analisi completata, restituita dalla [**funzione MpScanStart.**](mpscanstart.md) In alternativa, questo parametro può essere impostato sull'handle dell'interfaccia di Malware Protection Manager restituito da [**MpManagerOpen**](mpmanageropen.md) per enumerare tutte le minacce attive nel sistema, la cronologia della disinfezione delle minacce o le minacce dal database di firma.

</dd> <dt>

*ThreatSource* \[ Pollici\]
</dt> <dd>

Tipo: **MPTHREAT \_ SOURCE**

Utilizzato per controllare l'origine dell'enumerazione delle minacce. I valori possibili per questo parametro sono:



| Valore                                                                                                                                                                                                 | Significato                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <dt>**ANALISI DELL'ORIGINE MPTHREAT \_ \_**</dt> </dl>                   | Minacce associate all'handle di analisi specifico.<br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <dt>**ORIGINE MPTHREAT \_ \_ ATTIVA**</dt> </dl>             | Minacce attualmente attive nel sistema.<br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <dt>**CRONOLOGIA \_ DELL'ORIGINE MPTHREAT \_**</dt> </dl>          | Minacce che vengono agite e mantenute come cronologia.<br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <dt>**QUARANTENA DELL'ORIGINE MPTHREAT \_ \_**</dt> </dl> | Minacce in quarantena.<br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <dt>**FIRMA DI ORIGINE MPTHREAT \_ \_**</dt> </dl>    | Minacce che è possibile rilevare con il database di firma corrente.<br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <dt>**STATO ORIGINE \_ MPTHREAT \_**</dt> </dl>                | Minacce che sono state agite di recente. "Recently" è definito da un'impostazione interna configurabile.<br/> |



 

</dd> <dt>

*ThreatType* \[ Pollici\]
</dt> <dd>

Tipo: **TIPO MPTHREAT \_**

Usato per filtrare le minacce enumerate in base al tipo di rilevamento. I valori possibili per questo parametro sono:



| Valore                                                                                                                                                                                           | Significato                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <dt>**TIPO MPTHREAT \_ \_ KNOWNBAD**</dt> </dl>       | Il rilevamento viene eseguito in base a una firma, un'emulazione o un altro metodo di rilevamento delle minacce specifico.<br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <dt>**TIPO MPTHREAT \_ \_ SOSPETTO**</dt> </dl> | Il rilevamento viene eseguito in base al monitoraggio del comportamento.<br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <dt>**TIPO MPTHREAT \_ \_ SCONOSCIUTO**</dt> </dl>          | Il rilevamento viene eseguito in base a minacce sconosciute (non classificate).<br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <dt>**TIPO MPTHREAT \_ \_ KNOWNGOOD**</dt> </dl>    | Il rilevamento viene eseguito in base alle minacce sicure note.<br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <dt>**NIS DI TIPO MPTHREAT \_ \_**</dt> </dl>                      | Il rilevamento viene eseguito in base alle minacce NIS.<br/>                                                       |



 

</dd> <dt>

*phThreatEnumHandle* \[ Cambio\]
</dt> <dd>

Tipo: **PMPHANDLE**

Handle di enumerazione delle minacce restituito che identifica il contesto di enumerazione. Questo handle può essere usato per enumerare le informazioni sulle minacce [**usando MpThreatEnumerate**](mpthreatenumerate.md). L'handle deve essere chiuso con la [**funzione MpHandleClose.**](mphandleclose.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.

Se la funzione ha esito negativo, il valore restituito è un **codice HRESULT non** riuscito. Il chiamante può usare la [**funzione MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> </dl>

 

 






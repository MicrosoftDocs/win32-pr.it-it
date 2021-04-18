---
title: Funzione MpThreatOpen (MpClient. h)
description: Restituisce un handle di enumerazione allo scopo di recuperare le minacce.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpThreatOpen
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
ms.openlocfilehash: ca30435f9d7cba32771a2445d8a1156f0edaa9b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301674"
---
# <a name="mpthreatopen-function"></a>MpThreatOpen (funzione)

Restituisce un handle di enumerazione allo scopo di recuperare le minacce. Questa funzione può essere utilizzata per aprire le minacce rilevate da un'analisi specifica, tutte le minacce attive nel sistema, la cronologia della disinfezione da minacce o tutte le minacce presenti nel database di firma.

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

*hScanHandle* \[ in\]
</dt> <dd>

Tipo: **MPHANDLE**

Può essere un handle per un'operazione di analisi completata, restituito dalla funzione [**MpScanStart**](mpscanstart.md) . In alternativa, questo parametro può essere impostato sull'handle di interfaccia di malware Protection Manager restituito da [**MpManagerOpen**](mpmanageropen.md) per enumerare tutte le minacce attive nel sistema, la cronologia della disinfettazione delle minacce o le minacce del database di firma.

</dd> <dt>

*ThreatSource* \[ in\]
</dt> <dd>

Tipo: **\_ origine MPTHREAT**

Utilizzato per controllare l'origine dell'enumerazione delle minacce. I valori possibili per questo parametro sono:



| Valore                                                                                                                                                                                                 | Significato                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <dt>**\_analisi origine \_ MPTHREAT**</dt> </dl>                   | Minacce associate all'handle di analisi specifico.<br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <dt>**\_origine MPTHREAT \_ attiva**</dt> </dl>             | Minacce attualmente attive nel sistema.<br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <dt>**\_Cronologia origine \_ MPTHREAT**</dt> </dl>          | Minacce che vengono eseguite e conservate come cronologia.<br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <dt>**\_ \_ quarantena origine MPTHREAT**</dt> </dl> | Minacce in quarantena.<br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <dt>**\_firma di origine MPTHREAT \_**</dt> </dl>    | Minacce che è possibile rilevare con il database della firma corrente.<br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <dt>**\_stato origine \_ MPTHREAT**</dt> </dl>                | Minacce che sono state eseguite di recente. ("Di recente" è definito da un'impostazione interna configurabile).<br/> |



 

</dd> <dt>

*ThreatType* \[ in\]
</dt> <dd>

Tipo: **MPTHREAT \_**

Utilizzato per filtrare le minacce enumerate in base al tipo di rilevamento. I valori possibili per questo parametro sono:



| Valore                                                                                                                                                                                           | Significato                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <dt>**MPTHREAT \_ tipo \_ KNOWNBAD**</dt> </dl>       | Il rilevamento viene eseguito in base a una firma specifica, un'emulazione o un altro metodo di rilevamento delle minacce.<br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <dt>**\_tipo MPTHREAT \_ sospetto**</dt> </dl> | Il rilevamento viene eseguito in base al monitoraggio del comportamento.<br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <dt>**\_tipo MPTHREAT \_ sconosciuto**</dt> </dl>          | Il rilevamento viene eseguito in base a minacce sconosciute (non classificate).<br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <dt>**MPTHREAT \_ tipo \_ KNOWNGOOD**</dt> </dl>    | Il rilevamento viene eseguito in base a minacce sicure note.<br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <dt>**MPTHREAT di \_ tipo \_ NIS**</dt> </dl>                      | Il rilevamento viene eseguito in base alle minacce NIS.<br/>                                                       |



 

</dd> <dt>

*phThreatEnumHandle* \[ out\]
</dt> <dd>

Tipo: **PMPHANDLE**

Handle di enumerazione della minaccia restituito che identifica il contesto di enumerazione. Questo handle può essere usato per enumerare le informazioni sulle minacce usando [**MpThreatEnumerate**](mpthreatenumerate.md). L'handle deve essere chiuso con la funzione [**MpHandleClose**](mphandleclose.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.

Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito. Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
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

 

 






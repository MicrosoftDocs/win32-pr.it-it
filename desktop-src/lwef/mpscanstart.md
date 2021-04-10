---
title: Funzione MpScanStart (MpClient. h)
description: Avvia un'operazione di analisi.
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpScanStart
topic_type:
- apiref
api_name:
- MpScanStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d343787edc85a18dc7471d19165999a7252d18a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964487"
---
# <a name="mpscanstart-function"></a>MpScanStart (funzione)

Avvia un'operazione di analisi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpScanStart(
  _In_     MPHANDLE          hMpHandle,
  _In_     MPSCAN_TYPE       ScanType,
  _In_     DWORD             dwScanOptions,
  _In_opt_ PMPSCAN_RESOURCES pScanResources,
  _In_opt_ PMPCALLBACK_INFO  pCallbackInfo,
  _Out_    PMPHANDLE         phScanHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMpHandle* \[ in\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per l'interfaccia di malware Protection Manager. Questo handle viene restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*ScanType* \[ in\]
</dt> <dd>

Tipo: **[ **MPSCAN \_**](mpscan-type.md)**

Specifica il tipo di analisi. Questo parametro deve essere uno dei membri del [**\_ tipo MPSCAN**](mpscan-type.md) enueration.

</dd> <dt>

*dwScanOptions* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Specifica varie opzioni per l'operazione di analisi.



| Valore                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <dt>**\_opzione MPSCAN \_ None**</dt> </dl>                               | Non è richiesta alcuna opzione specifica.<br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <dt>**\_opzione MPSCAN \_ Async**</dt> </dl>                            | L'operazione di analisi deve essere asincrona, in cui **MpScanStart** viene restituito immediatamente dopo la corretta inizializzazione dell'analisi. Per impostazione predefinita, l'operazione di analisi è sincrona, ovvero **MpScanStart** restituirà solo dopo il completamento dell'analisi.<br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <dt>**\_stato dell'opzione MPSCAN \_**</dt> </dl>                   | Il chiamante è interessato a ricevere informazioni sullo stato di avanzamento dell'analisi tramite un callback.<br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <dt>**\_opzione MPSCAN \_ LOWPRIORITY**</dt> </dl>          | Eseguire l'analisi con priorità bassa. Per impostazione predefinita, l'operazione di analisi viene eseguita con priorità normale.<br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <dt>**\_opzione MPSCAN \_ PACKEDEXES**</dt> </dl>             | Analizza i file eseguibili compressi per individuare possibili minacce.<br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <dt>**\_archivi delle opzioni di MPSCAN \_**</dt> </dl>                   | Analizza il contenuto dell'archivio per individuare possibili minacce. Gli archivi sono file con estensioni, ad esempio zip, CAB o tar.<br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <dt>**\_euristica dell'opzione MPSCAN \_**</dt> </dl>             | Abilitare l'analisi basata su euristica. Questa operazione analizzerà le minacce con tipo di rilevamento impostato su euristica.<br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <dt>**\_opzione MPSCAN \_ REPORTFRIENDLY**</dt> </dl> | Segnala elementi descrittivi in un'analisi delle risorse. Questa operazione è destinata solo a un uso interno.<br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <dt>**\_opzione MPSCAN \_ REPORTUNKNOWN**</dt> </dl>    | Segnala elementi sconosciuti in un'analisi delle risorse. Questa operazione è destinata solo a un uso interno.<br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <dt>**\_opzione MPSCAN \_ consolidate**</dt> </dl>    | Non consolidare i risultati dell'analisi con la visualizzazione minacce globali. Questa operazione è utile per un client, ad esempio un client di posta elettronica, che vuole controllare la pulizia dell'esperienza utente autonomamente, anziché consentire la pulizia dell'esperienza utente predefinita. Questa operazione è destinata solo a un uso interno.<br/> |



 

</dd> <dt>

*pScanResources* \[ in, facoltativo\]
</dt> <dd>

Tipo: **\_ risorse PMPSCAN**

Puntatore alle informazioni sulle risorse di analisi. Questo parametro deve essere **null** per un'analisi veloce. Si tratta di un parametro facoltativo per un'analisi completa. Per un'analisi delle risorse, questo parametro deve essere specificato con almeno una struttura di informazioni sulle risorse. Per analizzare risorse specifiche, il chiamante deve disporre dell'autorizzazione di **\_ lettura generica** per la risorsa. Vedere [**\_ risorse di MPSCAN**](mpscan-resources.md).

</dd> <dt>

*pCallbackInfo* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PMPCALLBACK \_ info**

Puntatore alle informazioni di callback utilizzate per inserire il client con le modifiche dello stato di analisi (ad esempio, avvio e completamento) e le informazioni sullo stato di avanzamento. I [**\_ dati MPCALLBACK**](mpcallback-data.md) restituiti nella funzione di callback segnalano lo stato di analisi effettivo e le informazioni relative allo stato di avanzamento. Di seguito è riportato un elenco di possibili callback:



| Valore                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <dt>**\_avvio dell'analisi MPNOTIFY \_**</dt> </dl>                            | Operazione di analisi avviata.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <dt>**\_analisi MPNOTIFY \_ completata**</dt> </dl>                   | Operazione di analisi completata. Altre informazioni sono disponibili tramite la struttura [**\_ dei dati MPSCAN**](mpscan-data.md) .<br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <dt>**\_analisi MPNOTIFY \_ sospesa**</dt> </dl>                         | Operazione di analisi sospesa.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <dt>**\_analisi MPNOTIFY \_ ripresa**</dt> </dl>                      | Operazione di analisi ripresa dalla pausa.<br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <dt>**\_annullamento dell'analisi MPNOTIFY \_**</dt> </dl>                         | Operazione di analisi annullata.<br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <dt>**\_stato analisi \_ MPNOTIFY**</dt> </dl>                   | Informazioni sullo stato di avanzamento dell'analisi. Altre informazioni, ad esempio le statistiche sulle risorse, sono disponibili tramite la struttura [**\_ dei dati MPSCAN**](mpscan-data.md) .<br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <dt>**\_errore di analisi MPNOTIFY \_**</dt> </dl>                            | Analizza le informazioni sugli errori per una risorsa specifica. Le informazioni specifiche sulle risorse sono disponibili tramite la struttura [**\_ dei dati MPSCAN**](mpscan-data.md) .<br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <dt>**\_analisi MPNOTIFY \_ infettata**</dt> </dl>                   | L'analisi ha rilevato una risorsa infetta. Si noti che nella maggior parte dei casi questo comporterà una minaccia segnalata alla fine dell'analisi. In alcuni casi potrebbe non essere materializzata come minaccia a causa di esclusioni. Altre informazioni sulle risorse infette sono disponibili tramite la struttura [**\_ dei dati MPSCAN**](mpscan-data.md) .<br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <dt>**MPNOTIFY \_ Scan \_ MEMORYSTART**</dt> </dl>          | È stata avviata la parte di analisi veloce dell'analisi completa.<br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <dt>**MPNOTIFY \_ Scan \_ MEMORYCOMPLETE**</dt> </dl> | È stata completata la parte di analisi veloce dell'analisi completa.<br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**\_errore interno \_ MPNOTIFY**</dt> </dl>          | Si è verificato un errore generico durante l'operazione di analisi. Il codice di errore del valore *HRESULT* nei [**\_ dati MPCALLBACK**](mpcallback-data.md) è specifico.<br/>                                                                                                                                                                   |



 

</dd> <dt>

*phScanHandle* \[ out\]
</dt> <dd>

Tipo: **PMPHANDLE**

Handle di analisi restituito che identifica l'analisi attualmente avviata. Questo handle può essere usato nelle chiamate di funzione successive, ad esempio per recuperare un risultato di analisi. L'handle deve essere chiuso con la funzione [**MpHandleClose**](mphandleclose.md) .

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

[**\_dati MPCALLBACK**](mpcallback-data.md)
</dt> <dt>

[**\_dati MPSCAN**](mpscan-data.md)
</dt> <dt>

[**risorse di MPSCAN \_**](mpscan-resources.md)
</dt> <dt>

[**\_tipo MPSCAN**](mpscan-type.md)
</dt> </dl>

 

 






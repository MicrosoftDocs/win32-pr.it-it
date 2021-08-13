---
title: Funzione MpScanStart (MpClient.h)
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
ms.openlocfilehash: 34d56f6814ecdd13b2db4f698e8cc122d4d15e325bda17d82d56a5796d8590fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450241"
---
# <a name="mpscanstart-function"></a>Funzione MpScanStart

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

*hMpHandle* \[ Pollici\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per l'interfaccia di Malware Protection Manager. Questo handle viene restituito dalla [**funzione MpManagerOpen.**](mpmanageropen.md)

</dd> <dt>

*ScanType* \[ Pollici\]
</dt> <dd>

Tipo: **[ **MPSCAN \_ TYPE**](mpscan-type.md)**

Specifica il tipo di analisi. Questo parametro deve essere uno dei membri dell'enueration [**MPSCAN \_ TYPE.**](mpscan-type.md)

</dd> <dt>

*dwScanOptions* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Specifica varie opzioni per l'operazione di analisi.



| Valore                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <dt>**OPZIONE MPSCAN \_ \_ NONE**</dt> </dl>                               | Non è richiesta alcuna opzione specifica.<br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <dt>**OPZIONE MPSCAN \_ \_ ASYNC**</dt> </dl>                            | L'operazione di analisi deve essere asincrona, in cui **MpScanStart** restituisce immediatamente dopo l'avvio corretto dell'analisi. Per impostazione predefinita, l'operazione di analisi è sincrona, ovvero **MpScanStart** restituirà solo al termine dell'analisi.<br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <dt>**STATO \_ DELL'OPZIONE MPSCAN \_**</dt> </dl>                   | Il chiamante è interessato a ricevere informazioni sullo stato di avanzamento dell'analisi tramite un callback.<br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <dt>**OPZIONE MPSCAN \_ \_ LOWPRIORITY**</dt> </dl>          | Eseguire l'analisi con priorità bassa. Per impostazione predefinita, l'operazione di analisi viene eseguita con priorità normale.<br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <dt>**MPSCAN \_ OPTION \_ PACKEDEXES**</dt> </dl>             | Analizzare i file eseguibili imballati alla ricerca di possibili minacce.<br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <dt>**ARCHIVI \_ \_ DELL'OPZIONE MPSCAN**</dt> </dl>                   | Analizzare il contenuto dell'archivio per le possibili minacce. Gli archivi sono file con estensioni come .zip, .cab o tar.<br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <dt>**\_EURISTICA \_ DELL'OPZIONE MPSCAN**</dt> </dl>             | Abilitare l'analisi basata sull'euristica. Verranno analizzate le minacce con tipo di rilevamento impostato su euristica.<br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <dt>**OPZIONE MPSCAN \_ \_ REPORTASTRUMENTE**</dt> </dl> | Segnalare elementi descrittivi in un'analisi delle risorse. È destinato solo all'uso interno.<br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <dt>**OPZIONE MPSCAN \_ \_ REPORTUNKNOWN**</dt> </dl>    | Segnalare elementi sconosciuti in un'analisi delle risorse. È destinato solo all'uso interno.<br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <dt>**OPZIONE MPSCAN \_ \_ NOCONSOLIDATE**</dt> </dl>    | Non consolidare i risultati dell'analisi con la visualizzazione globale delle minacce. Ciò è utile per un client (ad esempio un client di posta elettronica) che vuole controllare l'esperienza utente di pulizia da sola anziché consentire l'esperienza utente di pulizia antimalware predefinita. È destinato solo all'uso interno.<br/> |



 

</dd> <dt>

*pScanResources* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PMPSCAN \_ RESOURCES**

Puntatore alle informazioni sulla risorsa di analisi. Questo parametro deve essere **NULL per** un'analisi rapida. Si tratta di un parametro facoltativo per un'analisi completa. Per un'analisi delle risorse questo parametro deve essere specificato con almeno una struttura di informazioni sulle risorse. Per analizzare risorse specifiche, il chiamante deve disporre **\_ dell'autorizzazione GENERIC READ** per la risorsa. Vedere [**MPSCAN \_ RESOURCES**](mpscan-resources.md).

</dd> <dt>

*pCallbackInfo* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PMPCALLBACK \_ INFO**

Puntatore alle informazioni di callback usate per alimentare il client con le modifiche dello stato di analisi ,ad esempio l'avvio e il completamento, e le informazioni sullo stato. I [**dati MPCALLBACK \_ passati**](mpcallback-data.md) nella funzione di callback segnalano lo stato di analisi effettivo e le informazioni relative allo stato. Di seguito è riportato un elenco di possibili callback:



| Valore                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <dt>**AVVIO ANALISI \_ MPNOTIFY \_**</dt> </dl>                            | Operazione di analisi avviata.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <dt>**ANALISI MPNOTIFY \_ \_ COMPLETATA**</dt> </dl>                   | Operazione di analisi completata. Altre informazioni sono disponibili tramite la [**struttura MPSCAN \_**](mpscan-data.md) DATA.<br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <dt>**ANALISI MPNOTIFY \_ \_ SOSPESA**</dt> </dl>                         | L'operazione di analisi è sospesa.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <dt>**ANALISI MPNOTIFY \_ \_ RIPRESA**</dt> </dl>                      | L'operazione di analisi è stata ripresa dalla sospensione.<br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ CANCEL**</dt> </dl>                         | L'operazione di analisi è stata annullata.<br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <dt>**STATO ANALISI \_ MPNOTIFY \_**</dt> </dl>                   | Analizzare le informazioni sullo stato. Informazioni aggiuntive, ad esempio statistiche sulle risorse, sono disponibili tramite [**la struttura MPSCAN \_ DATA.**](mpscan-data.md)<br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <dt>**ERRORE DI ANALISI \_ \_ MPNOTIFY**</dt> </dl>                            | Analizzare le informazioni sugli errori per una risorsa specifica. Le informazioni specifiche sulle risorse sono disponibili tramite [**la struttura MPSCAN \_**](mpscan-data.md) DATA.<br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ INFECTED**</dt> </dl>                   | L'analisi ha rilevato una risorsa infetta. Si noti che nella maggior parte dei casi ciò comporta una minaccia segnalata alla fine dell'analisi. A volte potrebbe non materializzarsi come una minaccia a causa di esclusioni. Altre informazioni sulle risorse infette sono disponibili tramite [**la struttura MPSCAN \_ DATA.**](mpscan-data.md)<br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ MEMORYSTART**</dt> </dl>          | Parte dell'analisi rapida dell'analisi completa è stata avviata.<br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ MEMORYCOMPLETE**</dt> </dl> | Parte dell'analisi rapida dell'analisi completa è stata completata.<br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**ERRORE INTERNO \_ \_ MPNOTIFY**</dt> </dl>          | L'operazione di analisi ha rilevato un errore generico. *HResult* in [**MPCALLBACK \_ DATA**](mpcallback-data.md) ha il codice di errore specifico.<br/>                                                                                                                                                                   |



 

</dd> <dt>

*phScanHandle* \[ Cambio\]
</dt> <dd>

Tipo: **PMPHANDLE**

Handle di analisi restituito che identifica l'analisi attualmente avviata. Questo handle può essere usato nelle chiamate di funzione successive, ad esempio per recuperare un risultato dell'analisi. L'handle deve essere chiuso con la [**funzione MpHandleClose.**](mphandleclose.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.

Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT non** riuscito. Il chiamante può usare la [**funzione MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.

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

[**DATI \_ MPCALLBACK**](mpcallback-data.md)
</dt> <dt>

[**MPSCAN \_ DATA**](mpscan-data.md)
</dt> <dt>

[**RISORSE \_ MPSCAN**](mpscan-resources.md)
</dt> <dt>

[**TIPO \_ MPSCAN**](mpscan-type.md)
</dt> </dl>

 

 






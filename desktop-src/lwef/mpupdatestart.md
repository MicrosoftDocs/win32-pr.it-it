---
title: Funzione MpUpdateStart (MpClient. h)
description: Avvia un'operazione di aggiornamento della firma.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpUpdateStart
topic_type:
- apiref
api_name:
- MpUpdateStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39867525529339c6b354ae771b070589ca52acfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478736"
---
# <a name="mpupdatestart-function"></a>MpUpdateStart (funzione)

Avvia un'operazione di aggiornamento della firma.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpUpdateStart(
  _In_     MPHANDLE         hMpHandle,
  _In_     DWORD            dwUpdateOptions,
  _In_opt_ PMPCALLBACK_INFO pCallbackInfo,
  _Out_    PMPHANDLE        phUpdateHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMpHandle* \[ in\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per l'interfaccia di malware Protection Manager. Questo handle viene restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*dwUpdateOptions* \[ in\]
</dt> <dd>

Tipo: **DWORD**

Specifica l'opzione per l'operazione di aggiornamento della firma. Può essere uno dei valori seguenti:



| Valore                                                                                                                                                                                              | Significato                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <dt>**\_opzione MPUPDATE \_ None**</dt> </dl>                | Non è richiesta alcuna opzione specifica.<br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <dt>**\_opzione MPUPDATE \_ Async**</dt> </dl>             | L'operazione di aggiornamento deve essere asincrona, in cui **MpUpdateStart** viene restituito immediatamente dopo la riuscita dell'avvio dell'aggiornamento della firma. Per impostazione predefinita, l'operazione di aggiornamento è sincrona, ovvero **MpUpdateStart** restituirà solo dopo il completamento dell'aggiornamento della firma.<br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <dt>**\_stato dell'opzione MPUPDATE \_**</dt> </dl>    | Il chiamante è interessato a ricevere informazioni sullo stato di aggiornamento della firma tramite un callback.<br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <dt>**\_opzione MPUPDATE \_ http**</dt> </dl>                | L'aggiornamento della firma viene eseguito scaricando il pacchetto di firma completa dal sito del portale Microsoft Security. Può essere usata come opzione di fallback se il client sta riscontrando un problema di download della firma tramite Microsoft Update.<br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <dt>**\_UNC option \_ MPUPDATE**</dt> </dl>                   | Esegue l'aggiornamento della firma utilizzando il download diretto da condivisioni UNC.<br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <dt>**\_opzione MPUPDATE \_ gestita**</dt> </dl>       | Esegue l'aggiornamento della firma utilizzando il servizio gestito WSUS.<br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <dt>**\_opzione MPUPDATE \_ non gestita**</dt> </dl> | Esegue l'aggiornamento delle firme usando il servizio non gestito MU/WU.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

*pCallbackInfo* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PMPCALLBACK \_ info**

Puntatore alle informazioni di callback utilizzate per inserire il client con le modifiche dello stato di aggiornamento della firma (ad esempio, avvio e completamento) e le informazioni sullo stato di avanzamento. I [**\_ dati MPCALLBACK**](mpcallback-data.md) restituiti nella funzione di callback segnalano lo stato di aggiornamento effettivo e le informazioni relative allo stato di avanzamento. Di seguito è riportato un elenco di possibili callback:



| Valore                                                                                                                                                                                                                                | Significato                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <dt>**\_inizio MPNOTIFY SIGUPDATE \_**</dt> </dl>                                      | Operazione di aggiornamento avviata.<br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ completata**</dt> </dl>                             | Operazione di aggiornamento completata.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <dt>**\_avvio della \_ ricerca \_ SIGUPDATE di MPNOTIFY**</dt> </dl>                | Ricerca degli aggiornamenti avviata.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <dt>**\_ricerca MPNOTIFY \_ SIGUPDATE \_ completata**</dt> </dl>       | Ricerca degli aggiornamenti completata. Altre informazioni sono disponibili tramite la struttura [**\_ dei dati MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <dt>**avvio del download di MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>          | Download per l'aggiornamento avviato.<br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <dt>**stato del download di MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl> | Scaricare informazioni sullo stato di avanzamento. Altre informazioni sono disponibili tramite la struttura [**\_ dei dati MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <dt>**Download di MPNOTIFY \_ SIGUPDATE \_ \_ completato**</dt> </dl> | Download per l'aggiornamento completato. Altre informazioni sono disponibili tramite la struttura [**\_ dei dati MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <dt>**\_ \_ avvio installazione di MPNOTIFY SIGUPDATE \_**</dt> </dl>             | Installazione dell'aggiornamento avviata.<br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <dt>**stato di installazione di MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>    | Informazioni sullo stato dell'installazione. Altre informazioni sono disponibili tramite la struttura [**\_ dei dati MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <dt>**installazione di MPNOTIFY \_ SIGUPDATE \_ \_ completata**</dt> </dl>    | L'installazione dell'aggiornamento è stata completata. Altre informazioni sono disponibili tramite la struttura [**\_ dei dati MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <dt>**\_richiesta SIGUPDATE \_ MPNOTIFY \_ elaborata**</dt> </dl> | Il servizio antimalware ha elaborato una richiesta di aggiornamento della firma. Esito negativo o esito positivo è indicato da *HRESULT* nei [**\_ dati MPCALLBACK**](mpcallback-data.md).<br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <dt>**riavvio di MPNOTIFY \_ SIGUPDATE \_ \_ obbligatorio**</dt> </dl>       | Per completare l'operazione di aggiornamento, è necessario riavviare il computer. Esito negativo o esito positivo è indicato da *HRESULT* nei [**\_ dati MPCALLBACK**](mpcallback-data.md).<br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**\_errore interno \_ MPNOTIFY**</dt> </dl>                                   | Si è verificato un errore generico durante l'operazione di aggiornamento della firma. Il codice di errore del valore *HRESULT* nei [**\_ dati MPCALLBACK**](mpcallback-data.md) è specifico.<br/>    |



 

</dd> <dt>

*phUpdateHandle* \[ out\]
</dt> <dd>

Tipo: **PMPHANDLE**

Handle di aggiornamento restituito che identifica l'operazione di aggiornamento della firma attualmente avviata. Questo handle può essere utilizzato nelle chiamate di funzione successive, ad esempio per controllare l'operazione di aggiornamento della firma. L'handle deve essere chiuso con la funzione [**MpHandleClose**](mphandleclose.md) .

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

[**\_dati MPSIGUPDATE**](mpsigupdate-data.md)
</dt> </dl>

 

 






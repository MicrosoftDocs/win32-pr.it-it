---
title: Funzione MpUpdateStart (MpClient.h)
description: Avvia un'operazione di aggiornamento della firma.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- Funzione MpUpdateStart legacy Windows dell'ambiente
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
ms.openlocfilehash: a61cda213ecfbb23c9ef366fcce7b5c91e806f26f0f4ebe8b45dc596b63d1b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975891"
---
# <a name="mpupdatestart-function"></a>Funzione MpUpdateStart

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

*hMpHandle* \[ Pollici\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per l'interfaccia di Malware Protection Manager. Questo handle viene restituito dalla [**funzione MpManagerOpen.**](mpmanageropen.md)

</dd> <dt>

*dwUpdateOptions* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD**

Specifica l'opzione per l'operazione di aggiornamento della firma. Può essere uno dei valori seguenti:



| Valore                                                                                                                                                                                              | Significato                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <dt>**OPZIONE MPUPDATE \_ \_ NONE**</dt> </dl>                | Non è richiesta alcuna opzione specifica.<br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <dt>**OPZIONE MPUPDATE \_ \_ ASYNC**</dt> </dl>             | L'operazione di aggiornamento deve essere asincrona, in cui **MpUpdateStart** restituisce immediatamente dopo l'avvio corretto dell'aggiornamento della firma. Per impostazione predefinita, l'operazione di aggiornamento è sincrona, ovvero **MpUpdateStart** restituirà solo al termine dell'aggiornamento della firma.<br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <dt>**STATO \_ DELL'OPZIONE \_ MPUPDATE**</dt> </dl>    | Il chiamante è interessato a ricevere informazioni sullo stato di avanzamento dell'aggiornamento della firma tramite un callback.<br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <dt>**OPZIONE MPUPDATE \_ \_ HTTP**</dt> </dl>                | L'aggiornamento della firma viene eseguito scaricando il pacchetto di firma completo dal sito del portale di sicurezza Microsoft. Questa opzione può essere usata come opzione di fallback se il client riscontra un problema di download della firma tramite Microsoft Update.<br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <dt>**OPZIONE MPUPDATE \_ \_ UNC**</dt> </dl>                   | Esegue l'aggiornamento della firma usando il download diretto dalle condivisioni UNC.<br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <dt>**GESTIONE \_ DELL'OPZIONE \_ MPUPDATE**</dt> </dl>       | Esegue l'aggiornamento della firma usando WSUS del servizio gestito.<br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <dt>**OPZIONE MPUPDATE \_ \_ NON GESTITA**</dt> </dl> | Esegue l'aggiornamento della firma usando mu/WU del servizio non gestito.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

*pCallbackInfo* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PMPCALLBACK \_ INFO**

Puntatore alle informazioni di callback usate per alimentare il client con modifiche dello stato di aggiornamento della firma (ad esempio, avvio e completamento) e informazioni sullo stato. I [**dati MPCALLBACK \_ passati**](mpcallback-data.md) nella funzione di callback segnalano lo stato di aggiornamento effettivo e le informazioni relative allo stato di avanzamento. Di seguito è riportato un elenco di possibili callback:



| Valore                                                                                                                                                                                                                                | Significato                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ START**</dt> </dl>                                      | Operazione di aggiornamento avviata.<br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ COMPLETATO**</dt> </dl>                             | Operazione di aggiornamento completata.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <dt>**AVVIO RICERCA MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>                | Cercare gli aggiornamenti avviati.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <dt>**RICERCA MPNOTIFY \_ SIGUPDATE \_ \_ COMPLETATA**</dt> </dl>       | Ricerca degli aggiornamenti completata. Altre informazioni sono disponibili tramite [**la struttura MPSIGUPDATE \_ DATA.**](mpsigupdate-data.md)<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <dt>**AVVIO DEL DOWNLOAD DI MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>          | Download per l'aggiornamento avviato.<br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ DOWNLOAD \_ PROGRESS**</dt> </dl> | Scaricare le informazioni sullo stato. Altre informazioni sono disponibili tramite [**la struttura MPSIGUPDATE \_ DATA.**](mpsigupdate-data.md)<br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <dt>**DOWNLOAD DI MPNOTIFY \_ SIGUPDATE \_ \_ COMPLETATO**</dt> </dl> | Download per l'aggiornamento completato. Altre informazioni sono disponibili tramite [**la struttura MPSIGUPDATE \_ DATA.**](mpsigupdate-data.md)<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <dt>**AVVIO DELL'INSTALLAZIONE DI MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>             | Installazione dell'aggiornamento avviata.<br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <dt>**STATO DI INSTALLAZIONE DI MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>    | Informazioni sullo stato dell'installazione. Altre informazioni sono disponibili tramite [**la struttura MPSIGUPDATE \_ DATA.**](mpsigupdate-data.md)<br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <dt>**INSTALLAZIONE DI MPNOTIFY \_ SIGUPDATE \_ \_ COMPLETATA**</dt> </dl>    | Installazione dell'aggiornamento completata. Altre informazioni sono disponibili tramite [**la struttura MPSIGUPDATE \_ DATA.**](mpsigupdate-data.md)<br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <dt>**RICHIESTA MPNOTIFY \_ SIGUPDATE \_ \_ ELABORATA**</dt> </dl> | Il servizio antimalware ha elaborato una richiesta di aggiornamento della firma. L'esito negativo o positivo è indicato *da hResult* in [**MPCALLBACK \_ DATA**](mpcallback-data.md).<br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <dt>**È NECESSARIO RIAVVIARE MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>       | Richiede il riavvio per completare l'operazione di aggiornamento. L'esito negativo o positivo è indicato *da hResult* in [**MPCALLBACK \_ DATA**](mpcallback-data.md).<br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**ERRORE INTERNO \_ \_ MPNOTIFY**</dt> </dl>                                   | L'operazione di aggiornamento della firma ha rilevato un errore generico. *HResult* in [**MPCALLBACK \_ DATA**](mpcallback-data.md) ha il codice di errore specifico.<br/>    |



 

</dd> <dt>

*phUpdateHandle* \[ Cambio\]
</dt> <dd>

Tipo: **PMPHANDLE**

Handle di aggiornamento restituito che identifica l'operazione di aggiornamento della firma attualmente avviata. Questo handle può essere usato nelle chiamate di funzione successive, ad esempio per controllare l'operazione di aggiornamento della firma. L'handle deve essere chiuso con la [**funzione MpHandleClose.**](mphandleclose.md)

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

[**DATI \_ MPCALLBACK**](mpcallback-data.md)
</dt> <dt>

[**MPSIGUPDATE \_ DATA**](mpsigupdate-data.md)
</dt> </dl>

 

 






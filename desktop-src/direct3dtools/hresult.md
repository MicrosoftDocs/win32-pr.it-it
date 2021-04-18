---
description: Valori HRESULT personalizzati per l'interfaccia di acquisizione di diagnostica della grafica.
MS-HAID: vspixengine.Hresult
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione HRESULT
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 246FA53F-FF5B-44E1-BABB-F45AE0212687
api_name:
- Hresult
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3d5419feb0acb5967132fbb804a9bbc11bfa4248
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521569"
---
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span id="vspixengine.hresult"></span>Enumerazione HRESULT

Valori HRESULT personalizzati per l'interfaccia di acquisizione di diagnostica della grafica.

## <a name="syntax"></a>Sintassi


```C++
};
```

## <a name="constants"></a>Costanti

<span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX \_ S \_ OK**  
HRESULT comune che indica che l'operazione è riuscita come previsto.

<span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX \_ S \_ false**  
HRESULT comune che indica che l'operazione ha avuto esito positivo, ma in un modo diverso rispetto a quello previsto.

<span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**\_file di errore pix \_ \_ non \_ trovato**  
HRESULT personalizzato che non è stato trovato nel file degli errori di Echo \_ \_ \_ .

<span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**errore PIX- \_ \_ ambiente non valido \_**  
HRESULT personalizzato che Echos ERROR \_ male \_ Environment.

<span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**\_formato errore pix non \_ valido \_**  
HRESULT personalizzato che echi il formato errore non \_ valido \_ .

<span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**\_violazione della \_ condivisione degli errori di pix \_**  
HRESULT personalizzato che Echos viola la violazione della condivisione degli errori \_ \_ .

<span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**\_disco errore \_ pix \_ completo**  
HRESULT personalizzato che echi il disco di errore \_ \_ pieno.

<span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**\_ \_ altri dati sull'errore pix \_**  
HRESULT personalizzato che Echos segnala l'errore di \_ altri \_ dati.

<span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**\_criteri di \_ \_ debug \_ Kit \_ mancanti in Pix E mancante**  
HRESULT personalizzato che indica che i criteri di debug Kit risultano mancanti.

<span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**\_versione pix E \_ non valida \_**  
HRESULT personalizzato che indica che è in uso una versione non valida.

<span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX \_ E \_ uso di \_ DCOMP**  
HRESULT personalizzato che indica che DirectComposition è in uso (l'acquisizione di DirectComposition non è supportata).

<span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX \_ E \_ uso di \_ DIRECTWRITE**  
HRESULT personalizzato che indica che DirectWrite è in uso (l'acquisizione di DirectWrite non è supportata).

<span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX \_ E \_ uso di \_ d3d9**  
HRESULT personalizzato che indica che Direct3D9 è in uso (l'acquisizione di Direct3D9 non è supportata in Windows 10).

<span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**\_ \_ \_ creazione shader per pix E cant \_**  
HRESULT personalizzato che indica che non è possibile creare uno shader specificato.

<span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX \_ E \_ uso di \_ D2D**  
HRESULT personalizzato che indica che Direct2D è in uso (l'acquisizione di Direct2D non è supportata).

<span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX \_ E \_ nessun \_ frame**  
HRESULT personalizzato che indica che non sono stati acquisiti frame.

<span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX \_ E \_ Disabilita \_ Spy**  

<span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX \_ E \_ WIN8LOG \_ su \_ win7**  
HRESULT personalizzato che indica che non è possibile riprodurre Windows 8 vsglog in Windows 7.

<span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**\_traccia dello \_ shader di compilazione E \_ pix \_**  
HRESULT personalizzato che indica che si è verificato un errore durante la compilazione della traccia dello shader.

<span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX \_ E \_ Nessuna \_ \_ visualizzazione dati \_ CS**  
HRESULT personalizzato che indica che non è presente alcuna visualizzazione dei dati di compute shader.

<span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**SDK non corrispondente a PIX \_ E \_ \_**  
HRESULT personalizzato che indica una mancata corrispondenza con l'SDK corrente.

<span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**PIX \_ E \_ possibile \_ mancata corrispondenza dell' \_ SDK**  
HRESULT personalizzato che indica una possibile mancata corrispondenza con l'SDK corrente.

<span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**\_pixel non \_ rilevabile \_ E pix**  
HRESULT personalizzato che indica la presenza di un pixel non rilevabile.

<span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**DEBUG di PIX \_ E \_ cant \_ \_ shader \_ con \_ \_ semantica di valori di sistema \_**  
HRESULT personalizzato che indica che non è possibile eseguire il debug di Sahder utilizzando la semantica di valori di sistema.

<span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX \_ S \_ UPDATEAVAILABLE**  
HRESULT personalizzato che indica che è disponibile un aggiornamento.

<span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**\_stato DXGI pix- \_ \_ nessun \_ Reindirizzamento**  
HRESULT personalizzato che Echos DXGI \_ non è stato \_ \_ reindirizzato.

<span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**\_stato DXGI \_ pix \_ senza \_ \_ accesso desktop**  
HRESULT personalizzato che Echos DXGI \_ \_ non ha \_ \_ accesso al desktop.

<span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**\_ \_ \_ origine VIDPN della grafica dello stato DXGI pix \_ \_ \_ in \_ uso**  
HRESULT personalizzato che Echos DXGI \_ status \_ Graphics \_ VIDPN \_ source \_ in \_ uso.

<span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**\_ \_ modalità stato DXGI \_ pix \_ modificata**  
HRESULT personalizzato che Echos DXGI \_ status \_ mode \_ modificato.

<span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**\_ \_ \_ modifica della modalità di stato DXGI pix \_ \_ in \_ corso**  
È stato modificato un HRESULT personalizzato che Echos DXGI \_ status \_ mode \_ \_ \_ .

<span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**\_UNOCCLUDED DXGI \_ stato \_ pix**  
HRESULT personalizzato che echi DXGI \_ stato \_ UNOCCLUDED.

<span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**il \_ progetto DDA di stato DXGI di pix \_ \_ \_ è \_ ancora \_ in linea**  
È ancora in uso un HRESULT personalizzato che Echos DXGI \_ status \_ DDA sta \_ \_ ancora \_ disegnando.

<span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX \_ E \_ NOTIMPL**  
HRESULT personalizzato che Echos E \_ NOTIMPL.

<span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX \_ E \_ nointerface**  
HRESULT personalizzato che Echos E \_ nointerface.

<span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**\_puntatore pix E \_**  
HRESULT personalizzato che Echos E \_ pointer.

<span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**interruzione di PIX \_ E \_**  
HRESULT personalizzato che ECHO E \_ Abort.

<span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**PIX \_ E \_ Fail**  
HRESULT personalizzato che Echos E ha \_ esito negativo.

<span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX \_ E \_ imprevisto**  
HRESULT personalizzato che Echos E \_ imprevisto.

<span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX \_ E \_ AccessDenied**  
HRESULT personalizzato che Echos E \_ AccessDenied.

<span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**\_handle pix E \_**  
HRESULT personalizzato che Echos E \_ gestisce.

<span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX \_ E \_ OutOfMemory**  
HRESULT personalizzato che Echos E \_ OutOfMemory.

<span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX \_ E \_ INVALIDARG**  
HRESULT personalizzato che Echos E \_ INVALIDARG.

<span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**\_ \_ disco errori Xbox \_ pix \_ completo**  
HRESULT personalizzato che indica che il disco è pieno.

<span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**\_ \_ indirizzo di posta elettronica pix \_ \_ in \_ uso**  
HRESULT personalizzato che indica che l'indirizzo è già in uso.

<span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**\_criteri dei \_ \_ Kit mancanti \_ \_ per pix WS E**  
HRESULT personalizzato che indica che l'indirizzo non è disponibile.

<span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX \_ te \_ FAILEDTOLOADSOFTWAREMODULE**  
HRESULT personalizzato che indica che non è stato possibile caricare un modulo software necessario.

<span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX \_ te \_ USEDSOFTWAREMODULETHATWASNTWARPORREF**  
HRESULT personalizzato che indica che il modulo software utilizzato non è il driver WARP o REF.

<span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX \_ te \_ CORRUPTEDFILE**  
HRESULT personalizzato che indica che il file è danneggiato.

<span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX \_ te \_ FAILEDTOOPENFILE**  
HRESULT personalizzato che indica che non è stato possibile aprire il file.

<span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX \_ te \_ CALLFAILEDONPLAYBACK**  
HRESULT personalizzato che indica che una chiamata non è riuscita durante la riproduzione.

<span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX \_ te \_ UNKNOWNUUID**  
HRESULT personalizzato che indica che è stato rilevato un UUID sconosciuto; Questa operazione non dovrebbe mai verificarsi.

<span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX \_ te \_ NOTCAPTUREFILEORCORRUPTED**  
HRESULT personalizzato che indica che il file non è un file di acquisizione o è danneggiato.

<span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX \_ te \_ NEWERFILE**  

<span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX \_ te \_ OLDERFILE**  

<span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX \_ te \_ INVALIDMOMENT**  

<span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**\_driver di te non \_ valido \_**  
HRESULT personalizzato che indica che il driver non è valido.

<span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**\_errore \_ di accesso non è \_ possibile accedere \_ \_ a DEPTHSTENCIL nella \_ CPU**  
HRESULT personalizzato che indica che la CPU ha tentato di accedere al buffer di stencil Depth, causando un errore.

<span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**\_errore pix \_ risoluzione \_ della \_ trama multicampionata \_**  
HRESULT personalizzato che indica che si è verificato un tentativo di risolvere una trama multicampionata, causando un errore.

<span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**\_chiamata di \_ errore DXGI pix \_ non valida \_**  
HRESULT personalizzato che Echos DXGI \_ errore \_ chiamata non valida \_ .

<span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**\_errore DXGI \_ pix \_ non \_ trovato**  
Errore HRESULT personalizzato che Echos DXGI non è stato \_ \_ \_ trovato.

<span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**\_ \_ \_ altri dati sull'errore DXGI pix \_**  
HRESULT personalizzato che Echos DXGI \_ \_ più \_ dati.

<span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**\_errore DXGI pix non \_ \_ supportato**  
HRESULT personalizzato che Echos DXGI \_ Error non è \_ supportato.

<span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**\_dispositivo di \_ errore DXGI pix \_ \_ rimosso**  
HRESULT personalizzato che Echos DXGI \_ Error \_ Device \_ removed.

<span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**\_dispositivo di \_ errore DXGI pix \_ \_ bloccato**  
HRESULT personalizzato che Echos DXGI \_ Error \_ Device è \_ bloccato.

<span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**\_ripristino del \_ dispositivo con errore DXGI \_ pix \_**  
HRESULT personalizzato che Echos DXGI \_ Error \_ Reset del dispositivo \_ .

<span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**il \_ disegno dell'errore DXGI pix \_ \_ è \_ ancora \_ in linea**  
Un HRESULT personalizzato che \_ \_ è ancora stato disegnato dall'errore Echos DXGI \_ \_ .

<span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**\_statistiche del frame di errore pix DXGI non \_ \_ \_ \_ contigue**  
HRESULT personalizzato che Echos DXGI \_ Error \_ frame \_ STATISTICs \_ disgiunto.

<span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**\_ \_ \_ \_ origine VIDPN della grafica dell'errore pix DXGI \_ \_ in \_ uso**  
HRESULT personalizzato che Echos DXGI \_ \_ Graphics Error \_ VIDPN \_ source \_ in \_ uso.

<span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**\_ \_ \_ errore interno del driver di errore \_ pix DXGI \_**  
HRESULT personalizzato che Echos DXGI \_ errore \_ interno del driver \_ \_ .

<span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**\_errore DXGI pix non \_ \_ esclusivo**  
HRESULT personalizzato che Echos DXGI \_ errore non \_ esclusivo.

<span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**\_errore DXGI \_ pix \_ non \_ attualmente \_ disponibile**  
HRESULT personalizzato che Echos DXGI \_ Error \_ non è \_ attualmente \_ disponibile.

<span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**\_errore di DXGI pix \_ \_ \_ client remoto \_ scollegato**  
HRESULT personalizzato che Echos DXGI \_ Error \_ Remote \_ client \_ disconnesso.

<span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**\_OutOfMemory DXGI \_ \_ remoto errore \_ pix**  
HRESULT personalizzato che Echos DXGI \_ \_ Remote Error \_ OutOfMemory.

<span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**\_ \_ \_ modifica della modalità di errore DXGI pix \_ \_ in \_ corso**  
HRESULT personalizzato che Echos DXGI \_ Error \_ mode \_ modifica \_ in \_ corso.

<span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**\_ \_ accesso agli errori di DXGI pix \_ \_ perso**  
Un HRESULT personalizzato che Echos \_ DXGI \_ l'accesso A errori \_ persi.

<span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**\_timeout di \_ \_ attesa errore DXGI pix \_**  
HRESULT personalizzato che Echos DXGI \_ errore \_ di \_ timeout di attesa.

<span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**\_sessione di \_ errore DXGI pix \_ \_ disconnessa**  
HRESULT personalizzato che Echos DXGI \_ Error \_ Session \_ disconnected.

<span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**l' \_ errore DXGI di pix viene limitato \_ \_ \_ a \_ output non \_ aggiornato**  
Un HRESULT personalizzato che Echos DXGI \_ errore \_ limita l'output non \_ \_ \_ aggiornato.

<span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**\_errore DXGI \_ pix \_ non in grado di \_ proteggere il \_ contenuto**  
Un HRESULT personalizzato che Echos DXGI \_ Error \_ non può \_ proteggere il \_ contenuto.

<span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**\_ \_ accesso agli errori di DXGI pix \_ \_ negato**  
HRESULT personalizzato che Echos DXGI \_ ha \_ negato l'accesso \_ .

<span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**il \_ nome dell'errore DXGI pix \_ \_ \_ \_ esiste già**  
Un HRESULT personalizzato che ha un nome di errore Echos DXGI \_ \_ \_ \_ esiste già.

<span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**\_ \_ componente SDK per errori DXGI pix \_ \_ \_ mancante**  
HRESULT personalizzato che Echos DXGI \_ Error \_ SDK \_ Component \_ mancante.

<span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**\_WASSTILLDRAWING di \_ \_ errore DDI DXGI pix \_**  
HRESULT personalizzato che Echos DXGI \_ DDI \_ \_ WASSTILLDRAWING Err.

<span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**\_errore DDI DXGI di pix non \_ \_ \_ supportato**  
HRESULT personalizzato che Echos DXGI \_ DDI \_ Err non è \_ supportato.

<span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**\_DXGI DDI di pix \_ Err non \_ \_ esclusivo**  
HRESULT personalizzato che Echos DXGI \_ DDI \_ Err non è \_ esclusivo.

<span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**\_Errore D3D10 \_ pix \_ troppi \_ \_ \_ oggetti stato \_ univoco**  
HRESULT personalizzato che Echos D3D10 \_ errore di \_ troppi \_ oggetti di \_ \_ stato univoco \_ .

<span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**\_File di \_ errore D3D10 pix \_ \_ non \_ trovato**  
HRESULT personalizzato che Echos D3D10 \_ Error \_ file \_ non \_ trovato.

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**\_Errore d3d11 \_ pix \_ troppi \_ \_ \_ oggetti stato \_ univoco**  
HRESULT personalizzato che Echos D3D11 \_ errore di \_ troppi \_ oggetti di \_ \_ stato univoco \_ .

<span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**\_File di \_ errore d3d11 pix \_ \_ non \_ trovato**  
HRESULT personalizzato che Echos D3D11 \_ Error \_ file \_ non \_ trovato.

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**\_Errore d3d11 \_ pix \_ troppi \_ \_ \_ oggetti visualizzazione \_ univoca**  
HRESULT personalizzato che Echos D3D11 \_ errore di \_ troppi \_ \_ \_ oggetti visualizzazione univoca \_ .

<span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**\_Mappa del \_ contesto posticipato dell'errore d3d11 di pix \_ \_ \_ \_ senza \_ \_ eliminazione iniziale**  
HRESULT personalizzato che Echos D3D11 \_ errore \_ posticipato della \_ mappa del contesto \_ \_ senza \_ \_ eliminazione iniziale.

<span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**\_chiamata di \_ \_ estrazione con errore pix \_**  
HRESULT personalizzato che indica che una chiamata di un progetto è stata completamente incompleta, causando un errore.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 




---
title: Codici risultato IMAPIv1 (Imapierror. h)
description: '\_Se il metodo ha esito positivo, i metodi delle interfacce IMAP restituiscono S OK. In caso contrario, restituiscono uno dei seguenti codici di risultato.'
ms.assetid: 0143ad10-9b65-4621-9bed-71dadd38c3fc
topic_type:
- apiref
api_name:
- IMAPI_S_PROPERTIESIGNORED
- IMAPI_S_BUFFER_TO_SMALL
- IMAPI_E_NOTOPENED
- IMAPI_E_NOTINITIALIZED
- IMAPI_E_USERABORT
- IMAPI_E_GENERIC
- IMAPI_E_MEDIUM_NOTPRESENT
- IMAPI_E_MEDIUM_INVALIDTYPE
- IMAPI_E_DEVICE_NOPROPERTIES
- IMAPI_E_DEVICE_NOTACCESSIBLE
- IMAPI_E_DEVICE_NOTPRESENT
- IMAPI_E_DEVICE_INVALIDTYPE
- IMAPI_E_INITIALIZE_WRITE
- IMAPI_E_INITIALIZE_ENDWRITE
- IMAPI_E_FILESYSTEM
- IMAPI_E_FILEACCESS
- IMAPI_E_DISCINFO
- IMAPI_E_TRACKNOTOPEN
- IMAPI_E_TRACKOPEN
- IMAPI_E_DISCFULL
- IMAPI_E_BADJOLIETNAME
- IMAPI_E_INVALIDIMAGE
- IMAPI_E_NOACTIVEFORMAT
- IMAPI_E_NOACTIVERECORDER
- IMAPI_E_WRONGFORMAT
- IMAPI_E_ALREADYOPEN
- IMAPI_E_WRONGDISC
- IMAPI_E_FILEEXISTS
- IMAPI_E_STASHINUSE
- IMAPI_E_DEVICE_STILL_IN_USE
- IMAPI_E_LOSS_OF_STREAMING
- IMAPI_E_COMPRESSEDSTASH
- IMAPI_E_ENCRYPTEDSTASH
- IMAPI_E_NOTENOUGHDISKFORSTASH
- IMAPI_E_REMOVABLESTASH
- IMAPI_E_CANNOT_WRITE_TO_MEDIA
- IMAPI_E_TRACK_NOT_BIG_ENOUGH
api_location:
- Imapierror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80e8aba2a2d3d12628a45c6716c6f94a405d752f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739983"
---
# <a name="imapiv1-result-codes"></a>Codici di risultato di IMAPIv1

\_Se il metodo ha esito positivo, i metodi delle interfacce IMAP restituiscono S OK. In caso contrario, restituiscono uno dei seguenti codici di risultato.



| Costante/valore                                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMAPI_S_PROPERTIESIGNORED"></span><span id="imapi_s_propertiesignored"></span><dl> <dt>**\_ IMAPI S \_ PROPERTIESIGNORED**</dt> <dt>0x40200</dt> </dl>                   | Una proprietà sconosciuta è stata passata in un set di proprietà ed è stata ignorata.<br/>                                                                                                                                                                              |
| <span id="IMAPI_S_BUFFER_TO_SMALL"></span><span id="imapi_s_buffer_to_small"></span><dl> <dt>**\_ IMAPI \_Buffer S \_ a \_ small**</dt> <dt>0x40201</dt> </dl>                       | Il buffer di output è troppo piccolo.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTOPENED"></span><span id="imapi_e_notopened"></span><dl> <dt>**\_ IMAPI E \_ ancoraaperte**</dt> <dt>0x8004020b</dt> </dl>                                        | Non è stata eseguita una chiamata a [**IDiscMaster:: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) .<br/>                                                                                                                                                                        |
| <span id="IMAPI_E_NOTINITIALIZED"></span><span id="imapi_e_notinitialized"></span><dl> <dt>**\_ IMAPI E \_ NOTINITIALIZED**</dt> <dt>0x8004020c</dt> </dl>                         | Un oggetto registratore non è stato inizializzato.<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_USERABORT"></span><span id="imapi_e_userabort"></span><dl> <dt>**\_ IMAPI E \_ USERABORT**</dt> <dt>0x8004020D</dt> </dl>                                        | L'utente ha annullato l'operazione.<br/>                                                                                                                                                                                                                  |
| <span id="IMAPI_E_GENERIC"></span><span id="imapi_e_generic"></span><dl> <dt>**\_ IMAPI 0x8004020E \_ generico E**</dt> <dt></dt> </dl>                                              | Si è verificato un errore generico.<br/>                                                                                                                                                                                                                         |
| <span id="IMAPI_E_MEDIUM_NOTPRESENT"></span><span id="imapi_e_medium_notpresent"></span><dl> <dt>**\_ IMAPI 0x8004020f \_ \_ NOTPRESENT E medium**</dt> <dt></dt> </dl>               | Non è presente alcun disco nel dispositivo.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_MEDIUM_INVALIDTYPE"></span><span id="imapi_e_medium_invalidtype"></span><dl> <dt>**\_ IMAPI 0x80040210 \_ \_ INVALIDTYPE E medium**</dt> <dt></dt> </dl>            | Il supporto non è un tipo utilizzabile.<br/>                                                                                                                                                                                                         |
| <span id="IMAPI_E_DEVICE_NOPROPERTIES"></span><span id="imapi_e_device_noproperties"></span><dl> <dt>**\_ IMAPI \_Dispositivi E \_ noproperties**</dt> <dt>0x80040211</dt> </dl>         | Il registratore non supporta proprietà.<br/>                                                                                                                                                                                                     |
| <span id="IMAPI_E_DEVICE_NOTACCESSIBLE"></span><span id="imapi_e_device_notaccessible"></span><dl> <dt>**\_ IMAPI \_Dispositivo E \_ NOTACCESSIBLE**</dt> <dt>0x80040212</dt> </dl>      | Non è possibile usare il dispositivo o è già in uso.<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DEVICE_NOTPRESENT"></span><span id="imapi_e_device_notpresent"></span><dl> <dt>**\_ IMAPI \_Dispositivo E \_ NOTPRESENT**</dt> <dt>0x80040213</dt> </dl>               | Il dispositivo non è presente o è stato rimosso.<br/>                                                                                                                                                                                                    |
| <span id="IMAPI_E_DEVICE_INVALIDTYPE"></span><span id="imapi_e_device_invalidtype"></span><dl> <dt>**\_ IMAPI \_Dispositivo E \_ INVALIDTYPE**</dt> <dt>0x80040214</dt> </dl>            | Il registratore non supporta un'operazione.<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_INITIALIZE_WRITE"></span><span id="imapi_e_initialize_write"></span><dl> <dt>**\_ IMAPI E \_ Inizializza \_ scrittura**</dt> <dt>0x80040215</dt> </dl>                  | Non è stato possibile inizializzare l'interfaccia dell'unità per la scrittura.<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_INITIALIZE_ENDWRITE"></span><span id="imapi_e_initialize_endwrite"></span><dl> <dt>**\_ IMAPI E \_ Inizializza \_ ENDWRITE**</dt> <dt>0x80040216</dt> </dl>         | Non è stato possibile inizializzare l'interfaccia dell'unità per la chiusura.<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_FILESYSTEM"></span><span id="imapi_e_filesystem"></span><dl> <dt>**\_ IMAPI E \_ filesystem**</dt> <dt>0x80040217</dt> </dl>                                     | Si è verificato un errore durante l'abilitazione o la disabilitazione dell'accesso file system o durante il rilevamento dell'inserimento automatico.<br/>                                                                                                                                                 |
| <span id="IMAPI_E_FILEACCESS"></span><span id="imapi_e_fileaccess"></span><dl> <dt>**\_ IMAPI E \_**</dt> <dt>0x80040218</dt> FILEACCESS </dl>                                     | Si è verificato un errore durante la scrittura del file di immagine.<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DISCINFO"></span><span id="imapi_e_discinfo"></span><dl> <dt>**\_ IMAPI E \_ DISCINFO**</dt> <dt>: 0x80040219</dt> </dl>                                           | Si è verificato un errore durante il tentativo di leggere i dati del disco dal dispositivo.<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_TRACKNOTOPEN"></span><span id="imapi_e_tracknotopen"></span><dl> <dt>**\_ IMAPI E \_ TRACKNOTOPEN**</dt> <dt>0x8004021a</dt> </dl>                               | Una traccia audio non è aperta per la scrittura.<br/>                                                                                                                                                                                                           |
| <span id="IMAPI_E_TRACKOPEN"></span><span id="imapi_e_trackopen"></span><dl> <dt>**\_ IMAPI E \_ TRACKOPEN**</dt> <dt>0x8004021b</dt> </dl>                                        | È già in corso la gestione temporanea di una traccia audio aperta.<br/>                                                                                                                                                                                                      |
| <span id="IMAPI_E_DISCFULL"></span><span id="imapi_e_discfull"></span><dl> <dt>**\_ IMAPI E \_ DISCFULL**</dt> <dt>0x8004021c</dt> </dl>                                           | Il disco non può conservare più dati.<br/>                                                                                                                                                                                                               |
| <span id="IMAPI_E_BADJOLIETNAME"></span><span id="imapi_e_badjolietname"></span><dl> <dt>**\_ IMAPI E \_ BADJOLIETNAME**</dt> <dt>0x8004021d</dt> </dl>                            | L'applicazione ha tentato di aggiungere un elemento con nome non corretto a un disco.<br/>                                                                                                                                                                                     |
| <span id="IMAPI_E_INVALIDIMAGE"></span><span id="imapi_e_invalidimage"></span><dl> <dt>**\_ IMAPI E \_ INVALIDIMAGE**</dt> <dt>0x8004021e</dt> </dl>                               | L'immagine di gestione temporanea non è adatta per un'ustione. È stata danneggiata o cancellata e non contiene contenuto utilizzabile.<br/>                                                                                                                                          |
| <span id="IMAPI_E_NOACTIVEFORMAT"></span><span id="imapi_e_noactiveformat"></span><dl> <dt>**\_ IMAPI E \_ NOACTIVEFORMAT**</dt> <dt>0x8004021f</dt> </dl>                         | Un master di formato attivo non è stato selezionato con [**IDiscMaster:: SetActiveDiscMasterFormat**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscmasterformat).<br/>                                                                                                      |
| <span id="IMAPI_E_NOACTIVERECORDER"></span><span id="imapi_e_noactiverecorder"></span><dl> <dt>**\_ IMAPI E \_ NOACTIVERECORDER**</dt> <dt>0x80040220</dt> </dl>                   | Un registratore del disco attivo non è stato selezionato con [**IDiscMaster:: SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder).<br/>                                                                                                              |
| <span id="IMAPI_E_WRONGFORMAT"></span><span id="imapi_e_wrongformat"></span><dl> <dt>**\_ IMAPI E \_ WRONGFORMAT**</dt> <dt>0x80040221</dt> </dl>                                  | È stata effettuata una chiamata a [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) quando [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) è il formato attivo o viceversa. Per usare un formato diverso, modificare il formato e cancellare il contenuto del file di immagine.<br/> |
| <span id="IMAPI_E_ALREADYOPEN"></span><span id="imapi_e_alreadyopen"></span><dl> <dt>**\_ IMAPI E \_ ALREADYOPEN**</dt> <dt>0x80040222</dt> </dl>                                  | Una chiamata a [**IDiscMaster:: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) è già stata eseguita su questo oggetto dall'applicazione.<br/>                                                                                                                            |
| <span id="IMAPI_E_WRONGDISC"></span><span id="imapi_e_wrongdisc"></span><dl> <dt>**\_ IMAPI E \_ WRONGDISC**</dt> <dt>0x80040223</dt> </dl>                                        | Il disco IMAPi con più sessioni è stato rimosso dal registratore attivo.<br/>                                                                                                                                                                           |
| <span id="IMAPI_E_FILEEXISTS"></span><span id="imapi_e_fileexists"></span><dl> <dt>**\_ IMAPI E \_ FILEexists**</dt> <dt>0x80040224</dt> </dl>                                     | Il file da aggiungere è già presente nel file di immagine e il flag di sovrascrittura non è stato impostato.<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_STASHINUSE"></span><span id="imapi_e_stashinuse"></span><dl> <dt>**\_ IMAPI E \_ STASHINUSE**</dt> <dt>0x80040225</dt> </dl>                                     | Un'altra applicazione sta già usando il file di accantonamento IMAP necessario per organizzare un'immagine del disco. Riprovare più tardi.<br/>                                                                                                                                        |
| <span id="IMAPI_E_DEVICE_STILL_IN_USE"></span><span id="imapi_e_device_still_in_use"></span><dl> <dt>**\_ IMAPI Il \_ dispositivo E è \_ ancora \_ in \_ uso**</dt> <dt>0x80040226</dt> </dl>       | Un'altra applicazione sta già usando questo dispositivo, quindi IMAPi non può accedere al dispositivo.<br/>                                                                                                                                                              |
| <span id="IMAPI_E_LOSS_OF_STREAMING"></span><span id="imapi_e_loss_of_streaming"></span><dl> <dt>**\_ IMAPI E \_ perdita \_ di \_ flussi di**</dt> <dt>0x80040227</dt> </dl>              | Il flusso del contenuto è andato perso; potrebbe essersi verificato un buffer in esecuzione.<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_COMPRESSEDSTASH"></span><span id="imapi_e_compressedstash"></span><dl> <dt>**\_ IMAPI E \_ COMPRESSEDSTASH**</dt> <dt>0x80040228</dt> </dl>                      | Il stash si trova in un volume compresso e non può essere letto.<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_ENCRYPTEDSTASH"></span><span id="imapi_e_encryptedstash"></span><dl> <dt>**\_ IMAPI E \_ ENCRYPTEDSTASH**</dt> <dt>0x80040229</dt> </dl>                         | Il stash si trova in un volume crittografato e non può essere letto.<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTENOUGHDISKFORSTASH"></span><span id="imapi_e_notenoughdiskforstash"></span><dl> <dt>**\_ IMAPI E \_ NOTENOUGHDISKFORSTASH**</dt> <dt>0x8004022a</dt> </dl>    | Lo spazio disponibile non è sufficiente per creare il file stash nel volume specificato.<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_REMOVABLESTASH"></span><span id="imapi_e_removablestash"></span><dl> <dt>**\_ IMAPI E \_ REMOVABLESTASH**</dt> <dt>0x8004022b</dt> </dl>                         | Il percorso di Stash selezionato si trova su un supporto rimovibile.<br/>                                                                                                                                                                                              |
| <span id="IMAPI_E_CANNOT_WRITE_TO_MEDIA"></span><span id="imapi_e_cannot_write_to_media"></span><dl> <dt>**\_ IMAPI E \_ non \_ è \_ in grado di scrivere su \_ supporti**</dt> <dt>0x8004022C</dt> </dl> | Non è possibile scrivere sul supporto.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_TRACK_NOT_BIG_ENOUGH"></span><span id="imapi_e_track_not_big_enough"></span><dl> <dt>**\_ IMAPI E \_ tenere traccia di 0x8004022d \_ non \_ \_ sufficientemente grande**</dt> <dt></dt> </dl>    | La traccia non è abbastanza grande.<br/>                                                                                                                                                                                                                      |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Imapierror. h</dt> </dl> |



 

 






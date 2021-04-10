---
description: Le applicazioni, inclusi i servizi, possono registrarsi per ricevere notifiche di eventi del dispositivo.
ms.assetid: c89da4ac-57dd-4d95-ac86-3eb137dee0bc
title: Eventi dispositivo (IoEvent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce58ba5dd21cdd505e945687603ddb54e77b2440
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225513"
---
# <a name="device-events-ioeventh"></a>Eventi dispositivo (IoEvent. h)

Le applicazioni, inclusi i servizi, possono registrarsi per ricevere notifiche di eventi del dispositivo. Ad esempio, un servizio di catalogo può ricevere l'avviso dei volumi montati o smontati, in modo da poter modificare i percorsi dei file nel volume. Il sistema notifica a un'applicazione che si è verificato un evento del dispositivo inviando all'applicazione un messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) . Il sistema notifica a un servizio che si è verificato un evento del dispositivo richiamando la funzione del gestore eventi del servizio, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).

Per ricevere le notifiche degli eventi del dispositivo, chiamare la funzione [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) con una struttura dell' [**handle di \_ trasmissione \_ dello sviluppo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) . Assicurarsi di impostare il membro **dell' \_ handle dbch** sull'handle di dispositivo ottenuto dalla funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . Impostare anche il membro **dbch \_ DeviceType** su **DBT \_ DEVTYP \_ handle**. La funzione restituisce un handle di notifica del dispositivo. Si noti che questo non è lo stesso dell'handle del volume.

Quando l'applicazione riceve una notifica, se il tipo di evento è [DBT \_ CUSTOMEVENT](dbt-customevent.md), è possibile che sia stato ricevuto uno degli eventi del dispositivo definiti in IoEvent. h. Per determinare se si è verificato uno di questi eventi, attenersi alla procedura riportata di seguito.

1.  Considerare i dati dell'evento come una struttura [**\_ \_ HDR di sviluppo broadcast**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) . Verificare che il membro **dbch \_ DeviceType** sia impostato su **DBT \_ DEVTYP \_ handle**.
2.  Se **dbch \_ DeviceType** è **DBT \_ DEVTYP \_ handle**, i dati dell'evento sono effettivamente un puntatore a una struttura di [**\_ \_ handle di broadcast di sviluppo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .
3.  Confrontare il membro **dbch \_ EventGuid** con il **GUID** elencato nella tabella seguente usando la funzione [**IsEqualGuid**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) .

<dl> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**\_ \_ \_ blocco esclusivo cdrom \_ i/o di GUID**
</dt> <dd> <dl> <dt>

bc56c139-7a10-47ee-a294-4c6a38f0149a
</dt> <dt>



Il dispositivo CD-ROM è stato bloccato per l'accesso esclusivo.

**Windows Server 2003 e Windows XP:** Il supporto per questo valore richiede IMAPi 2,0. Per altre informazioni, vedere [API di Image Mastering](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**\_ \_ \_ sblocco esclusivo GUID io \_ CDROM**
</dt> <dd> <dl> <dt>

a3b6d27d-5e35-4885-81e5-ee18c00ed779
</dt> <dt>



Un dispositivo CD-ROM bloccato per l'accesso esclusivo è stato sbloccato.

**Windows Server 2003 e Windows XP:** Il supporto per questo valore richiede IMAPi 2,0. Per altre informazioni, vedere [API di Image Mastering](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**il dispositivo di i/o GUID \_ \_ \_ diventa \_ pronto**
</dt> <dd> <dl> <dt>

d07433f0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



La rotazione dei supporti è in corso.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**\_ \_ richiesta esterna del dispositivo io \_ GUID \_**
</dt> <dd> <dl> <dt>

d07433d0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Esistono diverse cause possibili per questo evento. Per ulteriori informazioni, vedere la specifica di T10 MMC del comando GET EVENT STATUS NOTIFICATION, all'indirizzo [https://www.t10.org/](https://www.t10.org/) .


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**\_arrivo del \_ supporto i/o GUID \_**
</dt> <dd> <dl> <dt>

d07433c0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Al dispositivo è stato aggiunto un supporto rimovibile. Il **membro \_ dati dbch** è un puntatore a una struttura del [**\_ \_ \_ contesto di modifica dei supporti di classe**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) . Il membro **NewState** fornisce informazioni sullo stato. Il valore **MediaUnavailable** , ad esempio, indica che il supporto non è disponibile, ad esempio a causa di una sessione di registrazione attiva.

**Windows XP:** Il **membro \_ dati dbch** è un valore **ULONG** che rappresenta il numero di volte in cui il supporto è stato modificato dall'avvio del sistema.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**\_richiesta di \_ \_ espulsione del supporto io GUID \_**
</dt> <dd> <dl> <dt>

d07433d1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



L'unità del supporto rimovibile ha ricevuto una richiesta dall'utente per estrarre lo slot o i supporti specificati.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**\_ \_ rimozione supporti i/o GUID \_**
</dt> <dd> <dl> <dt>

d07433c1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Il supporto rimovibile è stato rimosso dal dispositivo o non è disponibile. Il **membro \_ dati dbch** è un puntatore a una struttura del [**\_ \_ \_ contesto di modifica dei supporti di classe**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) . Il membro **NewState** fornisce informazioni sullo stato. Il valore **MediaUnavailable** , ad esempio, indica che il supporto non è disponibile, ad esempio a causa di una sessione di registrazione attiva.

**Windows XP:** Il **membro \_ dati dbch** è un valore **ULONG** che rappresenta il numero di volte in cui il supporto è stato modificato dall'avvio del sistema.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**\_ \_ Modifica volume i/o GUID \_**
</dt> <dd> <dl> <dt>

7373654a-812a-11d0-bec7-08002be2092f
</dt> <dt>



L'etichetta del volume è cambiata.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**\_ \_ \_ dimensioni modifica volume \_ i/o GUID**
</dt> <dd> <dl> <dt>

3a1625be-ad03-49f1-8ef8-6bbac182d1fd
</dt> <dt>



Le dimensioni del file system nel volume sono state modificate.

**Windows Server 2003 e Windows XP:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**\_ \_ smontaggio volume i/o GUID \_**
</dt> <dd> <dl> <dt>

d16a55e8-1059-11d2-8ffd-00a0c9a06d32
</dt> <dt>



È in corso un tentativo di smontaggio del volume. È necessario chiudere tutti gli handle di file e directory nel volume. Questo evento non sarà necessariamente preceduto da un evento **di \_ \_ \_ blocco del volume io GUID** .


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**\_ \_ smontaggio del volume io GUID \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

e3c5b178-105d-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Tentativo di smontaggio di un volume non riuscito. Questo problema si verifica spesso perché un altro processo non è riuscito a rispondere a un avviso di **\_ \_ \_ smontaggio del volume** i/o di GUID chiudendo gli handle in attesa Poiché lo smontaggio non è riuscito, è possibile riaprire gli handle per il volume interessato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**\_ \_ \_ \_ modifica stato FVE volume \_ i/o GUID**
</dt> <dd> <dl> <dt>

062998b2-ee1f-4b6a-b857-e76cbbe9a6da
</dt> <dt>



Lo stato Crittografia unità BitLocker del volume è stato modificato. Questo evento viene segnalato quando BitLocker è abilitato o disabilitato oppure quando viene avviata, terminata, sospesa o ripresa la crittografia.

**Windows Server 2003 e Windows XP:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**\_ \_ blocco volume io \_ GUID**
</dt> <dd> <dl> <dt>

50708874-C9AF-11D1-8FEF-00a0c9a06d32
</dt> <dt>



Un altro processo sta tentando di bloccare il volume. È necessario chiudere tutti gli handle di file e directory nel volume.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**\_blocco del \_ volume io GUID \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32
</dt> <dt>



Tentativo di bloccare un volume non riuscito. Questo problema si verifica spesso perché un altro processo non è riuscito a rispondere a un evento di **\_ \_ \_ blocco del volume io GUID** chiudendo gli handle in attesa. Poiché il blocco non è riuscito, è possibile riaprire gli handle per il volume interessato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**\_montaggio del \_ volume \_ io GUID**
</dt> <dd> <dl> <dt>

b5804878-1a96-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Il volume è stato montato da un altro processo. È possibile aprire uno o più handle.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**\_ \_ \_ modifica nome volume \_ i/o GUID**
</dt> <dd> <dl> <dt>

2de97f83-4c06-11d2-a532-00609713055a
</dt> <dt>



Il nome del volume è stato modificato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**VOLUME i/o GUID \_ \_ \_ necessario \_ chkdsk**
</dt> <dd> <dl> <dt>

799a0960-0a0b-4e03-ad88-2fa7c6ce748a
</dt> <dt>



Un file system ha rilevato un danneggiamento del volume. L'applicazione deve eseguire CHKDSK sul volume o inviare una notifica all'utente.

**Windows Server 2003 e Windows XP:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**\_modifica della \_ \_ configurazione fisica \_ del volume io GUID \_**
</dt> <dd> <dl> <dt>

2de97f84-4c06-11d2-a532-00609713055a
</dt> <dt>



Il trucco fisico o lo stato fisico corrente del volume è stato modificato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**\_volume io del GUID \_ preparazione dell' \_ \_ espulsione**
</dt> <dd> <dl> <dt>

c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6
</dt> <dt>



Il file system sta preparando il disco da estrarre. Ad esempio, il file system sta arrestando un'operazione di formattazione in background o chiudendo la sessione in un supporto write-once.

**Windows Server 2003 e Windows XP:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**\_ \_ \_ \_ modifica ID univoco del volume io del GUID \_**
</dt> <dd> <dl> <dt>

af39da42-6622-41f5-970b-139d092fa3d9
</dt> <dt>



L'identificatore univoco del volume è stato modificato. Per altre informazioni sull'identificatore univoco, vedere [**IOCTL \_ MOUNTDEV \_ query \_ Unique \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo valore non è supportato fino a Windows Server 2008 R2 e Windows 7.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**\_ \_ sblocco volume i/o GUID \_**
</dt> <dd> <dl> <dt>

9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32
</dt> <dt>



Il volume è stato sbloccato da un altro processo. È possibile aprire uno o più handle.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**VOLUME i/o GUID \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

873113ca-1486-4508-82ac-c3b2e5297aaa
</dt> <dt>



Il supporto si sta esaurendo. Questo evento viene inviato quando un file system determina che la frequenza degli errori in un volume è troppo elevata o lo spazio di sostituzione del difetto è quasi esaurito.

**Windows Server 2003 e Windows XP:** Questo valore non è supportato.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Gli eventi di smontaggio del **\_ \_ volume \_** di i/o di GUID e smontaggio del volume di i/o GUID sono correlati, così come il **\_ \_ \_ blocco** del volume di i/o GUID e l'evento di **\_ \_ \_ blocco \_ del volume** i **\_ \_ \_ \_** Gli eventi di **\_ \_ \_ blocco** del volume i/o del GUID e del volume di i/o GUID indicano che è in corso il tentativo di un'operazione. **\_ \_ \_** È necessario agire sulla notifica degli eventi e registrare l'azione eseguita. Lo SMONTAggio del volume di i/o del **GUID \_ \_ \_ \_ non riuscito** e gli eventi di blocco del volume di i/o **GUID \_ \_ \_ \_** non sono riusciti. È quindi possibile usare il record per annullare le azioni eseguite in risposta all'operazione.

Il membro **dbch \_ hdevnotify** della struttura dell' [**\_ \_ handle di broadcast dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) indica il dispositivo interessato. Si noti che questo è l'handle di notifica del dispositivo restituito da [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), non un handle del volume. Per eseguire operazioni sul volume, eseguire il mapping di questo handle all'handle del volume corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>IoEvent. h</dt> </dl> |



 


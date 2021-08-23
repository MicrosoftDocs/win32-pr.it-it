---
description: Le applicazioni, inclusi i servizi, possono registrarsi per ricevere la notifica degli eventi del dispositivo.
ms.assetid: c89da4ac-57dd-4d95-ac86-3eb137dee0bc
title: Eventi del dispositivo (IoEvent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a44e6160ef3a59821e5d2b2a3d4e42ee1d14d5c2fb7deda689fb1c9c3186b428
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076255"
---
# <a name="device-events-ioeventh"></a>Eventi del dispositivo (IoEvent.h)

Le applicazioni, inclusi i servizi, possono registrarsi per ricevere la notifica degli eventi del dispositivo. Ad esempio, un servizio di catalogo può ricevere un avviso di volumi montati o smontati in modo da poter modificare i percorsi dei file nel volume. Il sistema notifica a un'applicazione che si è verificato un evento del dispositivo inviando all'applicazione [**un messaggio \_ DEVICECHANGE WM.**](wm-devicechange.md) Il sistema notifica a un servizio che si è verificato un evento del dispositivo richiamando la funzione del gestore eventi del servizio, [**HandlerEx.**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)

Per ricevere le notifiche degli eventi del dispositivo, chiamare la [**funzione RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) con una [**struttura DEV BROADCAST \_ \_ HANDLE.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) Assicurarsi di impostare il membro **\_ dell'handle dbch** sull'handle di dispositivo ottenuto dalla [**funzione CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Impostare anche il **membro dbch \_ devicetype** su **DBT \_ DEVTYP \_ HANDLE**. La funzione restituisce un handle di notifica del dispositivo. Si noti che non corrisponde all'handle di volume.

Quando l'applicazione riceve una notifica, se il tipo di evento è [DBT \_ CUSTOMEVENT](dbt-customevent.md), è possibile che sia stato ricevuto uno degli eventi del dispositivo definiti in IoEvent.h. Per determinare se si è verificato uno di questi eventi, seguire questa procedura.

1.  Considerare i dati dell'evento come [**una struttura DEV BROADCAST \_ \_ HDR.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) Verificare che il **membro \_ dbch devicetype** sia impostato su **DBT \_ DEVTYP \_ HANDLE**.
2.  Se **dbch \_ devicetype è** **DBT \_ DEVTYP \_ HANDLE,** i dati dell'evento sono in realtà un puntatore a una [**struttura DEV BROADCAST \_ \_ HANDLE.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle)
3.  Confrontare il **membro \_ dbch eventguid** con **i GUID** elencati nella tabella seguente usando la [**funzione IsEqualGUID.**](/windows/win32/api/guiddef/nf-guiddef-isequalguid)

<dl> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID \_ IO \_ CDROM \_ EXCLUSIVE \_ LOCK**
</dt> <dd> <dl> <dt>

bc56c139-7a10-47ee-a294-4c6a38f0149a
</dt> <dt>



Il dispositivo CD-ROM è stato bloccato per l'accesso esclusivo.

**Windows Server 2003 e Windows XP:** Il supporto per questo valore richiede IMAPI 2.0. Per altre informazioni, vedere [IMAGE Mastering API](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID \_ IO \_ CDROM \_ EXCLUSIVE \_ UNLOCK**
</dt> <dd> <dl> <dt>

a3b6d27d-5e35-4885-81e5-ee18c00ed779
</dt> <dt>



Un dispositivo CD-ROM bloccato per l'accesso esclusivo è stato sbloccato.

**Windows Server 2003 e Windows XP:** Il supporto per questo valore richiede IMAPI 2.0. Per altre informazioni, vedere [IMAGE Mastering API](/windows/desktop/imapi/portal).


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**GUID \_ \_ I/O DEVICE \_ BECOMING \_ READY**
</dt> <dd> <dl> <dt>

d07433f0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



È in corso lo spin-up multimediale.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**RICHIESTA \_ ESTERNA DEL DISPOSITIVO \_ \_ I/O \_ GUID**
</dt> <dd> <dl> <dt>

d07433d0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Esistono diverse possibili cause per questo evento. Per altre informazioni, vedere la specifica T10 MMC del comando GET EVENT STATUS NOTIFICATION all'indirizzo [https://www.t10.org/](https://www.t10.org/) .


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**GUID \_ IO \_ MEDIA \_ ARRIVAL**
</dt> <dd> <dl> <dt>

d07433c0-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Il supporto rimovibile è stato aggiunto al dispositivo. Il **membro dati dbch \_** è un puntatore a una struttura CLASS MEDIA CHANGE [**\_ \_ \_ CONTEXT.**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) Il **membro NewState** fornisce informazioni sullo stato. Ad esempio, il valore **MediaUnavailable** indica che il supporto non è disponibile, ad esempio a causa di una sessione di registrazione attiva.

**Windows XP:** Il **membro dati dbch \_** è un valore **ULONG** che rappresenta il numero di volte in cui il supporto è stato modificato dall'avvio del sistema.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**GUID \_ IO \_ MEDIA \_ EJECT \_ REQUEST**
</dt> <dd> <dl> <dt>

d07433d1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



L'unità del supporto rimovibile ha ricevuto una richiesta dall'utente di rimuovere lo slot o il supporto specificato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**RIMOZIONE \_ DEI SUPPORTI DI \_ I/O GUID \_**
</dt> <dd> <dl> <dt>

d07433c1-a98e-11d2-917a-00a0c9068ff3
</dt> <dt>



Il supporto rimovibile è stato rimosso dal dispositivo o non è disponibile. Il **membro dati dbch \_** è un puntatore a una struttura CLASS MEDIA CHANGE [**\_ \_ \_ CONTEXT.**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) Il **membro NewState** fornisce informazioni sullo stato. Ad esempio, il valore **MediaUnavailable** indica che il supporto non è disponibile, ad esempio a causa di una sessione di registrazione attiva.

**Windows XP:** Il **membro dati dbch \_** è un valore **ULONG** che rappresenta il numero di volte in cui il supporto è stato modificato dall'avvio del sistema.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**MODIFICA DEL \_ \_ VOLUME I/O \_ GUID**
</dt> <dd> <dl> <dt>

7373654a-812a-11d0-bec7-08002be2092f
</dt> <dt>



L'etichetta del volume è stata modificata.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**GUID \_ \_ I/O VOLUME \_ CHANGE \_ SIZE**
</dt> <dd> <dl> <dt>

3a1625be-ad03-49f1-8ef8-6bbac182d1fd
</dt> <dt>



Le dimensioni del file system nel volume sono state modificate.

**Windows Server 2003 e Windows XP:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**GUID \_ \_ I/O VOLUME \_ DISMOUNT**
</dt> <dd> <dl> <dt>

d16a55e8-1059-11d2-8ffd-00a0c9a06d32
</dt> <dt>



È in corso un tentativo di smontare il volume. È necessario chiudere tutti gli handle per i file e le directory nel volume. Questo evento non sarà necessariamente preceduto da un evento **\_ VOLUME LOCK \_ I/O \_ GUID.**


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**\_DISMOUNT VOLUME \_ I/O GUID \_ NON \_ RIUSCITO**
</dt> <dd> <dl> <dt>

e3c5b178-105d-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Tentativo di smontare un volume non riuscito. Ciò si verifica spesso perché un altro processo non è riuscito a rispondere a un avviso **\_ \_ \_ DISMOUNT VOLUME I/O GUID** chiudendo gli handle in sospeso. Poiché lo smontaggio non è riuscito, è possibile riaprire tutti gli handle per il volume interessato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**GUID \_ \_ I/O VOLUME \_ FVE \_ STATUS \_ CHANGE**
</dt> <dd> <dl> <dt>

062998b2-ee1f-4b6a-b857-e76cbbe9a6da
</dt> <dt>



Lo stato di Crittografia unità BitLocker del volume è stato modificato. Questo evento viene segnalato quando BitLocker è abilitato o disabilitato o quando la crittografia inizia, termina, sospende o riprende.

**Windows Server 2003 e Windows XP:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID \_ \_ I/O VOLUME \_ LOCK**
</dt> <dd> <dl> <dt>

50708874-c9af-11d1-8fef-00a0c9a06d32
</dt> <dt>



Un altro processo sta tentando di bloccare il volume. È necessario chiudere tutti gli handle per i file e le directory nel volume.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**GUID \_ \_ I/O VOLUME \_ LOCK \_ FAILED**
</dt> <dd> <dl> <dt>

ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32
</dt> <dt>



Tentativo di blocco di un volume non riuscito. Questo errore si verifica spesso perché un altro processo non è riuscito a rispondere a un evento **\_ VOLUME \_ \_ LOCK I/O GUID** chiudendo gli handle in sospeso. Poiché il blocco non è riuscito, è possibile riaprire tutti gli handle per il volume interessato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**GUID \_ \_ I/O VOLUME \_ MOUNT**
</dt> <dd> <dl> <dt>

b5804878-1a96-11d2-8ffd-00a0c9a06d32
</dt> <dt>



Il volume è stato montato da un altro processo. È possibile aprire uno o più handle.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**MODIFICA \_ DEL NOME DEL VOLUME \_ \_ I/O \_ GUID**
</dt> <dd> <dl> <dt>

2de97f83-4c06-11d2-a532-00609713055a
</dt> <dt>



Il nome del volume è stato modificato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**GUID \_ \_ I/O VOLUME \_ \_ NEED CHKDSK**
</dt> <dd> <dl> <dt>

799a0960-0a0b-4e03-ad88-2fa7c6ce748a
</dt> <dt>



Un file system ha rilevato un danneggiamento nel volume. L'applicazione deve eseguire CHKDSK nel volume o notificare all'utente di eseguire questa operazione.

**Windows Server 2003 e Windows XP:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**MODIFICA DELLA \_ CONFIGURAZIONE FISICA DEL VOLUME \_ \_ \_ I/O \_ GUID**
</dt> <dd> <dl> <dt>

2de97f84-4c06-11d2-a532-00609713055a
</dt> <dt>



Lo stato fisico fisico o fisico corrente del volume è stato modificato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID \_ \_ I/O VOLUME \_ PREPARING \_ EJECT**
</dt> <dd> <dl> <dt>

c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6
</dt> <dt>



Il file system sta preparando il disco da espulso. Ad esempio, il file system sta arrestando un'operazione di formattazione in background o chiudendo la sessione su supporti write-once.

**Windows Server 2003 e Windows XP:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**MODIFICA \_ \_ DELL'ID UNIVOCO DEL VOLUME \_ \_ I/O \_ GUID**
</dt> <dd> <dl> <dt>

af39da42-6622-41f5-970b-139d092fa3d9
</dt> <dt>



L'identificatore univoco del volume è stato modificato. Per altre informazioni sull'identificatore univoco, vedere [**IOCTL \_ MOUNTDEV \_ QUERY UNIQUE \_ \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo valore non è supportato fino a Windows Server 2008 R2 e Windows 7.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**SBLOCCO \_ VOLUME \_ I/O GUID \_**
</dt> <dd> <dl> <dt>

9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32
</dt> <dt>



Il volume è stato sbloccato da un altro processo. È possibile aprire uno o più handle.


</dt> </dl> </dd> <dt>

<span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**VOLUME \_ DI \_ I/O GUID \_ IN \_ USCITA**
</dt> <dd> <dl> <dt>

873113ca-1486-4508-82ac-c3b2e5297aaa
</dt> <dt>



I supporti si sta usticando. Questo evento viene inviato quando un file system determina che la frequenza di errore in un volume è troppo elevata o lo spazio di sostituzione dei difetti è quasi esaurito.

**Windows Server 2003 e Windows XP:** Questo valore non è supportato.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Gli **eventi GUID IO VOLUME \_ \_ \_ DISMOUNT** e **GUID IO VOLUME \_ \_ \_ DISMOUNT \_ FAILED** sono correlati, così come l'evento **GUID IO VOLUME \_ \_ \_ LOCK** e **GUID IO VOLUME LOCK \_ \_ \_ \_ FAILED.** Gli **eventi GUID IO VOLUME \_ \_ \_ DISMOUNT** e **GUID IO VOLUME \_ \_ \_ LOCK** indicano che è in corso un'operazione. È necessario agire sulla notifica dell'evento e registrare l'azione eseguita. Gli **eventi GUID IO VOLUME \_ \_ \_ DISMOUNT \_ FAILED e** GUID IO VOLUME LOCK **\_ \_ \_ \_ FAILED** indicano che l'operazione non è riuscita. È quindi possibile usare il record per annullare le azioni eseguite in risposta all'operazione.

Il **membro dbch \_ hdevnotify** della struttura [**DEV BROADCAST \_ \_ HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) indica il dispositivo interessato. Si noti che si tratta dell'handle di notifica del dispositivo restituito [**da RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)e non da un handle di volume. Per eseguire operazioni sul volume, eseguire il mapping di questo handle all'handle di volume corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>IoEvent.h</dt> </dl> |



 


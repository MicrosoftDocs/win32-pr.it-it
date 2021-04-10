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
# <a name="device-events-ioeventh"></a><span data-ttu-id="3f679-103">Eventi dispositivo (IoEvent. h)</span><span class="sxs-lookup"><span data-stu-id="3f679-103">Device Events (IoEvent.h)</span></span>

<span data-ttu-id="3f679-104">Le applicazioni, inclusi i servizi, possono registrarsi per ricevere notifiche di eventi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f679-104">Applications, including services, can register to receive notification of device events.</span></span> <span data-ttu-id="3f679-105">Ad esempio, un servizio di catalogo può ricevere l'avviso dei volumi montati o smontati, in modo da poter modificare i percorsi dei file nel volume.</span><span class="sxs-lookup"><span data-stu-id="3f679-105">For example, a catalog service can receive notice of volumes being mounted or dismounted so it can adjust the paths to files on the volume.</span></span> <span data-ttu-id="3f679-106">Il sistema notifica a un'applicazione che si è verificato un evento del dispositivo inviando all'applicazione un messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="3f679-106">The system notifies an application that a device event has occurred by sending the application a [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="3f679-107">Il sistema notifica a un servizio che si è verificato un evento del dispositivo richiamando la funzione del gestore eventi del servizio, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span><span class="sxs-lookup"><span data-stu-id="3f679-107">The system notifies a service that a device event has occurred by invoking the service's event handler function, [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex).</span></span>

<span data-ttu-id="3f679-108">Per ricevere le notifiche degli eventi del dispositivo, chiamare la funzione [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) con una struttura dell' [**handle di \_ trasmissione \_ dello sviluppo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .</span><span class="sxs-lookup"><span data-stu-id="3f679-108">To receive device event notices, call the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function with a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span> <span data-ttu-id="3f679-109">Assicurarsi di impostare il membro **dell' \_ handle dbch** sull'handle di dispositivo ottenuto dalla funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="3f679-109">Be sure to set the **dbch\_handle** member to the device handle obtained from the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="3f679-110">Impostare anche il membro **dbch \_ DeviceType** su **DBT \_ DEVTYP \_ handle**.</span><span class="sxs-lookup"><span data-stu-id="3f679-110">Also, set the **dbch\_devicetype** member to **DBT\_DEVTYP\_HANDLE**.</span></span> <span data-ttu-id="3f679-111">La funzione restituisce un handle di notifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f679-111">The function returns a device notification handle.</span></span> <span data-ttu-id="3f679-112">Si noti che questo non è lo stesso dell'handle del volume.</span><span class="sxs-lookup"><span data-stu-id="3f679-112">Note that this is not the same as the volume handle.</span></span>

<span data-ttu-id="3f679-113">Quando l'applicazione riceve una notifica, se il tipo di evento è [DBT \_ CUSTOMEVENT](dbt-customevent.md), è possibile che sia stato ricevuto uno degli eventi del dispositivo definiti in IoEvent. h.</span><span class="sxs-lookup"><span data-stu-id="3f679-113">When your application receives notification, if the event type is [DBT\_CUSTOMEVENT](dbt-customevent.md), you may have received one of the device events defined in IoEvent.h.</span></span> <span data-ttu-id="3f679-114">Per determinare se si è verificato uno di questi eventi, attenersi alla procedura riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="3f679-114">To determine if one of these events has occurred, use the following steps.</span></span>

1.  <span data-ttu-id="3f679-115">Considerare i dati dell'evento come una struttura [**\_ \_ HDR di sviluppo broadcast**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) .</span><span class="sxs-lookup"><span data-stu-id="3f679-115">Treat the event data as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="3f679-116">Verificare che il membro **dbch \_ DeviceType** sia impostato su **DBT \_ DEVTYP \_ handle**.</span><span class="sxs-lookup"><span data-stu-id="3f679-116">Verify that the **dbch\_devicetype** member is set to **DBT\_DEVTYP\_HANDLE**.</span></span>
2.  <span data-ttu-id="3f679-117">Se **dbch \_ DeviceType** è **DBT \_ DEVTYP \_ handle**, i dati dell'evento sono effettivamente un puntatore a una struttura di [**\_ \_ handle di broadcast di sviluppo**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) .</span><span class="sxs-lookup"><span data-stu-id="3f679-117">If **dbch\_devicetype** is **DBT\_DEVTYP\_HANDLE**, the event data is really a pointer to a [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure.</span></span>
3.  <span data-ttu-id="3f679-118">Confrontare il membro **dbch \_ EventGuid** con il **GUID** elencato nella tabella seguente usando la funzione [**IsEqualGuid**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) .</span><span class="sxs-lookup"><span data-stu-id="3f679-118">Compare the **dbch\_eventguid** member to the **GUID** s listed in the following table using the [**IsEqualGUID**](/windows/win32/api/guiddef/nf-guiddef-isequalguid) function.</span></span>

<dl> <dt>

<span data-ttu-id="3f679-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**\_ \_ \_ blocco esclusivo cdrom \_ i/o di GUID**</span><span class="sxs-lookup"><span data-stu-id="3f679-119"><span id="GUID_IO_CDROM_EXCLUSIVE_LOCK"></span><span id="guid_io_cdrom_exclusive_lock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span><span class="sxs-lookup"><span data-stu-id="3f679-120">bc56c139-7a10-47ee-a294-4c6a38f0149a</span></span>
</dt> <dt>



<span data-ttu-id="3f679-121">Il dispositivo CD-ROM è stato bloccato per l'accesso esclusivo.</span><span class="sxs-lookup"><span data-stu-id="3f679-121">The CD-ROM device has been locked for exclusive access.</span></span>

<span data-ttu-id="3f679-122">**Windows Server 2003 e Windows XP:** Il supporto per questo valore richiede IMAPi 2,0.</span><span class="sxs-lookup"><span data-stu-id="3f679-122">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="3f679-123">Per altre informazioni, vedere [API di Image Mastering](/windows/desktop/imapi/portal).</span><span class="sxs-lookup"><span data-stu-id="3f679-123">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**\_ \_ \_ sblocco esclusivo GUID io \_ CDROM**</span><span class="sxs-lookup"><span data-stu-id="3f679-124"><span id="GUID_IO_CDROM_EXCLUSIVE_UNLOCK"></span><span id="guid_io_cdrom_exclusive_unlock"></span>**GUID\_IO\_CDROM\_EXCLUSIVE\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span><span class="sxs-lookup"><span data-stu-id="3f679-125">a3b6d27d-5e35-4885-81e5-ee18c00ed779</span></span>
</dt> <dt>



<span data-ttu-id="3f679-126">Un dispositivo CD-ROM bloccato per l'accesso esclusivo è stato sbloccato.</span><span class="sxs-lookup"><span data-stu-id="3f679-126">A CD-ROM device that was locked for exclusive access has been unlocked.</span></span>

<span data-ttu-id="3f679-127">**Windows Server 2003 e Windows XP:** Il supporto per questo valore richiede IMAPi 2,0.</span><span class="sxs-lookup"><span data-stu-id="3f679-127">**Windows Server 2003 and Windows XP:** Support for this value requires IMAPI 2.0.</span></span> <span data-ttu-id="3f679-128">Per altre informazioni, vedere [API di Image Mastering](/windows/desktop/imapi/portal).</span><span class="sxs-lookup"><span data-stu-id="3f679-128">For more information, see [Image Mastering API](/windows/desktop/imapi/portal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**il dispositivo di i/o GUID \_ \_ \_ diventa \_ pronto**</span><span class="sxs-lookup"><span data-stu-id="3f679-129"><span id="GUID_IO_DEVICE_BECOMING_READY"></span><span id="guid_io_device_becoming_ready"></span>**GUID\_IO\_DEVICE\_BECOMING\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="3f679-130">d07433f0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="3f679-131">La rotazione dei supporti è in corso.</span><span class="sxs-lookup"><span data-stu-id="3f679-131">Media spin-up is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**\_ \_ richiesta esterna del dispositivo io \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="3f679-132"><span id="GUID_IO_DEVICE_EXTERNAL_REQUEST"></span><span id="guid_io_device_external_request"></span>**GUID\_IO\_DEVICE\_EXTERNAL\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="3f679-133">d07433d0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="3f679-134">Esistono diverse cause possibili per questo evento. Per ulteriori informazioni, vedere la specifica di T10 MMC del comando GET EVENT STATUS NOTIFICATION, all'indirizzo [https://www.t10.org/](https://www.t10.org/) .</span><span class="sxs-lookup"><span data-stu-id="3f679-134">There are several possible causes for this event; for more information, refer to T10 MMC specification of the GET EVENT STATUS NOTIFICATION Command, at [https://www.t10.org/](https://www.t10.org/).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**\_arrivo del \_ supporto i/o GUID \_**</span><span class="sxs-lookup"><span data-stu-id="3f679-135"><span id="GUID_IO_MEDIA_ARRIVAL"></span><span id="guid_io_media_arrival"></span>**GUID\_IO\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="3f679-136">d07433c0-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="3f679-137">Al dispositivo è stato aggiunto un supporto rimovibile.</span><span class="sxs-lookup"><span data-stu-id="3f679-137">Removable media has been added to the device.</span></span> <span data-ttu-id="3f679-138">Il **membro \_ dati dbch** è un puntatore a una struttura del [**\_ \_ \_ contesto di modifica dei supporti di classe**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) .</span><span class="sxs-lookup"><span data-stu-id="3f679-138">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="3f679-139">Il membro **NewState** fornisce informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="3f679-139">The **NewState** member provides status information.</span></span> <span data-ttu-id="3f679-140">Il valore **MediaUnavailable** , ad esempio, indica che il supporto non è disponibile, ad esempio a causa di una sessione di registrazione attiva.</span><span class="sxs-lookup"><span data-stu-id="3f679-140">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="3f679-141">**Windows XP:** Il **membro \_ dati dbch** è un valore **ULONG** che rappresenta il numero di volte in cui il supporto è stato modificato dall'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="3f679-141">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**\_richiesta di \_ \_ espulsione del supporto io GUID \_**</span><span class="sxs-lookup"><span data-stu-id="3f679-142"><span id="GUID_IO_MEDIA_EJECT_REQUEST"></span><span id="guid_io_media_eject_request"></span>**GUID\_IO\_MEDIA\_EJECT\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="3f679-143">d07433d1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="3f679-144">L'unità del supporto rimovibile ha ricevuto una richiesta dall'utente per estrarre lo slot o i supporti specificati.</span><span class="sxs-lookup"><span data-stu-id="3f679-144">The removable media's drive has received a request from the user to eject the specified slot or media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**\_ \_ rimozione supporti i/o GUID \_**</span><span class="sxs-lookup"><span data-stu-id="3f679-145"><span id="GUID_IO_MEDIA_REMOVAL"></span><span id="guid_io_media_removal"></span>**GUID\_IO\_MEDIA\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span><span class="sxs-lookup"><span data-stu-id="3f679-146">d07433c1-a98e-11d2-917a-00a0c9068ff3</span></span>
</dt> <dt>



<span data-ttu-id="3f679-147">Il supporto rimovibile è stato rimosso dal dispositivo o non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="3f679-147">Removable media has been removed from the device or is unavailable.</span></span> <span data-ttu-id="3f679-148">Il **membro \_ dati dbch** è un puntatore a una struttura del [**\_ \_ \_ contesto di modifica dei supporti di classe**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) .</span><span class="sxs-lookup"><span data-stu-id="3f679-148">The **dbch\_data** member is a pointer to a [**CLASS\_MEDIA\_CHANGE\_CONTEXT**](/windows/desktop/api/WinIoCtl/ns-winioctl-class_media_change_context) structure.</span></span> <span data-ttu-id="3f679-149">Il membro **NewState** fornisce informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="3f679-149">The **NewState** member provides status information.</span></span> <span data-ttu-id="3f679-150">Il valore **MediaUnavailable** , ad esempio, indica che il supporto non è disponibile, ad esempio a causa di una sessione di registrazione attiva.</span><span class="sxs-lookup"><span data-stu-id="3f679-150">For example, a value of **MediaUnavailable** indicates that the media is not available (for example, due to an active recording session).</span></span>

<span data-ttu-id="3f679-151">**Windows XP:** Il **membro \_ dati dbch** è un valore **ULONG** che rappresenta il numero di volte in cui il supporto è stato modificato dall'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="3f679-151">**Windows XP:** The **dbch\_data** member is a **ULONG** value that represents the number of times that media has been changed since system startup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**\_ \_ Modifica volume i/o GUID \_**</span><span class="sxs-lookup"><span data-stu-id="3f679-152"><span id="GUID_IO_VOLUME_CHANGE"></span><span id="guid_io_volume_change"></span>**GUID\_IO\_VOLUME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-153">7373654a-812a-11d0-bec7-08002be2092f</span><span class="sxs-lookup"><span data-stu-id="3f679-153">7373654a-812a-11d0-bec7-08002be2092f</span></span>
</dt> <dt>



<span data-ttu-id="3f679-154">L'etichetta del volume è cambiata.</span><span class="sxs-lookup"><span data-stu-id="3f679-154">The volume label has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**\_ \_ \_ dimensioni modifica volume \_ i/o GUID**</span><span class="sxs-lookup"><span data-stu-id="3f679-155"><span id="GUID_IO_VOLUME_CHANGE_SIZE"></span><span id="guid_io_volume_change_size"></span>**GUID\_IO\_VOLUME\_CHANGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-156">3a1625be-ad03-49f1-8ef8-6bbac182d1fd</span><span class="sxs-lookup"><span data-stu-id="3f679-156">3a1625be-ad03-49f1-8ef8-6bbac182d1fd</span></span>
</dt> <dt>



<span data-ttu-id="3f679-157">Le dimensioni del file system nel volume sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="3f679-157">The size of the file system on the volume has changed.</span></span>

<span data-ttu-id="3f679-158">**Windows Server 2003 e Windows XP:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3f679-158">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**\_ \_ smontaggio volume i/o GUID \_**</span><span class="sxs-lookup"><span data-stu-id="3f679-159"><span id="GUID_IO_VOLUME_DISMOUNT"></span><span id="guid_io_volume_dismount"></span>**GUID\_IO\_VOLUME\_DISMOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="3f679-160">d16a55e8-1059-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="3f679-161">È in corso un tentativo di smontaggio del volume.</span><span class="sxs-lookup"><span data-stu-id="3f679-161">An attempt to dismount the volume is in progress.</span></span> <span data-ttu-id="3f679-162">È necessario chiudere tutti gli handle di file e directory nel volume.</span><span class="sxs-lookup"><span data-stu-id="3f679-162">You should close all handles to files and directories on the volume.</span></span> <span data-ttu-id="3f679-163">Questo evento non sarà necessariamente preceduto da un evento **di \_ \_ \_ blocco del volume io GUID** .</span><span class="sxs-lookup"><span data-stu-id="3f679-163">This event will not necessarily be preceded by a **GUID\_IO\_VOLUME\_LOCK** event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**\_ \_ smontaggio del volume io GUID \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="3f679-164"><span id="GUID_IO_VOLUME_DISMOUNT_FAILED"></span><span id="guid_io_volume_dismount_failed"></span>**GUID\_IO\_VOLUME\_DISMOUNT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="3f679-165">e3c5b178-105d-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="3f679-166">Tentativo di smontaggio di un volume non riuscito.</span><span class="sxs-lookup"><span data-stu-id="3f679-166">An attempt to dismount a volume failed.</span></span> <span data-ttu-id="3f679-167">Questo problema si verifica spesso perché un altro processo non è riuscito a rispondere a un avviso di **\_ \_ \_ smontaggio del volume** i/o di GUID chiudendo gli handle in attesa</span><span class="sxs-lookup"><span data-stu-id="3f679-167">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_DISMOUNT** notice by closing its outstanding handles.</span></span> <span data-ttu-id="3f679-168">Poiché lo smontaggio non è riuscito, è possibile riaprire gli handle per il volume interessato.</span><span class="sxs-lookup"><span data-stu-id="3f679-168">Because the dismount failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**\_ \_ \_ \_ modifica stato FVE volume \_ i/o GUID**</span><span class="sxs-lookup"><span data-stu-id="3f679-169"><span id="GUID_IO_VOLUME_FVE_STATUS_CHANGE"></span><span id="guid_io_volume_fve_status_change"></span>**GUID\_IO\_VOLUME\_FVE\_STATUS\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-170">062998b2-ee1f-4b6a-b857-e76cbbe9a6da</span><span class="sxs-lookup"><span data-stu-id="3f679-170">062998b2-ee1f-4b6a-b857-e76cbbe9a6da</span></span>
</dt> <dt>



<span data-ttu-id="3f679-171">Lo stato Crittografia unità BitLocker del volume è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="3f679-171">The volume's BitLocker Drive Encryption status has changed.</span></span> <span data-ttu-id="3f679-172">Questo evento viene segnalato quando BitLocker è abilitato o disabilitato oppure quando viene avviata, terminata, sospesa o ripresa la crittografia.</span><span class="sxs-lookup"><span data-stu-id="3f679-172">This event is signaled when BitLocker is enabled or disabled, or when encryption begins, ends, pauses, or resumes.</span></span>

<span data-ttu-id="3f679-173">**Windows Server 2003 e Windows XP:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3f679-173">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**\_ \_ blocco volume io \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="3f679-174"><span id="GUID_IO_VOLUME_LOCK"></span><span id="guid_io_volume_lock"></span>**GUID\_IO\_VOLUME\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-175">50708874-C9AF-11D1-8FEF-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="3f679-175">50708874-c9af-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="3f679-176">Un altro processo sta tentando di bloccare il volume.</span><span class="sxs-lookup"><span data-stu-id="3f679-176">Another process is attempting to lock the volume.</span></span> <span data-ttu-id="3f679-177">È necessario chiudere tutti gli handle di file e directory nel volume.</span><span class="sxs-lookup"><span data-stu-id="3f679-177">You should close all handles to files and directories on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**\_blocco del \_ volume io GUID \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="3f679-178"><span id="GUID_IO_VOLUME_LOCK_FAILED"></span><span id="guid_io_volume_lock_failed"></span>**GUID\_IO\_VOLUME\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="3f679-179">ae2eed10-0ba8-11d2-8ffb-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="3f679-180">Tentativo di bloccare un volume non riuscito.</span><span class="sxs-lookup"><span data-stu-id="3f679-180">An attempt to lock a volume failed.</span></span> <span data-ttu-id="3f679-181">Questo problema si verifica spesso perché un altro processo non è riuscito a rispondere a un evento di **\_ \_ \_ blocco del volume io GUID** chiudendo gli handle in attesa.</span><span class="sxs-lookup"><span data-stu-id="3f679-181">This often happens because another process failed to respond to a **GUID\_IO\_VOLUME\_LOCK** event by closing its outstanding handles.</span></span> <span data-ttu-id="3f679-182">Poiché il blocco non è riuscito, è possibile riaprire gli handle per il volume interessato.</span><span class="sxs-lookup"><span data-stu-id="3f679-182">Because the lock failed, you may reopen any handles to the affected volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**\_montaggio del \_ volume \_ io GUID**</span><span class="sxs-lookup"><span data-stu-id="3f679-183"><span id="GUID_IO_VOLUME_MOUNT"></span><span id="guid_io_volume_mount"></span>**GUID\_IO\_VOLUME\_MOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="3f679-184">b5804878-1a96-11d2-8ffd-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="3f679-185">Il volume è stato montato da un altro processo.</span><span class="sxs-lookup"><span data-stu-id="3f679-185">The volume has been mounted by another process.</span></span> <span data-ttu-id="3f679-186">È possibile aprire uno o più handle.</span><span class="sxs-lookup"><span data-stu-id="3f679-186">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**\_ \_ \_ modifica nome volume \_ i/o GUID**</span><span class="sxs-lookup"><span data-stu-id="3f679-187"><span id="GUID_IO_VOLUME_NAME_CHANGE"></span><span id="guid_io_volume_name_change"></span>**GUID\_IO\_VOLUME\_NAME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-188">2de97f83-4c06-11d2-a532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="3f679-188">2de97f83-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="3f679-189">Il nome del volume è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="3f679-189">The volume name has been changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**VOLUME i/o GUID \_ \_ \_ necessario \_ chkdsk**</span><span class="sxs-lookup"><span data-stu-id="3f679-190"><span id="GUID_IO_VOLUME_NEED_CHKDSK"></span><span id="guid_io_volume_need_chkdsk"></span>**GUID\_IO\_VOLUME\_NEED\_CHKDSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span><span class="sxs-lookup"><span data-stu-id="3f679-191">799a0960-0a0b-4e03-ad88-2fa7c6ce748a</span></span>
</dt> <dt>



<span data-ttu-id="3f679-192">Un file system ha rilevato un danneggiamento del volume.</span><span class="sxs-lookup"><span data-stu-id="3f679-192">A file system has detected corruption on the volume.</span></span> <span data-ttu-id="3f679-193">L'applicazione deve eseguire CHKDSK sul volume o inviare una notifica all'utente.</span><span class="sxs-lookup"><span data-stu-id="3f679-193">The application should run CHKDSK on the volume or notify the user to do so.</span></span>

<span data-ttu-id="3f679-194">**Windows Server 2003 e Windows XP:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3f679-194">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**\_modifica della \_ \_ configurazione fisica \_ del volume io GUID \_**</span><span class="sxs-lookup"><span data-stu-id="3f679-195"><span id="GUID_IO_VOLUME_PHYSICAL_CONFIGURATION_CHANGE"></span><span id="guid_io_volume_physical_configuration_change"></span>**GUID\_IO\_VOLUME\_PHYSICAL\_CONFIGURATION\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-196">2de97f84-4c06-11d2-a532-00609713055a</span><span class="sxs-lookup"><span data-stu-id="3f679-196">2de97f84-4c06-11d2-a532-00609713055a</span></span>
</dt> <dt>



<span data-ttu-id="3f679-197">Il trucco fisico o lo stato fisico corrente del volume è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="3f679-197">The physical makeup or current physical state of the volume has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**\_volume io del GUID \_ preparazione dell' \_ \_ espulsione**</span><span class="sxs-lookup"><span data-stu-id="3f679-198"><span id="GUID_IO_VOLUME_PREPARING_EJECT"></span><span id="guid_io_volume_preparing_eject"></span>**GUID\_IO\_VOLUME\_PREPARING\_EJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span><span class="sxs-lookup"><span data-stu-id="3f679-199">c79eb16e-0dac-4e7a-a86c-b25ceeaa88f6</span></span>
</dt> <dt>



<span data-ttu-id="3f679-200">Il file system sta preparando il disco da estrarre.</span><span class="sxs-lookup"><span data-stu-id="3f679-200">The file system is preparing the disc to be ejected.</span></span> <span data-ttu-id="3f679-201">Ad esempio, il file system sta arrestando un'operazione di formattazione in background o chiudendo la sessione in un supporto write-once.</span><span class="sxs-lookup"><span data-stu-id="3f679-201">For example, the file system is stopping a background formatting operation or closing the session on write-once media.</span></span>

<span data-ttu-id="3f679-202">**Windows Server 2003 e Windows XP:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3f679-202">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**\_ \_ \_ \_ modifica ID univoco del volume io del GUID \_**</span><span class="sxs-lookup"><span data-stu-id="3f679-203"><span id="GUID_IO_VOLUME_UNIQUE_ID_CHANGE"></span><span id="guid_io_volume_unique_id_change"></span>**GUID\_IO\_VOLUME\_UNIQUE\_ID\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-204">af39da42-6622-41f5-970b-139d092fa3d9</span><span class="sxs-lookup"><span data-stu-id="3f679-204">af39da42-6622-41f5-970b-139d092fa3d9</span></span>
</dt> <dt>



<span data-ttu-id="3f679-205">L'identificatore univoco del volume è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="3f679-205">The volume's unique identifier has been changed.</span></span> <span data-ttu-id="3f679-206">Per altre informazioni sull'identificatore univoco, vedere [**IOCTL \_ MOUNTDEV \_ query \_ Unique \_ ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).</span><span class="sxs-lookup"><span data-stu-id="3f679-206">For more information about the unique identifier, see [**IOCTL\_MOUNTDEV\_QUERY\_UNIQUE\_ID**](/windows-hardware/drivers/ddi/content/mountdev/ni-mountdev-ioctl_mountdev_query_unique_id).</span></span>

<span data-ttu-id="3f679-207">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo valore non è supportato fino a Windows Server 2008 R2 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3f679-207">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported until Windows Server 2008 R2 and Windows 7.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**\_ \_ sblocco volume i/o GUID \_**</span><span class="sxs-lookup"><span data-stu-id="3f679-208"><span id="GUID_IO_VOLUME_UNLOCK"></span><span id="guid_io_volume_unlock"></span>**GUID\_IO\_VOLUME\_UNLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-209">9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32</span><span class="sxs-lookup"><span data-stu-id="3f679-209">9a8c3d68-d0cb-11d1-8fef-00a0c9a06d32</span></span>
</dt> <dt>



<span data-ttu-id="3f679-210">Il volume è stato sbloccato da un altro processo.</span><span class="sxs-lookup"><span data-stu-id="3f679-210">The volume has been unlocked by another process.</span></span> <span data-ttu-id="3f679-211">È possibile aprire uno o più handle.</span><span class="sxs-lookup"><span data-stu-id="3f679-211">You may open one or more handles to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f679-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**VOLUME i/o GUID \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3f679-212"><span id="GUID_IO_VOLUME_WEARING_OUT"></span><span id="guid_io_volume_wearing_out"></span>**GUID\_IO\_VOLUME\_WEARING\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f679-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span><span class="sxs-lookup"><span data-stu-id="3f679-213">873113ca-1486-4508-82ac-c3b2e5297aaa</span></span>
</dt> <dt>



<span data-ttu-id="3f679-214">Il supporto si sta esaurendo. Questo evento viene inviato quando un file system determina che la frequenza degli errori in un volume è troppo elevata o lo spazio di sostituzione del difetto è quasi esaurito.</span><span class="sxs-lookup"><span data-stu-id="3f679-214">The media is wearing out. This event is sent when a file system determines that the error rate on a volume is too high, or its defect replacement space is almost exhausted.</span></span>

<span data-ttu-id="3f679-215">**Windows Server 2003 e Windows XP:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3f679-215">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f679-216">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f679-216">Remarks</span></span>

<span data-ttu-id="3f679-217">Gli eventi di smontaggio del **\_ \_ volume \_** di i/o di GUID e smontaggio del volume di i/o GUID sono correlati, così come il **\_ \_ \_ blocco** del volume di i/o GUID e l'evento di **\_ \_ \_ blocco \_ del volume** i **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3f679-217">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** events are related, as are the **GUID\_IO\_VOLUME\_LOCK** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** event.</span></span> <span data-ttu-id="3f679-218">Gli eventi di **\_ \_ \_ blocco** del volume i/o del GUID e del volume di i/o GUID indicano che è in corso il tentativo di un'operazione. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3f679-218">The **GUID\_IO\_VOLUME\_DISMOUNT** and **GUID\_IO\_VOLUME\_LOCK** events indicate that an operation is being attempted.</span></span> <span data-ttu-id="3f679-219">È necessario agire sulla notifica degli eventi e registrare l'azione eseguita.</span><span class="sxs-lookup"><span data-stu-id="3f679-219">You should act on the event notification, and record the action taken.</span></span> <span data-ttu-id="3f679-220">Lo SMONTAggio del volume di i/o del **GUID \_ \_ \_ \_ non riuscito** e gli eventi di blocco del volume di i/o **GUID \_ \_ \_ \_** non sono riusciti.</span><span class="sxs-lookup"><span data-stu-id="3f679-220">The **GUID\_IO\_VOLUME\_DISMOUNT\_FAILED** and **GUID\_IO\_VOLUME\_LOCK\_FAILED** events indicate that the attempted operation failed.</span></span> <span data-ttu-id="3f679-221">È quindi possibile usare il record per annullare le azioni eseguite in risposta all'operazione.</span><span class="sxs-lookup"><span data-stu-id="3f679-221">You may then use your record to undo the actions you made in response to the operation.</span></span>

<span data-ttu-id="3f679-222">Il membro **dbch \_ hdevnotify** della struttura dell' [**\_ \_ handle di broadcast dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) indica il dispositivo interessato.</span><span class="sxs-lookup"><span data-stu-id="3f679-222">The **dbch\_hdevnotify** member of the [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_handle) structure indicates the affected device.</span></span> <span data-ttu-id="3f679-223">Si noti che questo è l'handle di notifica del dispositivo restituito da [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), non un handle del volume.</span><span class="sxs-lookup"><span data-stu-id="3f679-223">Note that this is the device notification handle returned by [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa), not a volume handle.</span></span> <span data-ttu-id="3f679-224">Per eseguire operazioni sul volume, eseguire il mapping di questo handle all'handle del volume corrispondente.</span><span class="sxs-lookup"><span data-stu-id="3f679-224">To perform operations on the volume, map this handle to the corresponding volume handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f679-225">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f679-225">Requirements</span></span>



| <span data-ttu-id="3f679-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f679-226">Requirement</span></span> | <span data-ttu-id="3f679-227">Valore</span><span class="sxs-lookup"><span data-stu-id="3f679-227">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3f679-228">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f679-228">Minimum supported client</span></span><br/> | <span data-ttu-id="3f679-229">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3f679-229">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="3f679-230">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f679-230">Minimum supported server</span></span><br/> | <span data-ttu-id="3f679-231">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3f679-231">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="3f679-232">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f679-232">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f679-233"><dt>IoEvent. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f679-233"><dt>IoEvent.h</dt></span></span> </dl> |



 


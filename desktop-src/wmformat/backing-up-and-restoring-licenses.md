---
title: Backup e ripristino di licenze
description: Backup e ripristino di licenze
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- Windows Media Format SDK, backup delle licenze
- Windows Media Format SDK, ripristino di licenze
- Windows Media Format SDK, backup e ripristino delle licenze
- ASF (Advanced Systems Format), backup di licenze
- ASF (Advanced Systems Format), backup delle licenze
- ASF (Advanced Systems Format), ripristino di licenze
- ASF (Advanced Systems Format), ripristino di licenze
- ASF (Advanced Systems Format), backup e ripristino delle licenze
- ASF (Advanced Systems Format), backup e ripristino delle licenze
- Digital Rights Management (DRM), backup delle licenze
- DRM (Digital Rights Management), backup delle licenze
- Digital Rights Management (DRM), ripristino di licenze
- DRM (Digital Rights Management), ripristino di licenze
- Digital Rights Management (DRM), backup e ripristino delle licenze
- DRM (Digital Rights Management), backup e ripristino delle licenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10d8e76c191225288a1021e08e4c77e7e14f3c6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723527"
---
# <a name="backing-up-and-restoring-licenses"></a><span data-ttu-id="7854c-118">Backup e ripristino di licenze</span><span class="sxs-lookup"><span data-stu-id="7854c-118">Backing Up and Restoring Licenses</span></span>

<span data-ttu-id="7854c-119">I processi di backup e ripristino sono asincroni.</span><span class="sxs-lookup"><span data-stu-id="7854c-119">The backup and restore processes are asynchronous.</span></span> <span data-ttu-id="7854c-120">Vengono attivati quando l'utente seleziona un comando di menu o un'opzione nell'applicazione per eseguire il backup o il ripristino delle licenze.</span><span class="sxs-lookup"><span data-stu-id="7854c-120">They are triggered when the user selects a menu command or option in the application to back up or restore licenses.</span></span> <span data-ttu-id="7854c-121">È necessario consentire all'utente di specificare i percorsi in cui deve essere eseguito il backup e il ripristino delle licenze.</span><span class="sxs-lookup"><span data-stu-id="7854c-121">You should allow the user to specify the locations where licenses must be backed up to and restored from.</span></span>

<span data-ttu-id="7854c-122">Per eseguire il backup delle licenze:</span><span class="sxs-lookup"><span data-stu-id="7854c-122">To back up licenses:</span></span>

1.  <span data-ttu-id="7854c-123">Utilizzare la funzione [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) per creare l'oggetto di ripristino di backup.</span><span class="sxs-lookup"><span data-stu-id="7854c-123">Use the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="7854c-124">Chiamare il metodo [**IWMBackupRestoreProps:: seprop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) per impostare il percorso di backup, ovvero il percorso in cui si scriveranno i file, ad esempio: \\ o D: \\ licenses.</span><span class="sxs-lookup"><span data-stu-id="7854c-124">Call the [**IWMBackupRestoreProps::SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) method to set the backup path (the location where you will write the files, such as A:\\ or D:\\Licenses).</span></span>
3.  <span data-ttu-id="7854c-125">Chiamare il metodo [**IWMLicenseBackup:: BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) per eseguire il backup delle licenze nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="7854c-125">Call the [**IWMLicenseBackup::BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) method to back up the licenses to the specified path.</span></span>

<span data-ttu-id="7854c-126">Al metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) vengono inviati gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7854c-126">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="7854c-127">**WMT \_ BACKUPRESTORE \_ Begin** indica che il processo di backup è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="7854c-127">**WMT\_BACKUPRESTORE\_BEGIN** indicates the backup process has started.</span></span>
-   <span data-ttu-id="7854c-128">**WMT \_ BACKUPRESTORE \_ end** indica che il processo di backup è stato completato.</span><span class="sxs-lookup"><span data-stu-id="7854c-128">**WMT\_BACKUPRESTORE\_END** indicates the backup process has been completed.</span></span>
-   <span data-ttu-id="7854c-129">**WMT \_ \_Licenza limitata** indica che non è possibile eseguire il backup di una o più licenze perché il diritto non è consentito dal proprietario del contenuto.</span><span class="sxs-lookup"><span data-stu-id="7854c-129">**WMT\_RESTRICTED\_LICENSE** indicates that one or more licenses cannot be backed up because the right has been disallowed by the content owner.</span></span>

<span data-ttu-id="7854c-130">L'ID chiave è incluso anche in questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="7854c-130">The key ID is also included in this message.</span></span> <span data-ttu-id="7854c-131">Se è stato implementato un database per i file protetti che includono l'ID e i metadati della chiave, è possibile visualizzare un messaggio all'utente con il titolo specifico, ad esempio il titolo di un brano, per il quale non è possibile eseguire il backup della licenza.</span><span class="sxs-lookup"><span data-stu-id="7854c-131">If you have implemented a database for protected files that includes the key ID and metadata, you can display a message to the user with the specific title (such as a song title) for which the license cannot be backed up.</span></span> <span data-ttu-id="7854c-132">In caso contrario, il messaggio deve essere generico e informare l'utente che non è possibile eseguire il backup di alcune licenze.</span><span class="sxs-lookup"><span data-stu-id="7854c-132">Otherwise, the message must be generic and inform the user that some licenses cannot be backed up.</span></span>

<span data-ttu-id="7854c-133">Per ripristinare le licenze:</span><span class="sxs-lookup"><span data-stu-id="7854c-133">To restore licenses:</span></span>

1.  <span data-ttu-id="7854c-134">Utilizzare la funzione **WMCreateBackupRestorer** per creare l'oggetto di ripristino di backup.</span><span class="sxs-lookup"><span data-stu-id="7854c-134">Use the **WMCreateBackupRestorer** function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="7854c-135">Chiamare il metodo **IWMBackupRestoreProps:: seprop** per impostare il percorso di ripristino sul percorso in cui viene eseguito il backup delle licenze.</span><span class="sxs-lookup"><span data-stu-id="7854c-135">Call the **IWMBackupRestoreProps::SetProp** method to set the restore path to the location where licenses are backed up.</span></span>
3.  <span data-ttu-id="7854c-136">Chiamare il metodo [**IWMLicenseRestore:: RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) per ripristinare le licenze da tale percorso.</span><span class="sxs-lookup"><span data-stu-id="7854c-136">Call the [**IWMLicenseRestore::RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) method to restore licenses from that location.</span></span>

<span data-ttu-id="7854c-137">Al metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) vengono inviati gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7854c-137">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="7854c-138">**WMT \_ La \_ connessione BACKUPRESTORE** indica che l'applicazione sta effettuando la connessione al servizio di gestione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="7854c-138">**WMT\_BACKUPRESTORE\_CONNECTING** indicates that the application is connecting to the License Management Service.</span></span>
-   <span data-ttu-id="7854c-139">**WMT \_ La \_ disconnessione di BACKUPRESTORE** indica che l'applicazione è in stato di disconnessione dal servizio di gestione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="7854c-139">**WMT\_BACKUPRESTORE\_DISCONNECTING** indicates that the application is disconnecting from the License Management Service.</span></span>
-   <span data-ttu-id="7854c-140">**WMT \_ BACKUPRESTORE \_ Begin** indica che il processo di ripristino è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="7854c-140">**WMT\_BACKUPRESTORE\_BEGIN** indicates the restore process has started.</span></span>
-   <span data-ttu-id="7854c-141">**WMT \_ BACKUPRESTORE \_ end** indica che il processo di ripristino è stato completato.</span><span class="sxs-lookup"><span data-stu-id="7854c-141">**WMT\_BACKUPRESTORE\_END** indicates the restore process has been completed.</span></span>

> [!Note]  
> <span data-ttu-id="7854c-142">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="7854c-142">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7854c-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7854c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7854c-144">**Funzionalità di Rights Management digitali**</span><span class="sxs-lookup"><span data-stu-id="7854c-144">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="7854c-145">**Interfaccia IWMBackupRestoreProps**</span><span class="sxs-lookup"><span data-stu-id="7854c-145">**IWMBackupRestoreProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[<span data-ttu-id="7854c-146">**Interfaccia IWMLicenseBackup**</span><span class="sxs-lookup"><span data-stu-id="7854c-146">**IWMLicenseBackup Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[<span data-ttu-id="7854c-147">**Interfaccia IWMLicenseRestore**</span><span class="sxs-lookup"><span data-stu-id="7854c-147">**IWMLicenseRestore Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 





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
# <a name="backing-up-and-restoring-licenses"></a>Backup e ripristino di licenze

I processi di backup e ripristino sono asincroni. Vengono attivati quando l'utente seleziona un comando di menu o un'opzione nell'applicazione per eseguire il backup o il ripristino delle licenze. È necessario consentire all'utente di specificare i percorsi in cui deve essere eseguito il backup e il ripristino delle licenze.

Per eseguire il backup delle licenze:

1.  Utilizzare la funzione [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) per creare l'oggetto di ripristino di backup.
2.  Chiamare il metodo [**IWMBackupRestoreProps:: seprop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) per impostare il percorso di backup, ovvero il percorso in cui si scriveranno i file, ad esempio: \\ o D: \\ licenses.
3.  Chiamare il metodo [**IWMLicenseBackup:: BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) per eseguire il backup delle licenze nel percorso specificato.

Al metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) vengono inviati gli eventi seguenti:

-   **WMT \_ BACKUPRESTORE \_ Begin** indica che il processo di backup è stato avviato.
-   **WMT \_ BACKUPRESTORE \_ end** indica che il processo di backup è stato completato.
-   **WMT \_ \_Licenza limitata** indica che non è possibile eseguire il backup di una o più licenze perché il diritto non è consentito dal proprietario del contenuto.

L'ID chiave è incluso anche in questo messaggio. Se è stato implementato un database per i file protetti che includono l'ID e i metadati della chiave, è possibile visualizzare un messaggio all'utente con il titolo specifico, ad esempio il titolo di un brano, per il quale non è possibile eseguire il backup della licenza. In caso contrario, il messaggio deve essere generico e informare l'utente che non è possibile eseguire il backup di alcune licenze.

Per ripristinare le licenze:

1.  Utilizzare la funzione **WMCreateBackupRestorer** per creare l'oggetto di ripristino di backup.
2.  Chiamare il metodo **IWMBackupRestoreProps:: seprop** per impostare il percorso di ripristino sul percorso in cui viene eseguito il backup delle licenze.
3.  Chiamare il metodo [**IWMLicenseRestore:: RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) per ripristinare le licenze da tale percorso.

Al metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) vengono inviati gli eventi seguenti:

-   **WMT \_ La \_ connessione BACKUPRESTORE** indica che l'applicazione sta effettuando la connessione al servizio di gestione delle licenze.
-   **WMT \_ La \_ disconnessione di BACKUPRESTORE** indica che l'applicazione è in stato di disconnessione dal servizio di gestione delle licenze.
-   **WMT \_ BACKUPRESTORE \_ Begin** indica che il processo di ripristino è stato avviato.
-   **WMT \_ BACKUPRESTORE \_ end** indica che il processo di ripristino è stato completato.

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Interfaccia IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[**Interfaccia IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[**Interfaccia IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 





---
title: Backup e ripristino delle licenze
description: Backup e ripristino delle licenze
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- Windows Media Format SDK, backup delle licenze
- Windows Media Format SDK, ripristino delle licenze
- Windows Media Format SDK, backup e ripristino delle licenze
- Advanced Systems Format (ASF), backup delle licenze
- ASF (Advanced Systems Format), backup delle licenze
- Advanced Systems Format (ASF), ripristino delle licenze
- ASF (Advanced Systems Format), ripristino delle licenze
- Advanced Systems Format (ASF), backup e ripristino delle licenze
- ASF (Advanced Systems Format), backup e ripristino delle licenze
- digital rights management (DRM), backup delle licenze
- DRM (digital rights management), backup delle licenze
- digital rights management (DRM), ripristino delle licenze
- DRM (digital rights management), ripristino delle licenze
- digital rights management (DRM), backup e ripristino delle licenze
- DRM (digital rights management), backup e ripristino delle licenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378a41d975e8f19d38c637d585759d0038f5b86550769ae49d6a6490844f223e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028139"
---
# <a name="backing-up-and-restoring-licenses"></a>Backup e ripristino delle licenze

I processi di backup e ripristino sono asincroni. Vengono attivati quando l'utente seleziona un comando di menu o un'opzione nell'applicazione per eseguire il backup o il ripristino delle licenze. È necessario consentire all'utente di specificare i percorsi in cui è necessario eseguire il backup e il ripristino delle licenze.

Per eseguire il backup delle licenze:

1.  Usare la [**funzione WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) per creare l'oggetto di ripristino del backup.
2.  Chiamare il metodo [**IWMBackupRestoreProps::SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) per impostare il percorso di backup ,ovvero il percorso in cui si scriveranno i file, ad esempio A: \\ o D: \\ Licenses.
3.  Chiamare il [**metodo IWMLicenseBackup::BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) per eseguire il backup delle licenze nel percorso specificato.

Gli eventi seguenti vengono inviati al [**metodo IWMStatusCallback::OnStatus:**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)

-   **WMT \_ BACKUPRESTORE \_ BEGIN** indica che il processo di backup è stato avviato.
-   **WMT \_ BACKUPRESTORE \_ END** indica che il processo di backup è stato completato.
-   **WMT \_ RESTRICTED \_ LICENSE** indica che non è possibile eseguire il backup di una o più licenze perché il diritto non è consentito dal proprietario del contenuto.

Anche l'ID chiave è incluso in questo messaggio. Se è stato implementato un database per i file protetti che include l'ID chiave e i metadati, è possibile visualizzare un messaggio all'utente con il titolo specifico (ad esempio un titolo di brano) per cui non è possibile eseguire il backup della licenza. In caso contrario, il messaggio deve essere generico e informare l'utente che non è possibile eseguire il backup di alcune licenze.

Per ripristinare le licenze:

1.  Usare la **funzione WMCreateBackupRestorer** per creare l'oggetto di ripristino del backup.
2.  Chiamare il **metodo IWMBackupRestoreProps::SetProp** per impostare il percorso di ripristino nel percorso in cui viene eseguito il backup delle licenze.
3.  Chiamare il [**metodo IWMLicenseRestore::RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) per ripristinare le licenze da tale posizione.

Gli eventi seguenti vengono inviati al [**metodo IWMStatusCallback::OnStatus:**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)

-   **WMT \_ BACKUPRESTORE \_ CONNECTING** indica che l'applicazione si connette al servizio di gestione delle licenze.
-   **WMT \_ BACKUPRESTORE \_ DISCONNECTING** indica che l'applicazione si sta disconnettendo dal servizio di gestione licenze.
-   **WMT \_ BACKUPRESTORE \_ BEGIN** indica che il processo di ripristino è stato avviato.
-   **WMT \_ BACKUPRESTORE \_ END** indica che il processo di ripristino è stato completato.

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Interfaccia IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[**Interfaccia IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[**Interfaccia IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 





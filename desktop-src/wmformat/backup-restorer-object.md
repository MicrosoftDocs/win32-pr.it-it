---
title: Oggetto ripristinatore backup
description: Oggetto ripristinatore backup
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- Windows Media Format SDK, oggetti del ripristino di backup
- ASF (Advanced Systems Format), oggetti del ripristino di backup
- ASF (formato avanzato dei sistemi), oggetti del ripristino di backup
- oggetti, backup di oggetti del ripristino
- ripristino di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08e8bec9bb7bbc2a45fbf632e69d230a2536633
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299427"
---
# <a name="backup-restorer-object"></a>Oggetto ripristinatore backup

Il ripristino di backup fornisce le interfacce per gestire le licenze di backup, in genere su supporti rimovibili, quindi il ripristino di tali licenze su un nuovo computer.

L'oggetto di ripristino di backup viene creato dalla funzione [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) , che imposta un puntatore a un'interfaccia [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) . Le altre interfacce dell'oggetto di ripristino di backup possono essere ottenute chiamando il metodo **QueryInterface** .

Le interfacce seguenti sono supportate dall'oggetto di ripristino di backup.



| Interfaccia                                              | Descrizione                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | Imposta e recupera le proprietà richieste dalle interfacce [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) e [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) . |
| [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | Esegue il backup delle licenze, in genere in modo che possano essere ripristinate su un altro computer.                                                                          |
| [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | Ripristina le licenze.                                                                                                                                        |



 

L'interfaccia di callback seguente deve essere implementata dall'applicazione per poter utilizzare l'oggetto di ripristino di backup.



| Interfaccia                                      | Descrizione                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Riceve i messaggi di stato dai processi eseguiti in un thread separato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Backup e ripristino di licenze**](backing-up-and-restoring-licenses.md)
</dt> <dt>

[**Oggetti**](objects.md)
</dt> </dl>

 

 





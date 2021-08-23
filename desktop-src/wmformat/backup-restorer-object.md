---
title: Oggetto Backup Restorer
description: Oggetto Backup Restorer
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- Windows Media Format SDK,backup restorer objects
- Advanced Systems Format (ASF),backup restorer objects
- ASF (Advanced Systems Format),backup restorer objects
- oggetti, oggetti di ripristino di backup
- backup restorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a7bf14f8afda284d8d0ae3d4f36d37fff0baa63f4f42802a98830038ec2d850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028129"
---
# <a name="backup-restorer-object"></a>Oggetto Backup Restorer

Il ripristino del backup fornisce interfacce per gestire il backup delle licenze, in genere su supporti rimovibili, e quindi il ripristino di tali licenze in un nuovo computer.

L'oggetto di ripristino del backup viene creato dalla funzione [**WMCreateBackupRestorer,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) che imposta un puntatore a [**un'interfaccia IWMLicenseBackup.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) Le altre interfacce dell'oggetto di ripristino del backup possono essere ottenute chiamando il **metodo QueryInterface.**

Le interfacce seguenti sono supportate dall'oggetto di ripristino del backup.



| Interfaccia                                              | Descrizione                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | Imposta e recupera le proprietà richieste dalle [**interfacce IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) [**e IWMLicenseRestore.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) |
| [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | Esegue il backup delle licenze, in genere in modo che possano essere ripristinate in un altro computer.                                                                          |
| [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | Ripristina le licenze.                                                                                                                                        |



 

L'interfaccia di callback seguente deve essere implementata dall'applicazione per poter usare l'oggetto di ripristino del backup.



| Interfaccia                                      | Descrizione                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Riceve i messaggi di stato dai processi eseguiti in un thread separato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Backup e ripristino delle licenze**](backing-up-and-restoring-licenses.md)
</dt> <dt>

[**Oggetti**](objects.md)
</dt> </dl>

 

 





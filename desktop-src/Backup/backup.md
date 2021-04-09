---
title: Backup
description: Consentire alle applicazioni di backup di comunicare con altre applicazioni e servizi sulle operazioni di backup e ripristino. Eseguire il backup su nastro, inizializzare il nastro e recuperare le informazioni sull'unità nastro. Gestire i file duplicati con l'archivio a istanza singola (SIS).
ms.assetid: 97c3e2c4-8214-4093-bd13-3c38c91e08bd
keywords:
- backup di backup
- backup backup, Home
- Backup operazioni di ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689a5a4613bdf029b270947b523727ea00a6e05d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118106"
---
# <a name="backup"></a>Backup

Le chiavi del registro di sistema per il backup e il ripristino consentono alle applicazioni di backup di comunicare con altre applicazioni e servizi per le operazioni di backup e ripristino. Per ulteriori informazioni, vedere [chiavi e valori del registro di sistema per il backup e il ripristino](registry-keys-for-backup-and-restore.md).

L'API backup su nastro consente alle applicazioni di backup di leggere e scrivere su un nastro, inizializzare un nastro e recuperare informazioni su nastro o unità nastro. Per ulteriori informazioni, vedere [backup su nastro](tape-backup.md).

L'archivio a istanza singola (SIS) è un'architettura progettata per gestire i file duplicati con un sovraccarico minimo. L'applicazione di backup usa l'API di backup SIS per accedere all'architettura SIS. Per altre informazioni, vedere [archivio a istanza singola e backup SIS](single-instance-store-and-sis-backup.md).

Il backup e il ripristino di file crittografati sono abilitati dall'API di crittografia non elaborata, che legge e scrive i file crittografati mantenendo i dati in formato crittografato. L'API consente di eseguire il backup e il ripristino dei dati crittografati in questi file, rispettando allo stesso tempo gli obiettivi del mantenimento della sicurezza dei dati di cui è stato eseguito il backup e l'utilizzo da parte di un'applicazione che non dispone dell'autorizzazione per l'utilizzo delle chiavi di crittografia nel file. Per ulteriori informazioni, vedere [backup e ripristino di file crittografati](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).

Lo strumento Srdelayed può consentire alle applicazioni di ripristino dello stato del sistema di spostare, eliminare e impostare il nome breve dei file di sistema. Per ulteriori informazioni, vedere [Srdelayed.exe](srdelayed-exe.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al backup](backup-reference.md)
</dt> </dl>

 

 
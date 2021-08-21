---
title: Backup
description: Consentire alle applicazioni di backup di comunicare con altre applicazioni e servizi sulle operazioni di backup e ripristino. Eseguire il backup su nastro, inizializzare il nastro e recuperare le informazioni sull'unità nastro. Mantenere i file duplicati con l'archivio a istanza singola (SIS).
ms.assetid: 97c3e2c4-8214-4093-bd13-3c38c91e08bd
keywords:
- backup backup
- backup Backup , home
- operazioni di ripristino Backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efe2668df47c271aba5befc3ba380c313b7bc15c11162a29b8364be6eb3fead
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588891"
---
# <a name="backup"></a>Backup

Le chiavi del Registro di sistema per il backup e il ripristino consentono alle applicazioni di backup di comunicare con altre applicazioni e servizi sulle operazioni di backup e ripristino. Per altre informazioni, vedere Chiavi e [valori del Registro di sistema per il backup e il ripristino.](registry-keys-for-backup-and-restore.md)

L'API di backup su nastro consente alle applicazioni di backup di leggere e scrivere su un nastro, inizializzare un nastro e recuperare informazioni sul nastro o sull'unità nastro. Per altre informazioni, vedere [Backup su nastro.](tape-backup.md)

L'archivio a istanza singola (SIS) è un'architettura progettata per mantenere i file duplicati con un sovraccarico minimo. L'applicazione di backup usa l'API di backup SIS per accedere all'architettura SIS. Per altre informazioni, vedere [Single-Instance Store and SIS Backup](single-instance-store-and-sis-backup.md).

Il backup e il ripristino dei file crittografati sono abilitati dall'API di crittografia non elaborata, che legge e scrive i file crittografati mantenendo i dati in formato crittografato. L'API consente di eseguire il backup e il ripristino dei dati crittografati in questi file, rispettando al tempo stesso gli obiettivi di mantenimento della sicurezza dei dati di cui è stato eseguito il backup e di essere utilizzabile da un'applicazione che non dispone dell'autorizzazione per usare le chiavi di crittografia nel file. Per altre informazioni, vedere [Backup e ripristino di file crittografati.](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files)

Lo strumento Srdelayed consente alle applicazioni di ripristino dello stato del sistema di spostare, eliminare e impostare il nome breve dei file di sistema. Per altre informazioni, vedere [Srdelayed.exe](srdelayed-exe.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul backup](backup-reference.md)
</dt> </dl>

 

 
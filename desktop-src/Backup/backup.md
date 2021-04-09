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
# <a name="backup"></a><span data-ttu-id="737a2-108">Backup</span><span class="sxs-lookup"><span data-stu-id="737a2-108">Backup</span></span>

<span data-ttu-id="737a2-109">Le chiavi del registro di sistema per il backup e il ripristino consentono alle applicazioni di backup di comunicare con altre applicazioni e servizi per le operazioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="737a2-109">Registry keys for backup and restore allow backup applications to communicate with other applications and services about backup and restore operations.</span></span> <span data-ttu-id="737a2-110">Per ulteriori informazioni, vedere [chiavi e valori del registro di sistema per il backup e il ripristino](registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="737a2-110">For more information, see [Registry Keys and Values for Backup and Restore](registry-keys-for-backup-and-restore.md).</span></span>

<span data-ttu-id="737a2-111">L'API backup su nastro consente alle applicazioni di backup di leggere e scrivere su un nastro, inizializzare un nastro e recuperare informazioni su nastro o unità nastro.</span><span class="sxs-lookup"><span data-stu-id="737a2-111">The tape backup API enables backup applications to read from and write to a tape, initialize a tape, and retrieve tape or tape drive information.</span></span> <span data-ttu-id="737a2-112">Per ulteriori informazioni, vedere [backup su nastro](tape-backup.md).</span><span class="sxs-lookup"><span data-stu-id="737a2-112">For more information, see [Tape Backup](tape-backup.md).</span></span>

<span data-ttu-id="737a2-113">L'archivio a istanza singola (SIS) è un'architettura progettata per gestire i file duplicati con un sovraccarico minimo.</span><span class="sxs-lookup"><span data-stu-id="737a2-113">Single-instance store (SIS) is an architecture designed to maintain duplicate files with a minimum of overhead.</span></span> <span data-ttu-id="737a2-114">L'applicazione di backup usa l'API di backup SIS per accedere all'architettura SIS.</span><span class="sxs-lookup"><span data-stu-id="737a2-114">Backup application use the SIS backup API to access the SIS architecture.</span></span> <span data-ttu-id="737a2-115">Per altre informazioni, vedere [archivio a istanza singola e backup SIS](single-instance-store-and-sis-backup.md).</span><span class="sxs-lookup"><span data-stu-id="737a2-115">For more information, see [Single-Instance Store and SIS Backup](single-instance-store-and-sis-backup.md).</span></span>

<span data-ttu-id="737a2-116">Il backup e il ripristino di file crittografati sono abilitati dall'API di crittografia non elaborata, che legge e scrive i file crittografati mantenendo i dati in formato crittografato.</span><span class="sxs-lookup"><span data-stu-id="737a2-116">Backup and restore of encrypted files is enabled by the raw encryption API, which reads and writes encrypted files while keeping the data in encrypted format.</span></span> <span data-ttu-id="737a2-117">L'API consente di eseguire il backup e il ripristino dei dati crittografati in questi file, rispettando allo stesso tempo gli obiettivi del mantenimento della sicurezza dei dati di cui è stato eseguito il backup e l'utilizzo da parte di un'applicazione che non dispone dell'autorizzazione per l'utilizzo delle chiavi di crittografia nel file.</span><span class="sxs-lookup"><span data-stu-id="737a2-117">The API allows the encrypted data in these files to be backed up and restored, while meeting the goals of maintaining the security of the backed up data, and being usable by an application that lacks permission to use the encryption keys on the file.</span></span> <span data-ttu-id="737a2-118">Per ulteriori informazioni, vedere [backup e ripristino di file crittografati](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).</span><span class="sxs-lookup"><span data-stu-id="737a2-118">For more information, see [Backup and Restore of Encrypted Files](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).</span></span>

<span data-ttu-id="737a2-119">Lo strumento Srdelayed può consentire alle applicazioni di ripristino dello stato del sistema di spostare, eliminare e impostare il nome breve dei file di sistema.</span><span class="sxs-lookup"><span data-stu-id="737a2-119">The Srdelayed tool can enable system state recovery applications to move, delete, and set the short name of system files.</span></span> <span data-ttu-id="737a2-120">Per ulteriori informazioni, vedere [Srdelayed.exe](srdelayed-exe.md).</span><span class="sxs-lookup"><span data-stu-id="737a2-120">For more information, see [Srdelayed.exe](srdelayed-exe.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="737a2-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="737a2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="737a2-122">Riferimento al backup</span><span class="sxs-lookup"><span data-stu-id="737a2-122">Backup Reference</span></span>](backup-reference.md)
</dt> </dl>

 

 
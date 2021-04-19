---
description: Tutte le informazioni su un file, incluse le dimensioni, gli indicatori di data e ora, le autorizzazioni e il contenuto dei dati, vengono archiviati nelle voci della tabella file master (MFT) o nello spazio esterno alla MFT descritta dalle voci MFT.
ms.assetid: e0933846-278e-4bc8-8982-c5819c252dad
title: Tabella file master (file system locali)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260740c03e7b7e4ebe9c7e8ec90035431f6be649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317769"
---
# <a name="master-file-table-local-file-systems"></a>Tabella file master (file system locali)

Il file system NTFS contiene un file denominato *tabella file master* o MFT. In MFT è presente almeno una voce per ogni file in un volume file system NTFS, incluso il MFT stesso. Tutte le informazioni su un file, incluse le dimensioni, gli indicatori di data e ora, le autorizzazioni e il contenuto dei dati, vengono archiviati in voci MFT o nello spazio esterno alla MFT descritta dalle voci MFT.

Man mano che i file vengono aggiunti a un volume di file system NTFS, più voci vengono aggiunte alla MFT e le dimensioni della MFT aumentano. Quando i file vengono eliminati da un volume file system NTFS, le relative voci MFT sono contrassegnate come gratuite e possono essere riutilizzate. Tuttavia, lo spazio su disco allocato per queste voci non viene riallocato e la dimensione del MFT non diminuisce.

Il file system NTFS riserva spazio per la MFT, in modo che il MFT rimanga più contiguo possibile mentre cresce. Lo spazio riservato dal file system NTFS per il MFT in ogni volume è denominato zona MFT. Lo spazio per file e directory viene inoltre allocato da questo spazio, ma solo dopo che è stato allocato tutto lo spazio del volume al di fuori della zona MFT.

A seconda della dimensione media del file e di altre variabili, è possibile allocare la zona MFT riservata o lo spazio non riservato sul disco prima di riempire la capacità del disco. I volumi con un numero ridotto di file di dimensioni relativamente grandi allocano prima lo spazio riservato, mentre i volumi con un numero elevato di file di dimensioni relativamente ridotte allocano prima la zona MFT. In entrambi i casi, la frammentazione di MFT inizia a essere eseguita quando un'area o l'altra viene allocata completamente. Se lo spazio non riservato è completamente allocato, lo spazio per i file e le directory utente verrà allocato dalla zona MFT. Se la zona MFT è completamente allocata, lo spazio per le nuove voci MFT verrà allocato dallo spazio non riservato.

Il MFT può essere deframmentato. Per ridurre la possibilità che la zona MFT venga allocata completamente prima del completamento del processo di deframmentazione, lasciare il numero massimo di spazio all'inizio della zona MFT prima di deframmentare il volume. Se la zona MFT viene allocata completamente prima del completamento della deframmentazione, è necessario che lo spazio non sia allocato all'esterno della zona MFT.

L'area MFT predefinita viene calcolata e riservata dal sistema durante il montaggio del volume e si basa sulle dimensioni del volume. È possibile aumentare la zona MFT per mezzo della voce del registro di sistema descritta in dettaglio nell' [articolo 174619 della Microsoft Knowledge base](https://support.microsoft.com/kb/174619), ma non è possibile rendere la zona MFT predefinita inferiore a quella calcolata. L'aumento della zona MFT non riduce lo spazio su disco che gli utenti possono utilizzare per i file di dati.

Per determinare le dimensioni correnti della MFT, analizzare l'unità di file system NTFS con utilità di deframmentazione dischi, quindi fare clic sul pulsante **Visualizza report** . Verranno visualizzate le statistiche dell'unità, incluse le dimensioni MFT correnti e il numero di frammenti. È anche possibile ottenere le dimensioni di MFT usando il codice di [**controllo \_ \_ \_ \_ dei dati del volume NTFS FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data) .

 

 

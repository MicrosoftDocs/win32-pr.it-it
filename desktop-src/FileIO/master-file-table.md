---
description: Tutte le informazioni su un file, incluse le dimensioni, gli indicatori di data e ora, le autorizzazioni e il contenuto dei dati, vengono archiviate nelle voci della tabella del file master (MFT) o nello spazio all'esterno del MFT descritto dalle voci MFT.
ms.assetid: e0933846-278e-4bc8-8982-c5819c252dad
title: Tabella file master (file system locali)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fefec19906e6e2e2c67bbcabf8bd891ccc032b7e8d0882a3622011c324d11c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525641"
---
# <a name="master-file-table-local-file-systems"></a>Tabella file master (file system locali)

Il file system NTFS contiene un file denominato *tabella file master* o MFT. In MFT è presente almeno una voce per ogni file in un volume file system NTFS, incluso il MFT stesso. Tutte le informazioni su un file, incluse le dimensioni, i timestamp e i timestamp, le autorizzazioni e il contenuto dei dati, vengono archiviate nelle voci MFT o nello spazio esterno al MFT descritto dalle voci MFT.

Quando i file vengono aggiunti a un volume file system NTFS, vengono aggiunte altre voci al MFT e le dimensioni di MFT aumentano. Quando i file vengono eliminati da un volume file system NTFS, le relative voci MFT vengono contrassegnate come gratuite e possono essere riutilizzate. Tuttavia, lo spazio su disco allocato per queste voci non viene riallocato e le dimensioni del MFT non diminuiscono.

Il file system NTFS riserva spazio per MFT per mantenere il MFT il più contiguo possibile man mano che aumenta. Lo spazio riservato dal file system NTFS per MFT in ogni volume è denominato zona MFT. Anche lo spazio per file e directory viene allocato da questo spazio, ma solo dopo l'allocazione di tutto lo spazio del volume all'esterno della zona MFT.

A seconda delle dimensioni medie del file e di altre variabili, la zona MFT riservata o lo spazio non riservato sul disco può essere allocato per primo quando il disco riempie la capacità. I volumi con un numero ridotto di file relativamente grandi allocano prima lo spazio non riservato, mentre i volumi con un numero elevato di file relativamente piccoli allocano prima la zona MFT. In entrambi i casi, la frammentazione del MFT inizia a verificarsi quando un'area o l'altra diventa completamente allocata. Se lo spazio non riservato è completamente allocato, lo spazio per i file e le directory utente verrà allocato dalla zona MFT. Se la zona MFT è completamente allocata, lo spazio per le nuove voci MFT verrà allocato dallo spazio non riservato.

L'MFT stesso può essere deframmentato. Per ridurre la possibilità che la zona MFT diventi completamente allocata prima del completamento del processo di deframmentazione, lasciare la quantità di spazio all'inizio della zona MFT il più possibile prima di deframmentare il volume. Se la zona MFT viene allocata completamente prima del completamento della deframmentazione, è necessario che vi sia spazio non allocato all'esterno della zona MFT.

La zona MFT predefinita viene calcolata e riservata dal sistema quando monta il volume e si basa sulle dimensioni del volume. È possibile aumentare la zona MFT tramite la voce del Registro di sistema illustrata in dettaglio nell'articolo [Microsoft Knowledge Base 174619](https://support.microsoft.com/kb/174619), ma non è possibile rendere la zona MFT predefinita più piccola di quella calcolata. L'aumento della zona MFT non riduce lo spazio su disco che gli utenti possono usare per i file di dati.

Per determinare le dimensioni correnti di MFT, analizzare l'unità file system NTFS con Utilità di deframmentazione dischi, quindi fare clic **sul pulsante Visualizza** report. Verranno visualizzate le statistiche delle unità, incluse le dimensioni MFT correnti e il numero di frammenti. È anche possibile ottenere le dimensioni del MFT usando il codice di controllo [**\_ FSCTL GET NTFS VOLUME \_ \_ \_ DATA.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)

 

 

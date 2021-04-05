---
description: Le tabelle in cui sono elencate le funzionalità e le funzionalità supportano i confronti per i quattro file System Windows principali, NTFS, exFAT, UDF e FAT32.
ms.assetid: 28cf2805-f1ce-46b4-bf08-a329f67f4d99
title: Confronto delle funzionalità del file System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7547e48ff68a8fdab195087904a47a535aa3464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753567"
---
# <a name="file-system-functionality-comparison"></a>Confronto delle funzionalità del file System

Le tabelle seguenti elencano le funzionalità e i confronti di supporto per i quattro file System Windows principali, NTFS, exFAT, UDF e FAT32:

-   [Funzionalità](#file-system-functionality-comparison)
-   [Limiti](#limits)
-   [Journaling e log delle modifiche](#journaling-and-change-log)
-   [Blocca funzionalità di allocazione](#block-allocation-features)
-   [Sicurezza](#security)
-   [Compressione](#compression)
-   [Quote](#quotas)
-   [Archivio a istanza singola](#single-instance-store)
-   [Argomenti correlati](#related-topics)

## <a name="functionality"></a>Funzionalità



| Funzionalità                             | NTFS                           | exFAT          | UDF                           | FAT32                      |
|-------------------------------------|--------------------------------|----------------|-------------------------------|----------------------------|
| Timestamp di creazione<br/>     | Sì<br/>                 | Sì<br/> | Sì<br/>                | Sì<br/>             |
| Timestamp ultimo accesso<br/>  | No (vedere la nota sotto)<br/> | Sì<br/> | Sì<br/>                | Sì (solo data)<br/> |
| Timestamp dell'Ultima modifica<br/>  | Sì<br/>                 | Sì<br/> | Sì<br/>                | Sì<br/>             |
| Timestamp dell'ultimo archivio<br/> | No<br/>                  | No<br/>  | No<br/>                 | No<br/>              |
| Con distinzione tra maiuscole e minuscole<br/>           | Sì (opzione)<br/>        | No<br/>  | Sì<br/>                | No<br/>              |
| Conservazione del case<br/>          | Sì<br/>                 | Sì<br/> | Sì<br/>                | Sì<br/>             |
| Collegamenti reali<br/>               | Sì<br/>                 | No<br/>  | Sì<br/>                | No<br/>              |
| Soft link<br/>               | Sì<br/>                 | No<br/>  | No<br/>                 | No<br/>              |
| File sparse<br/>             | Sì<br/>                 | No<br/>  | Sì<br/>                | No<br/>              |
| Flussi denominati<br/>            | Sì<br/>                 | No<br/>  | Sì<br/>                | No<br/>              |
| Blocchi opportunistici (oplock)<br/>                  | Sì<br/>                 | Sì<br/> | Sì<br/>                | Sì<br/>             |
| Attributi estesi<br/>      | Sì<br/>                 | No<br/>  | Sì (solo su disco)<br/> | No<br/>              |
| Flussi dei dati alternativi<br/>   | Sì<br/>                 | No<br/>  | Sì<br/>                | No<br/>              |
| Punti di montaggio<br/>             | Sì<br/>                 | No<br/>  | No<br/>                 | No<br/>              |



 

**Windows Server 2003 e Windows XP:** Il campo data e ora ultimo accesso NTFS è stato aggiornato.

## <a name="limits"></a>Limiti



| Funzionalità                             | NTFS                                                                                      | exFAT                                                                                     | UDF                                                                                       | FAT32                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Lunghezza massima del nome del file<br/> | 255 caratteri Unicode<br/>                                                         | 255 caratteri Unicode<br/>                                                         | 127 caratteri ASCII Unicode o 254<br/>                                            | 255 caratteri Unicode<br/>                                                         |
| Lunghezza massima del nome del percorso<br/> | 32.760 caratteri Unicode con ogni componente del percorso non più di 255 caratteri<br/> | 32.760 caratteri Unicode con ogni componente del percorso non più di 255 caratteri<br/> | 32.760 caratteri Unicode con ogni componente del percorso non più di 255 caratteri<br/> | 32.760 caratteri Unicode con ogni componente del percorso non più di 255 caratteri<br/> |
| Dimensione massima dei file<br/>        | 2 ^ 64 1 byte<br/>                                                                   | 2 ^ 64 1 byte<br/>                                                                   | 2 ^ 64 1 byte<br/>                                                                   | 4 GiB<br/>                                                                          |
| Dimensioni massime volume<br/>      | 16 TB (dimensioni del cluster da 4 KB) o 256TB (dimensione del cluster 64 KB)<br/>                        | 2 ^ 32 1 cluster (dimensioni massime del cluster = 2 ^ 25 1)<br/>                               | 2 ^ 32 blocchi<br/>                                                                    | 2 ^ 32 blocchi<br/>                                                                    |



 

## <a name="journaling-and-change-log"></a>Journaling e log delle modifiche



| Funzionalità                             | NTFS           | exFAT         | UDF           | FAT32         |
|-------------------------------------|----------------|---------------|---------------|---------------|
| Journaling solo metadati<br/> | Sì<br/> | No<br/> | No<br/> | No<br/> |
| Log modifiche file<br/>          | Sì<br/> | No<br/> | No<br/> | No<br/> |



 

## <a name="block-allocation-features"></a>Blocca funzionalità di allocazione



| Funzionalità                        | NTFS                                                                        | exFAT         | UDF            | FAT32         |
|--------------------------------|-----------------------------------------------------------------------------|---------------|----------------|---------------|
| Compressione della coda<br/>        | Sì (i file di piccole dimensioni vengono resi residenti nel descrittore del flusso MFT)<br/> | No<br/> | No<br/>  | No<br/> |
| Extents<br/>             | Sì<br/>                                                              | No<br/> | Sì<br/> | No<br/> |
| Dimensioni blocco variabili<br/> | No (impostato dal volume)<br/>                                           | No<br/> | No<br/>  | No<br/> |



 

## <a name="security"></a>Sicurezza



| Funzionalità                                  | NTFS                                                 | exFAT               | UDF                 | FAT32         |
|------------------------------------------|------------------------------------------------------|---------------------|---------------------|---------------|
| Rileva proprietario file<br/>              | Sì<br/>                                       | No<br/>       | No<br/>       | No<br/> |
| Autorizzazioni per file POSIX<br/>        | No (disponibile nella funzionalità del sottosistema POSIX)<br/> | No<br/>       | Sì<br/>      | No<br/> |
| Elenchi di controllo di accesso<br/>          | Sì<br/>                                       | No<br/>       | No<br/>       | No<br/> |
| Crittografia a livello di file System<br/> | Sì<br/>                                       | No<br/>       | No<br/>       | No<br/> |
| Checksum/ECC<br/>                  | No<br/>                                        | Metadati<br/> | Metadati<br/> | No<br/> |



 

## <a name="compression"></a>Compressione



| Funzionalità                         | NTFS           | exFAT         | UDF           | FAT32         |
|---------------------------------|----------------|---------------|---------------|---------------|
| Compressione incorporata<br/> | Sì<br/> | No<br/> | No<br/> | No<br/> |



 

## <a name="quotas"></a>Quote



| Funzionalità                               | NTFS                           | exFAT         | UDF           | FAT32         |
|---------------------------------------|--------------------------------|---------------|---------------|---------------|
| Spazio su disco a livello di utente<br/>      | Sì<br/>                 | No<br/> | No<br/> | No<br/> |
| Spazio su disco a livello di directory<br/> | No (vedere la nota sotto)<br/> | No<br/> | No<br/> | No<br/> |



 

**Nota**  La funzionalità quote di spazio su disco a livello di directory in NTFS è disponibile tramite il file server Gestione risorse.

## <a name="single-instance-store"></a>Archivio Single-Instance



| Funzionalità               | NTFS                           | exFAT         | UDF           | FAT32         |
|-----------------------|--------------------------------|---------------|---------------|---------------|
| A livello di file<br/> | No (vedere la nota sotto)<br/> | No<br/> | No<br/> | No<br/> |



 

**Nota**  L'archivio a istanza singola per NTFS è disponibile come parte della funzionalità di archiviazione a istanza singola di Windows Server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla gestione dei file](about-file-management.md)
</dt> <dt>

[Archivio a istanza singola e backup SIS](/windows/desktop/Backup/single-instance-store-and-sis-backup)
</dt> </dl>

 


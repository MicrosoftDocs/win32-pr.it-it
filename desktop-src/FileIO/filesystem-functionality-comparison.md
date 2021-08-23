---
description: Le tabelle che elencano funzionalità e funzionalità supportano i confronti per i quattro file system Windows, NTFS, exFAT, UDF e FAT32.
ms.assetid: 28cf2805-f1ce-46b4-bf08-a329f67f4d99
title: Confronto delle funzionalità del file system
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5af85dbacfd04920d8eb0a9558e0d57cc6e4020da35ffac57f7bdc703e6ef15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790691"
---
# <a name="file-system-functionality-comparison"></a>Confronto delle funzionalità del file system

Nelle tabelle seguenti sono elencati i confronti tra funzionalità e supporto delle funzionalità per i quattro file system Windows principali, NTFS, exFAT, UDF e FAT32:

-   [Funzionalità](#file-system-functionality-comparison)
-   [Limiti](#limits)
-   [Inserimento nel journal e log delle modifiche](#journaling-and-change-log)
-   [Funzionalità di allocazione blocchi](#block-allocation-features)
-   [Sicurezza](#security)
-   [Compressione](#compression)
-   [Quote](#quotas)
-   [Archivio a istanza singola](#single-instance-store)
-   [Argomenti correlati](#related-topics)

## <a name="functionality"></a>Funzionalità



| Funzionalità                             | NTFS                           | exFAT          | UDF                           | FAT32                      |
|-------------------------------------|--------------------------------|----------------|-------------------------------|----------------------------|
| Timestamp di creazione<br/>     | Sì<br/>                 | Sì<br/> | Sì<br/>                | Sì<br/>             |
| Timestamp dell'ultimo accesso<br/>  | No (vedere la nota sotto)<br/> | Sì<br/> | Sì<br/>                | Sì (solo data)<br/> |
| Timestamp dell'ultima modifica<br/>  | Sì<br/>                 | Sì<br/> | Sì<br/>                | Sì<br/>             |
| Timestamp dell'ultimo archivio<br/> | No<br/>                  | No<br/>  | No<br/>                 | No<br/>              |
| Con distinzione tra maiuscole e minuscole<br/>           | Sì (opzione)<br/>        | No<br/>  | Sì<br/>                | No<br/>              |
| Mantenimento delle maiuscole/minuscole<br/>          | Sì<br/>                 | Sì<br/> | Sì<br/>                | Sì<br/>             |
| Collegamenti reali<br/>               | Sì<br/>                 | No<br/>  | Sì<br/>                | No<br/>              |
| Soft link<br/>               | Sì<br/>                 | No<br/>  | No<br/>                 | No<br/>              |
| File sparse<br/>             | Sì<br/>                 | No<br/>  | Sì<br/>                | No<br/>              |
| Flussi denominati<br/>            | Sì<br/>                 | No<br/>  | Sì<br/>                | No<br/>              |
| Blocchi opportunistici (oplock)<br/>                  | Sì<br/>                 | Sì<br/> | Sì<br/>                | Sì<br/>             |
| Attributi estesi<br/>      | Sì<br/>                 | No<br/>  | Sì (solo su disco)<br/> | No<br/>              |
| Flussi dei dati alternativi<br/>   | Sì<br/>                 | No<br/>  | Sì<br/>                | No<br/>              |
| Punti di montaggio<br/>             | Sì<br/>                 | No<br/>  | No<br/>                 | No<br/>              |



 

**Windows Server 2003 e Windows XP:** Il campo timestamp dell'ultimo accesso NTFS viene aggiornato.

## <a name="limits"></a>Limiti



| Funzionalità                             | NTFS                                                                                      | exFAT                                                                                     | UDF                                                                                       | FAT32                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Lunghezza massima del nome del file<br/> | 255 caratteri Unicode<br/>                                                         | 255 caratteri Unicode<br/>                                                         | 127 caratteri Unicode o 254 caratteri ASCII<br/>                                            | 255 caratteri Unicode<br/>                                                         |
| Lunghezza massima del nome del percorso<br/> | 32.760 caratteri Unicode con ogni componente del percorso non più di 255 caratteri<br/> | 32.760 caratteri Unicode con ogni componente del percorso non più di 255 caratteri<br/> | 32.760 caratteri Unicode con ogni componente del percorso non più di 255 caratteri<br/> | 32.760 caratteri Unicode con ogni componente del percorso non più di 255 caratteri<br/> |
| Dimensione massima dei file<br/>        | 2^64 1 byte<br/>                                                                   | 2^64 1 byte<br/>                                                                   | 2^64 1 byte<br/>                                                                   | 4 GiB<br/>                                                                          |
| Dimensioni massime volume<br/>      | 16 TB (dimensioni del cluster da 4 KB) o 256 TB (dimensioni del cluster di 64 KB)<br/>                        | 2^32 1 cluster (dimensioni massime del cluster = 2^25 1)<br/>                               | 2^32 blocchi<br/>                                                                    | 2^32 blocchi<br/>                                                                    |



 

## <a name="journaling-and-change-log"></a>Inserimento nel journal e log delle modifiche



| Funzionalità                             | NTFS           | exFAT         | UDF           | FAT32         |
|-------------------------------------|----------------|---------------|---------------|---------------|
| Inserimento nel journal solo metadati<br/> | Sì<br/> | No<br/> | No<br/> | No<br/> |
| Log delle modifiche dei file<br/>          | Sì<br/> | No<br/> | No<br/> | No<br/> |



 

## <a name="block-allocation-features"></a>Funzionalità di allocazione blocchi



| Funzionalità                        | NTFS                                                                        | exFAT         | UDF            | FAT32         |
|--------------------------------|-----------------------------------------------------------------------------|---------------|----------------|---------------|
| Creazione di un pacchetto della parte finale<br/>        | Sì (i file di piccole dimensioni vengono resi residenti nel descrittore di flusso MFT)<br/> | No<br/> | No<br/>  | No<br/> |
| Extents<br/>             | Sì<br/>                                                              | No<br/> | Sì<br/> | No<br/> |
| Dimensioni dei blocchi variabili<br/> | No (impostato dal volume)<br/>                                           | No<br/> | No<br/>  | No<br/> |



 

## <a name="security"></a>Sicurezza



| Funzionalità                                  | NTFS                                                 | exFAT               | UDF                 | FAT32         |
|------------------------------------------|------------------------------------------------------|---------------------|---------------------|---------------|
| Tenere traccia del proprietario del file<br/>              | Sì<br/>                                       | No<br/>       | No<br/>       | No<br/> |
| Autorizzazioni per file POSIX<br/>        | No (disponibile nella funzionalità del sottosistema POSIX)<br/> | No<br/>       | Sì<br/>      | No<br/> |
| Elenchi di controllo di accesso<br/>          | Sì<br/>                                       | No<br/>       | No<br/>       | No<br/> |
| Crittografia a livello di file system<br/> | Sì<br/>                                       | No<br/>       | No<br/>       | No<br/> |
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



 

**Nota**  La funzionalità delle quote di spazio su disco a livello di directory in NTFS è disponibile tramite il file server Resource Manager.

## <a name="single-instance-store"></a>Single-Instance Store



| Funzionalità               | NTFS                           | exFAT         | UDF           | FAT32         |
|-----------------------|--------------------------------|---------------|---------------|---------------|
| A livello di file<br/> | No (vedere la nota sotto)<br/> | No<br/> | No<br/> | No<br/> |



 

**Nota**  L'archivio a istanza singola per NTFS è disponibile come parte della funzionalità Archiviazione istanza singola in Windows Server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla gestione dei file](about-file-management.md)
</dt> <dt>

[Archivio a istanza singola e backup SIS](/windows/desktop/Backup/single-instance-store-and-sis-backup)
</dt> </dl>

 


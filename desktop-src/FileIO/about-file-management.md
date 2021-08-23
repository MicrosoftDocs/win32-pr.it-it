---
description: Informazioni sulla gestione dei file.
ms.assetid: cf4e69b9-86dd-43a4-9011-6209fc65f550
title: Informazioni su Gestione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2544d31ecb95029053987a3d64e80f4cdf8c0f3170b3a679b542e145ca262947
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766371"
---
# <a name="about-file-management"></a>Informazioni su Gestione file

Gli argomenti seguenti contengono altre informazioni sulla gestione dei file.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                 | Descrizione                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Confronto delle funzionalità del file system](filesystem-functionality-comparison.md)<br/>            | Le tabelle che elencano funzionalità e funzionalità supportano i confronti per i quattro file system Windows, NTFS, exFAT, UDF e FAT32.<br/>                                                                           |
| [File e cluster](files-and-clusters.md)<br/>                                               | Un *file* è un'unità di dati nel file system a cui un utente può accedere e gestire.<br/>                                                                                                                              |
| [Creazione, eliminazione e gestione di file](creating--deleting--and-maintaining-files.md)<br/> | Funzioni da usare per creare, eliminare e gestire i file.<br/>                                                                                                                                                       |
| [Recupero e impostazione delle informazioni sui file](obtaining-and-setting-file-information.md)<br/>       | Funzioni da utilizzare per ottenere e impostare le informazioni sui file.<br/>                                                                                                                                                             |
| [Lettura e scrittura in file](reading-from-and-writing-to-files.md)<br/>                 | Un'applicazione legge e scrive in un file usando le [**funzioni ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) .<br/> |
| [Collegamento di file e directory](file-and-directory-linking.md)<br/>                               | Nella versione NTFS sono supportati due tipi di file system collegamenti: collegamenti rigidi [e giunzioni.](hard-links-and-junctions.md)<br/>                                                                                     |
| [Bloccare la clonazione](block-cloning.md)<br/>                                                         | *Un'operazione di clonazione* a blocchi indica file system copiare un intervallo di byte di file per conto di un'applicazione.<br/>                                                                                                |
| [Compressione e decompressione dei file](file-compression-and-decompression.md)<br/>               | L'file system NTFS usa Lempel-Ziv compressione, ovvero un algoritmo di compressione senza perdita di dati.<br/>                                                                                                                  |
| [Crittografia file](file-encryption.md)<br/>                                                     | Il file system crittografato (EFS) fornisce la protezione crittografica di singoli file nei volumi file system NTFS usando un sistema a chiave pubblica.<br/>                                                               |
| [Sicurezza dei file e diritti di accesso](file-security-and-access-rights.md)<br/>                     | Poiché i file [sono oggetti a](/windows/desktop/SecAuthZ/securable-objects)protezione diretta, l'accesso a essi è regolamentato dal modello di controllo di accesso che regola l'accesso a tutti gli altri oggetti a protezione diretta in Windows.<br/>                     |
| [Input e output (I/O)](input-and-output--i-o-.md)<br/>                                       | Windows consente di eseguire operazioni di input e output (I/O) sui componenti di archiviazione che si trovano in computer locali e remoti.<br/>                                                                        |
| [File sparse](sparse-files.md)<br/>                                                           | La compressione di file che contengono per lo più zeri consente un uso efficiente dello spazio su disco.<br/>                                                                                                                        |
| [Collegamenti simbolici](symbolic-links.md)<br/>                                                       | Un collegamento simbolico è un oggetto del file system che punta a un altro file system. L'oggetto a cui punta viene chiamato destinazione.<br/>                                                                          |



 

 


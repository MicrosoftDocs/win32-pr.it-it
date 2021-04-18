---
description: Informazioni sulla gestione dei file.
ms.assetid: cf4e69b9-86dd-43a4-9011-6209fc65f550
title: Informazioni sulla gestione dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe8e5f53a0021d4a6fba90a31698d05971e7bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307284"
---
# <a name="about-file-management"></a>Informazioni sulla gestione dei file

Negli argomenti seguenti sono contenute ulteriori informazioni sulla gestione dei file.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                 | Descrizione                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Confronto delle funzionalità del file System](filesystem-functionality-comparison.md)<br/>            | Le tabelle in cui sono elencate le funzionalità e le funzionalità supportano i confronti per i quattro file System Windows principali, NTFS, exFAT, UDF e FAT32.<br/>                                                                           |
| [File e cluster](files-and-clusters.md)<br/>                                               | Un *file* è un'unità di dati nel file System a cui un utente può accedere e gestire.<br/>                                                                                                                              |
| [Creazione, eliminazione e gestione di file](creating--deleting--and-maintaining-files.md)<br/> | Funzioni da utilizzare per creare, eliminare e gestire i file.<br/>                                                                                                                                                       |
| [Recupero e impostazione delle informazioni sui file](obtaining-and-setting-file-information.md)<br/>       | Funzioni da utilizzare per ottenere e impostare le informazioni sul file.<br/>                                                                                                                                                             |
| [Lettura e scrittura nei file](reading-from-and-writing-to-files.md)<br/>                 | Un'applicazione legge e scrive in un file usando le funzioni [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) .<br/> |
| [Collegamento di file e directory](file-and-directory-linking.md)<br/>                               | Nel file system NTFS sono supportati due tipi di collegamenti: [collegamenti reali e giunzioni](hard-links-and-junctions.md).<br/>                                                                                     |
| [Clonazione del blocco](block-cloning.md)<br/>                                                         | Un'operazione di *clonazione a blocchi* indica al file System di copiare un intervallo di byte di file per conto di un'applicazione.<br/>                                                                                                |
| [Compressione e decompressione dei file](file-compression-and-decompression.md)<br/>               | Il file system NTFS utilizza la compressione Lempel-Ziv, ovvero un algoritmo di compressione senza perdita di perdite.<br/>                                                                                                                  |
| [Crittografia file](file-encryption.md)<br/>                                                     | Il file system crittografato (EFS) fornisce la protezione crittografica dei singoli file nei volumi file system NTFS usando un sistema a chiave pubblica.<br/>                                                               |
| [Sicurezza file e diritti di accesso](file-security-and-access-rights.md)<br/>                     | Poiché i file sono [oggetti a protezione diretta](/windows/desktop/SecAuthZ/securable-objects), l'accesso viene regolato dal modello di controllo di accesso che regola l'accesso a tutti gli altri oggetti a protezione diretta di Windows.<br/>                     |
| [Input e output (I/O)](input-and-output--i-o-.md)<br/>                                       | Windows consente di eseguire operazioni di I/O (input e output) sui componenti di archiviazione che si trovano in computer locali e remoti.<br/>                                                                        |
| [File sparse](sparse-files.md)<br/>                                                           | La compressione dei file che contengono principalmente zeri consente un uso efficiente dello spazio su disco.<br/>                                                                                                                        |
| [Collegamenti simbolici](symbolic-links.md)<br/>                                                       | Un collegamento simbolico è un oggetto di file System che punta a un altro oggetto file system. L'oggetto a cui si fa riferimento è denominato destinazione.<br/>                                                                          |



 

 


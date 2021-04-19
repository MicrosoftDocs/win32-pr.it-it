---
description: I volumi vengono implementati da un driver di dispositivo denominato responsabile del volume.
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: Informazioni sulla gestione dei volumi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0767d137eeecaa4ded060382b689b5ea3780dcbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317814"
---
# <a name="about-volume-management"></a>Informazioni sulla gestione dei volumi

I volumi vengono implementati da un driver di dispositivo denominato responsabile del volume. Gli esempi includono FtDisk Manager, gestione dischi logici (LDM) e VERITAS Logical Volume Manager (LVM). I responsabili del volume forniscono un livello di astrazione fisica, protezione dei dati (tramite una forma di RAID) e prestazioni.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                       | Descrizione                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Riconoscimento del file System](file-system-recognition.md)<br/>           | L'obiettivo del riconoscimento file system consiste nel consentire al sistema operativo Windows di disporre di un'opzione aggiuntiva per un file system valido ma non riconosciuto diverso da "RAW".<br/>                                                                                                         |
| [Denominazione di un volume](naming-a-volume.md)<br/>                           | Un'etichetta è un nome descrittivo assegnato a un volume, in genere da un utente finale, per renderlo più semplice da riconoscere. Un volume può avere un'etichetta, una lettera di unità, entrambi o nessuno. Per impostare l'etichetta per un volume, utilizzare la funzione [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .<br/> |
| [Enumerazione dei volumi](enumerating-volumes.md)<br/>                   | Per ottenere un elenco completo dei volumi in un computer o per modificare ogni volume a sua volta, è possibile enumerare i volumi.<br/>                                                                                                                                                       |
| [Recupero delle informazioni sul volume](obtaining-volume-information.md)<br/> | Prima di accedere a file e directory in un volume specifico, è necessario determinare le funzionalità del file system usando la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) .<br/>                                                                              |
| [Journal delle modifiche](change-journals.md)<br/>                           | Quando viene apportata una modifica a un file o a una directory in un volume, il Journal delle modifiche USN per tale volume viene aggiornato con una descrizione della modifica e il nome del file o della directory.<br/>                                                                                        |
| [Cartelle montate](volume-mount-points.md)<br/>                       | Con le cartelle montate è possibile unificare diversi file System, ad esempio NTFS file system, un file system FAT a 16 bit e un file system ISO-9660 in un'unità CD-ROM in un file system logico in un singolo volume NTFS.<br/>                                                      |
| [Tabella file master](master-file-table.md)<br/>                       | Tutte le informazioni su un file, incluse le dimensioni, gli indicatori di data e ora, le autorizzazioni e il contenuto dei dati, vengono archiviati nelle voci della tabella file master (MFT) o nello spazio esterno alla MFT descritta dalle voci MFT.<br/>                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento tecnico per dischi e volumi di base](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Guida di riferimento tecnico ai dischi e ai volumi dinamici](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Riferimento per gestione volume](volume-management-reference.md)
</dt> </dl>

 


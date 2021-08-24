---
description: I volumi vengono implementati da un driver di dispositivo denominato gestione volumi.
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: Informazioni sulla gestione dei volumi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5446726b7caf448eef74884e8b6afc9d27dc4d4fdc6ffadd4572e667aaeb2cf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766311"
---
# <a name="about-volume-management"></a>Informazioni sulla gestione dei volumi

I volumi vengono implementati da un driver di dispositivo denominato gestione volumi. Ad esempio, FtDisk Manager, Logical Disk Manager (LDM) e VERITAS Logical Volume Manager (LVM). I gestori di volumi offrono un livello di astrazione fisica, protezione dei dati (con una qualche forma di RAID) e prestazioni.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                       | Descrizione                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Riconoscimento del file system](file-system-recognition.md)<br/>           | L'obiettivo file system riconoscimento è consentire al sistema operativo Windows di avere un'opzione aggiuntiva per un file system valido ma non riconosciuto diverso da "RAW".<br/>                                                                                                         |
| [Denominazione di un volume](naming-a-volume.md)<br/>                           | Un'etichetta è un nome descrittivo assegnato a un volume, in genere da un utente finale, per semplificarne il riconoscimento. Un volume può avere un'etichetta, una lettera di unità, entrambi o nessuno dei due. Per impostare l'etichetta per un volume, usare la [**funzione SetVolumeLabel.**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela)<br/> |
| [Enumerazione dei volumi](enumerating-volumes.md)<br/>                   | Per creare un elenco completo dei volumi in un computer o modificare ogni volume a sua volta, è possibile enumerare i volumi.<br/>                                                                                                                                                       |
| [Recupero di informazioni sul volume](obtaining-volume-information.md)<br/> | Prima di accedere a file e directory in un determinato volume, è necessario determinare le funzionalità del file system usando la [**funzione GetVolumeInformation.**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                                                                              |
| [Journal delle modifiche](change-journals.md)<br/>                           | Quando viene apportata una modifica a un file o a una directory in un volume, il journal delle modifiche USN per tale volume viene aggiornato con una descrizione della modifica e il nome del file o della directory.<br/>                                                                                        |
| [Cartelle montate](volume-mount-points.md)<br/>                       | Usando le cartelle montate, è possibile unificare file system diversi, ad esempio il file system NTFS, un file system FAT a 16 bit e un file system ISO-9660 in un'unità CD-ROM in un unico file system logico in un singolo volume NTFS.<br/>                                                      |
| [Tabella file master](master-file-table.md)<br/>                       | Tutte le informazioni su un file, incluse le dimensioni, gli indicatori di data e ora, le autorizzazioni e il contenuto dei dati, vengono archiviate nelle voci della tabella file master (MFT) o nello spazio esterno a MFT descritto dalle voci MFT.<br/>                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni tecniche su dischi e volumi di base](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Informazioni di riferimento tecnico su dischi e volumi dinamici](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Informazioni di riferimento sulla gestione dei volumi](volume-management-reference.md)
</dt> </dl>

 


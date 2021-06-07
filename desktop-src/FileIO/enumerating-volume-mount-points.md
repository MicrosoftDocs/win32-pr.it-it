---
description: Funzioni da usare per enumerare le cartelle montate in un volume.
ms.assetid: 052a363f-adfd-4f66-a8b0-5d9d37eedcb0
title: Enumerazione delle cartelle montate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b047e4af74f33d6bc56476734f0f39c41dd14f
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386660"
---
# <a name="enumerating-mounted-folders"></a>Enumerazione delle cartelle montate

Le funzioni seguenti vengono usate per enumerare le cartelle montate in un volume NTFS specificato:

-   [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)

Queste funzioni funzionano in modo molto simile alle [**funzioni FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose.**](/windows/desktop/api/FileAPI/nf-fileapi-findclose)

Per enumerare le cartelle montate in un volume, verificare innanzitutto se il volume supporta le cartelle montate. A tale scopo, usare il nome del volume restituito dalle funzioni [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) e [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) per chiamare la [**funzione GetVolumeInformation.**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) I nomi restituiti includono una barra rovesciata finale ( ) per essere compatibili con \\ la [**funzione GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) e le funzioni correlate. Per altre informazioni sulle funzioni usate per analizzare i volumi in un computer, vedere [Enumerazione dei volumi.](enumerating-volumes.md) Quando si chiama la **funzione GetVolumeInformation,** se "NTFS" viene restituito nel *parametro lpFileSystemNameBuffer,* il volume è un volume NTFS. Il file system NTFS supporta le cartelle montate.

Se il volume è un volume NTFS, avviare una ricerca delle cartelle montate chiamando [**FindFirstVolumeMountPoint.**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) Se la ricerca ha esito positivo, elaborare i risultati in base ai requisiti dell'applicazione. Usare quindi [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa) in un ciclo per individuare ed elaborare le cartelle montate una alla volta. Quando non sono più presenti cartelle montate da enumerare, chiudere l'handle di ricerca chiamando [**FindVolumeMountPointClose.**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) Si noti che la ricerca troverà solo le cartelle montate presenti nel volume specificato.

Non si deve presupporre alcuna correlazione tra l'ordine delle cartelle montate restituite da queste funzioni e l'ordine delle cartelle montate restituite da altri strumenti o funzioni.

 

 




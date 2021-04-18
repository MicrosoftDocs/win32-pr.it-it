---
description: Funzioni da utilizzare per enumerare le cartelle montate in un volume.
ms.assetid: 052a363f-adfd-4f66-a8b0-5d9d37eedcb0
title: Enumerazione di cartelle montate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29585100a4b8a94e1b7b78d36b6f0fda228094d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313883"
---
# <a name="enumerating-mounted-folders"></a>Enumerazione di cartelle montate

Le funzioni seguenti vengono utilizzate per enumerare le cartelle montate in un volume NTFS specificato:

-   [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)

Queste funzioni funzionano in modo molto simile alle funzioni [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .

Per enumerare le cartelle montate in un volume, verificare prima di tutto se il volume supporta le cartelle montate. A tale scopo, usare il nome del volume restituito dalle funzioni [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) e [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) per chiamare la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) . I nomi restituiti includono una barra rovesciata finale ( \) per essere compatibile con la funzione [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) e le funzioni correlate). Per ulteriori informazioni sulle funzioni utilizzate per analizzare i volumi in un computer, vedere [enumerazione dei volumi](enumerating-volumes.md). Quando si chiama la funzione **GetVolumeInformation** , se nel parametro *lpFileSystemNameBuffer* viene restituito "NTFS", il volume è un volume NTFS. Il file system NTFS supporta le cartelle montate.

Se il volume è un volume NTFS, iniziare la ricerca delle cartelle montate chiamando [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa). Se la ricerca ha esito positivo, elaborare i risultati in base ai requisiti dell'applicazione. Usare quindi [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa) in un ciclo per individuare ed elaborare le cartelle montate una alla volta. Quando non sono presenti altre cartelle montate da enumerare, chiudere l'handle di ricerca chiamando [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose). Si noti che la ricerca troverà solo le cartelle montate che si trovano nel volume specificato.

Non è consigliabile presupporre alcuna correlazione tra l'ordine delle cartelle montate restituite da queste funzioni e l'ordine delle cartelle montate restituite da altre funzioni o strumenti.

 

 




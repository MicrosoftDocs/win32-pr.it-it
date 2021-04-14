---
description: Prima di accedere a file e directory in un volume specifico, è necessario determinare le funzionalità del file system usando la funzione GetVolumeInformation.
ms.assetid: 008e0cc4-bc12-47e8-a8b7-d4fa9395fceb
title: Recupero delle informazioni sul volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc5323c3f82db1115a81902f156e9366abad31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527043"
---
# <a name="obtaining-volume-information"></a>Recupero delle informazioni sul volume

La funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) recupera le informazioni relative all'file System su un volume specificato. Queste informazioni includono il nome del volume, il numero di serie del volume, il nome file system, i flag file system, la lunghezza massima di un nome file e così via. Prima di accedere a file e directory in un volume specifico, è necessario determinare le funzionalità del file system usando la funzione [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) . Questa funzione restituisce i valori che è possibile usare per adattare l'applicazione in modo che funzioni con l'file system.

In generale, è consigliabile evitare di utilizzare buffer statici per i nomi file e i percorsi. Usare invece i valori restituiti da [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) per allocare i buffer in base alle esigenze. Se è necessario utilizzare buffer statici, riservare 256 caratteri per i nomi file e 260 caratteri per i percorsi.

Le funzioni [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) e [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) recuperano rispettivamente i percorsi della directory di sistema e della directory di Windows.

La funzione [**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea) recupera le informazioni sull'organizzazione su un volume, inclusi il numero di byte per settore, il numero di settori per cluster, il numero di cluster disponibili e il numero totale di cluster. Tuttavia, **GetDiskFreeSpace** non è in grado di segnalare dimensioni del volume maggiori di 2 GB. Per assicurarsi che l'applicazione funzioni con dischi rigidi con capacità elevata, usare la funzione [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) .

La funzione [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) indica se il volume a cui fa riferimento la lettera di unità specificata è rimovibile, fisso, CD-ROM, RAM o unità di rete.

La funzione [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) identifica i volumi presenti. La funzione [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw) recupera una stringa con terminazione null per ogni volume presente. Usare queste stringhe ogni volta che è richiesta una directory radice.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riconoscimento del file System](file-system-recognition.md)
</dt> </dl>

 

 

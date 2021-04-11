---
description: Controllo della memorizzazione nella cache in Transactional NTFS.
ms.assetid: 0fd272ee-cf5f-4ba9-b8aa-ff0016f51d4b
title: Distribuzione di Transactional NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7c44e0ad3b83854e56d18171072a7cb4615d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967107"
---
# <a name="deploying-transactional-ntfs"></a>Distribuzione di Transactional NTFS

Transactional NTFS (TxF), come la maggior parte dei meccanismi di transazione, dipende dall'ordinamento corretto delle Scritture di dati. Verificare che l'ordine di scrittura appropriato richieda il controllo esplicito della memorizzazione nella cache dei dati Per soddisfare questo requisito, TxF richiede che le unità disco implementino i meccanismi di controllo della memorizzazione nella cache che fanno parte di interfacce di unità standardizzate come SCSI, SATA e ATA.

Il meccanismo di controllo della memorizzazione nella cache usato da TxF è un flag noto come funzione FUA (Force Unit Access). Questo flag specifica che l'unità deve scrivere i dati in un archivio multimediale stabile prima del completamento della segnalazione. In alcuni punti critici all'interno di una transazione, TxF deve emettere un FUA per garantire che alcuni dati di controllo necessari per eseguire correttamente il rollback di una transazione non vadano persi se si verifica un errore di alimentazione.

Le unità disco di classe server (SCSI e Fiber Channel) supportano in genere il flag FUA. A partire da vista, Windows supporta il flag FUA solo per i dischi SCSI e Fibre Channel.

Nelle unità di prodotti (ATA/SATA/USB) TxF presenta periodi di vulnerabilità durante i quali un'interruzione dell'alimentazione di un'unità può comportare la mancata esecuzione del rollback della transazione da parte di TxF, in modo da lasciare i dati in uno stato incoerente, a meno che la cache di scrittura dell'unità non sia disabilitata.

Alcune schede bus host (HBA) e i controller di archiviazione (ad esempio, i sistemi RAID) dispongono di cache con supporto integrato per le batterie. Poiché questi dispositivi conservano i dati memorizzati nella cache se si verifica un errore di alimentazione, non è necessario che i dischi connessi a tali dispositivi rispettino il flag FUA. Inoltre, un disco il cui alimentatore è protetto da un alimentatore senza interruzioni (UPS) non deve rispettare il flag FUA. Ciò è dovuto al fatto che il gruppo di continuità manterrà il consumo di energia sufficiente affinché il disco scarichi la cache sul supporto.

La disabilitazione della cache di scrittura di un'unità elimina la necessità per l'unità di rispettare il flag FUA. È possibile disabilitare la memorizzazione nella cache di scrittura di un disco tramite il codice di controllo delle [**informazioni della cache del \_ set di dischi \_ \_ \_ IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_set_cache_information) sul disco. Lo stato della cache di scrittura (on/off) verrà mantenuto tra i riavvii del sistema. Il rilascio di questo codice di controllo avrà conseguenze molto significative sulle prestazioni per tutte le I/O rilasciate su tale disco, il che probabilmente sarà un notevole calo delle prestazioni. L'uso di questo codice di controllo deve essere considerato attentamente prima della distribuzione.

> [!Note]  
> Affinché TxF sia in grado di proteggere costantemente l'integrità dei dati tramite errori di alimentazione, il sistema deve soddisfare almeno uno dei criteri seguenti:
>
> -   Usare dischi di classe server (SCSI, Fibre Channel).
> -   Assicurarsi che i dischi siano connessi a una scheda HBA di Caching con batteria.
> -   Utilizzare un controller di archiviazione (ad esempio, sistema RAID) come dispositivo di archiviazione.
> -   Assicurarsi che l'alimentazione del disco sia protetta da un UPS.
> -   Verificare che la funzionalità di memorizzazione nella cache in scrittura del disco sia disabilitata.

 

 

 




---
description: L'obiettivo del riconoscimento file system consiste nel consentire al sistema operativo Windows di disporre di un'opzione aggiuntiva per un file system valido ma non riconosciuto diverso da &\# 0034;&RAW \# 0034;.
ms.assetid: a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3
title: Riconoscimento del file System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 457d4146588ba2db2b75d06c7afac10ecb18e87c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310021"
---
# <a name="file-system-recognition"></a>Riconoscimento del file System

L'obiettivo del riconoscimento file system consiste nel consentire al sistema operativo Windows di disporre di un'opzione aggiuntiva per un file system valido ma non riconosciuto diverso da "RAW". A tale scopo, a partire da Windows 7 e Windows Server 2008 R2, il sistema definisce un tipo di struttura dati fissa che può essere scritto nei supporti in cui è attiva una tecnologia abilitata che modifica il formato file system. Questa struttura di dati, se presente sul settore del disco logico zero, viene quindi riconosciuta dal sistema operativo e informa l'utente che il supporto contiene un file system valido ma non riconosciuto e non è un volume non elaborato se i driver per il file system non sono installati.

## <a name="file-system-recognition-features-and-use"></a>Funzionalità di riconoscimento e utilizzo del file System

Diverse tecnologie di archiviazione recenti hanno modificato il formato di file system su disco in modo che i supporti su cui sono abilitate tali tecnologie diventano non riconoscibili per le versioni precedenti di Windows a causa dei driver file system non esistenti quando è stata rilasciata una versione precedente di Windows. Di seguito è riportato il comportamento predefinito precedente in questo scenario. Quando il supporto di archiviazione non è un file system noto, viene identificato come RAW e quindi propagato alla shell di Windows, dove AutoPlay richiede l'interfaccia utente del formato. Il riconoscimento del file System può risolvere questo problema se gli autori del nuovo file system scrivono correttamente la [**struttura di dati**](file-system-recognition-structure.md) corretta sul disco.

Il riconoscimento del file System usa le funzionalità e i livelli seguenti all'interno del sistema operativo per raggiungere gli obiettivi:

-   Supporti di archiviazione, in cui una struttura di dati fissa risiede in una sequenza di byte disposti internamente in una struttura predefinita denominata struttura dei dati della [**\_ struttura di \_ riconoscimento \_ del file System**](file-system-recognition-structure.md) . È responsabilità dello sviluppatore file system creare correttamente questa struttura su disco.
-   Riconoscimento del file System a livello di applicazione, ottenibile tramite l'uso del codice di controllo di I/O del [**\_ \_ file \_ System \_ di query FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition) . Per un esempio di come usare questo codice di controllo, vedere [ottenere informazioni sul riconoscimento del file System](obtaining-file-system-recognition-information.md).
-   Codice di convalida del checksum, archiviato nella struttura dei dati della [**\_ struttura di \_ riconoscimento \_ del file System**](file-system-recognition-structure.md) . Per un esempio di come calcolare questo checksum, vedere [calcolo di un checksum di riconoscimento del file System](computing-a-file-system-recognition-checksum.md).
-   L'interfaccia utente della shell di Windows usa le funzionalità elencate in precedenza per fornire un AutoPlay più flessibile e affidabile e il supporto correlato per i file System non riconosciuti, ma può funzionare solo se la struttura dei dati della [**\_ struttura di \_ riconoscimento \_ del file System**](file-system-recognition-structure.md) esiste nel settore del disco logico zero. Gli sviluppatori che implementano nuovi file System devono utilizzare questo sistema per garantire che i file system non vengano erroneamente considerati di tipo "RAW".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Calcolo di un checksum di riconoscimento del file System](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Recupero delle informazioni di riconoscimento del file System](obtaining-file-system-recognition-information.md)
</dt> <dt>

[Recupero delle informazioni sul volume](obtaining-volume-information.md)
</dt> </dl>

 

 

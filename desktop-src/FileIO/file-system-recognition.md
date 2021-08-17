---
description: L'obiettivo del riconoscimento file system è quello di consentire al sistema operativo Windows di avere un'opzione aggiuntiva per un file system valido ma non riconosciuto diverso da \# &0034; RAW&\# 0034;.
ms.assetid: a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3
title: Riconoscimento del file system
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cf33e8a6e3378ad5b9f0123cb78fa228b5b780e7440a2981b10982e76d187a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996958"
---
# <a name="file-system-recognition"></a>Riconoscimento del file system

L'obiettivo file system riconoscimento è quello di consentire al sistema operativo Windows di avere un'opzione aggiuntiva per un'file system valida ma non riconosciuta diversa da "RAW". A tale scopo, a partire da Windows 7 e Windows Server 2008 R2, il sistema definisce un tipo di struttura di dati fissa che può essere scritto nel supporto in cui è attiva una tecnologia abilitata che modifica il formato file system. Questa struttura dei dati, se presente nel settore del disco logico zero, verrà quindi riconosciuta dal sistema operativo e informerà l'utente che il supporto contiene un file system valido ma non riconosciuto e non è un volume RAW se i driver per il file system non sono installati.

## <a name="file-system-recognition-features-and-use"></a>Funzionalità e uso del riconoscimento del file system

Diverse tecnologie di archiviazione recenti hanno modificato il formato di file system su disco in modo che i supporti in cui queste tecnologie sono abilitate diventino irriconoscibili rispetto alle versioni precedenti di Windows a causa dei driver di file system non esistenti quando è stata rilasciata una particolare versione precedente di Windows. Il comportamento predefinito precedente in questo scenario era il seguente. Quando il supporto di archiviazione non è un file system noto, viene identificato come RAW e quindi propagato alla shell di Windows, dove La riproduzione automatica richiede con l'interfaccia utente di formattazione. Il riconoscimento del file system può risolvere questo problema se gli autori del nuovo file system scrivono correttamente la struttura [**dei dati**](file-system-recognition-structure.md) corretta sul disco.

Il riconoscimento del file system usa le funzionalità e i livelli seguenti all'interno del sistema operativo per raggiungere i propri obiettivi:

-   Archiviazione, in cui una struttura di dati fissa risiede come una sequenza di byte disposti internamente in una struttura predefinita denominata struttura dei dati RECOGNITION STRUCTURE del [**FILE \_ SYSTEM. \_ \_**](file-system-recognition-structure.md) È responsabilità dello sviluppatore file system creare correttamente questa struttura su disco.
-   Riconoscimento del file system a livello di applicazione, ottenuto tramite l'uso del codice di controllo I/O del dispositivo [**FSCTL \_ QUERY FILE SYSTEM \_ \_ \_ RECOGNITION.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition) Per un esempio di come usare questo codice di controllo, vedere [Obtaining File System Recognition Information](obtaining-file-system-recognition-information.md).
-   Codice di convalida del checksum, archiviato all'interno della struttura dei dati RECOGNITION STRUCTURE di [**FILE \_ SYSTEM. \_ \_**](file-system-recognition-structure.md) Per un esempio di come calcolare questo checksum, vedere Calcolo [di un checksum di riconoscimento del file system.](computing-a-file-system-recognition-checksum.md)
-   L'interfaccia utente di Windows Shell usa le funzionalità elencate in precedenza per offrire una riproduzione automatica più flessibile e affidabile e il supporto correlato per i file system non riconosciuti, ma può funzionare solo se la struttura dei dati STRUTTURA DI RICONOSCIMENTO [**FILE \_ SYSTEM \_ \_**](file-system-recognition-structure.md) esiste nel settore del disco logico zero. Gli sviluppatori che implementano nuovi file system devono usare questo sistema per assicurarsi che il file system non sia erroneamente considerato di tipo "RAW".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Calcolo di un checksum di riconoscimento del file system](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Recupero di informazioni di riconoscimento del file system](obtaining-file-system-recognition-information.md)
</dt> <dt>

[Recupero di informazioni sui volumi](obtaining-volume-information.md)
</dt> </dl>

 

 

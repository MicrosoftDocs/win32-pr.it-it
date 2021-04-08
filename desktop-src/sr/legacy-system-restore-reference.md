---
title: Riferimento ripristino configurazione di sistema legacy
description: Questa documentazione descrive i dettagli di implementazione del repository usati da una versione legacy di ripristino configurazione di sistema. Non si applica all'implementazione di ripristino configurazione di sistema in Windows Vista.
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8703cbf88b97458f07c616d48405708e25acec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855458"
---
# <a name="legacy-system-restore-reference"></a>Riferimento ripristino configurazione di sistema legacy

\[Queste informazioni si applicano solo a Windows XP con Service Pack 2 (SP2).\]

Questa documentazione descrive i dettagli di implementazione del repository usati da una versione legacy di ripristino configurazione di sistema. Non si applica all'implementazione di ripristino configurazione di sistema in Windows Vista.

## <a name="system-restore-repository-structure"></a>Struttura del repository di ripristino del sistema

Windows XP con SP2 contiene un repository per ripristino configurazione di sistema nella cartella seguente:% SYSTEMDRIVE% \\ System Volume Information. Questo repository contiene informazioni per i punti di ripristino, che sono essenzialmente uno snapshot del sistema in un momento specifico.

Il repository è strutturato nel modo seguente:

**System Volume Information**    ** \_ Restore {*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP * n** *     ** \_ Restore {*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP * n***

Per determinare quale \_ cartella di ripristino {*GUID*} usare, leggere il **GUID** specificato nel file seguente: SYSTEMROOT% \\ system32 \\ Restore \\MachineGUID.txt.

All'interno di ogni \_ cartella Restore {*GUID*}, il \_ file driver. cfg contiene informazioni provenienti da una struttura di **\_ \_ configurazione persistente SR** definita nel modo seguente:

``` syntax
typedef struct _SR_PERSISTENT_CONFIG
 {      
  ULONG Signature;            // Set to CPrs
  ULONG FileNameNumber;       // Number for next temp file 
                              // For example, A0000001 would be 1  
  INT64 FileSeqNumber;        // Next sequence number
  ULONG CurrentRestoreNumber; // For example, RP5 would be 5
 } SR_PERSISTENT_CONFIG, * PSR_PERSISTENT_CONFIG;
```

## <a name="files-contained-in-each-rpnfolder"></a>File contenuti in ogni cartella RP *n*

Ogni cartella RP *n* contiene una cartella snapshot che contiene gli elementi seguenti:

-   Uno snapshot degli hive del registro di sistema
-   Una cartella del repository che contiene uno snapshot del repository WMI
-   Snapshot del database COM+
-   Uno snapshot del database IIS

Ogni cartella RP *n* contiene un file RP. log che contiene informazioni generali sul punto di ripristino dalla struttura [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) .

Ogni cartella RP *n* può contenere file usati per tenere traccia delle modifiche per un punto di ripristino. Il primo file è denominato Change. log, il file successivo è denominato Change. log. 1 e così via. Ogni file di log delle modifiche contiene le strutture seguenti:

-   [**MODIFICARE \_ l' \_ intestazione del log**](change-log-header.md)
-   [**Modifica \_ di \_Voce di log**](change-log-entry.md)1
-   [**Modifica \_ di \_Voce di log**](change-log-entry.md)2
-   ...
-   [**Modifica \_ di \_Voce di log**](change-log-entry.md)*n*

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strutture di ripristino del sistema legacy](legacy-system-restore-structures.md)
</dt> </dl>

 

 





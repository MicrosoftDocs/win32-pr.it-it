---
description: Registrazione e segnalazione errori
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Registrazione e segnalazione errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdc29d32ae26429f2fe23fe88762fabf82185c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305213"
---
# <a name="logging-and-error-reporting"></a>Registrazione e segnalazione errori

## <a name="log-file"></a>File di registro

COMREPL genera un file di log contenente i messaggi di stato e di errore. Questo file è archiviato nel computer in cui COMREPL è stato avviato in% systemdir% \\ com \\ Replication \\ comrepl. log.

Questo file di log viene cancellato quando viene avviata una fase di copia. L'installazione successiva nelle destinazioni viene aggiunta al file.

## <a name="error-handling"></a>Gestione degli errori

Gli errori sono indicati nel file di log descritto in precedenza. Per informazioni dettagliate sull'errore, vedere il registro eventi nei computer di origine o di destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei file](file-management.md)
</dt> <dt>

[Fasi di replica](replication-phases.md)
</dt> <dt>

[Uso di COMREPL](using-comrepl.md)
</dt> <dt>

[Cosa viene replicato](what-gets-replicated.md)
</dt> </dl>

 

 




---
description: Registrazione e segnalazione errori
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Registrazione e segnalazione errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d974b4043b4365839aec6a4fae392ae1d84900e8b8347949147b8df13326bd1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990761"
---
# <a name="logging-and-error-reporting"></a>Registrazione e segnalazione errori

## <a name="log-file"></a>File di registro

COMREPL genera un file di log contenente messaggi di stato e di errore. Questo file viene archiviato nel computer in cui è stato avviato COMREPL in %systemdir% \\ com \\ replication \\ ComRepl.log.

Questo file di log viene cancellato all'avvio di una fase di copia. L'installazione successiva nelle destinazioni verrà aggiunta al file.

## <a name="error-handling"></a>Gestione degli errori

Gli errori vengono indicati nel file di log descritto in precedenza. Informazioni dettagliate sull'errore sono disponibili anche nel registro eventi nei computer di origine o di destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei file](file-management.md)
</dt> <dt>

[Fasi di replica](replication-phases.md)
</dt> <dt>

[Uso di COMREPL](using-comrepl.md)
</dt> <dt>

[Elementi replicati](what-gets-replicated.md)
</dt> </dl>

 

 




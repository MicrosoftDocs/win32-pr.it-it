---
title: Database WinSNMP
description: L'implementazione di Microsoft WinSNMP gestisce un archivio di informazioni amministrative in un database.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83573cad12c05f6dd4b7e2375df5941e05fadb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471094"
---
# <a name="the-winsnmp-database"></a>Database WinSNMP

L'implementazione di Microsoft WinSNMP gestisce un archivio di informazioni amministrative in un database. Il database include le seguenti informazioni:

-   Proprietà della rete e della versione.

    L'implementazione utilizza queste proprietà per determinare il protocollo di trasporto di rete e il Framework della versione SNMP da utilizzare per completare le richieste di trasmissione. Per ulteriori informazioni, vedere [informazioni sulle versioni SNMP](about-snmp-versions.md).

-   Modalità di conversione dell'entità e del contesto.

    L'implementazione utilizza questa modalità per interpretare i nomi descrittivi per le entità e i contesti SNMP. Per ulteriori informazioni, vedere [impostazione della modalità di conversione dell'entità e del contesto](setting-the-entity-and-context-translation-mode.md).

-   Impostazione dei criteri di ritrasmissione.

    L'implementazione usa questa impostazione per determinare se eseguire o meno i criteri di ritrasmissione dell'applicazione. L'implementazione archivia un valore di timeout e un numero di tentativi per ogni entità di destinazione. Per ulteriori informazioni, vedere [informazioni sulla ritrasmissione](about-retransmission.md) e [la gestione dei criteri di ritrasmissione](managing-the-retransmission-policy.md).

 

 





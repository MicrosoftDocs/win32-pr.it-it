---
title: The WinSNMP Database
description: L'implementazione Microsoft WinSNMP gestisce un archivio di informazioni amministrative in un database.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc2f478c9bb1c05d3a094e2a15fac0a9cef5968f245257a0702d045eb90bd2fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886001"
---
# <a name="the-winsnmp-database"></a>The WinSNMP Database

L'implementazione Microsoft WinSNMP gestisce un archivio di informazioni amministrative in un database. Il database include le informazioni seguenti:

-   Proprietà di rete e versione.

    L'implementazione usa queste proprietà per determinare il protocollo di trasporto di rete e il framework di versione SNMP da usare per completare le richieste di trasmissione. Per altre informazioni, vedere [Informazioni sulle versioni SNMP.](about-snmp-versions.md)

-   Modalità di conversione di entità e contesto.

    L'implementazione usa questa modalità per interpretare i nomi descrittivi per le entità e i contesti SNMP. Per altre informazioni, vedere [Impostazione della modalità di conversione di entità e contesto](setting-the-entity-and-context-translation-mode.md).

-   Impostazione dei criteri di ritrasmissione.

    L'implementazione usa questa impostazione per determinare se deve eseguire o meno i criteri di ritrasmissione dell'applicazione. L'implementazione archivia un valore di timeout e un numero di tentativi per ogni entità di destinazione. Per altre informazioni, vedere [Informazioni sulla ritrasmissione](about-retransmission.md) [e gestione dei criteri di ritrasmissione.](managing-the-retransmission-policy.md)

 

 





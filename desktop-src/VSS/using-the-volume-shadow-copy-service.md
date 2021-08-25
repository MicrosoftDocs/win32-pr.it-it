---
description: Le operazioni di backup e ripristino vss usano ognuna un protocollo per l'interazione dei sistemi che usano l'archiviazione di massa (writer) e di quelli che ne esercitino il backup (richiedenti).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Uso del Servizio Copia Shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ad0f07cc20da83f9401ff5194776300c5aad23a950b2fbc7f14f787fe22f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866251"
---
# <a name="using-the-volume-shadow-copy-service"></a>Uso del Servizio Copia Shadow del volume

Le operazioni di backup e ripristino vss usano ognuna un protocollo per l'interazione dei sistemi che usano l'archiviazione di massa (writer) e di quelli che ne esercitino il backup (richiedenti).

Entrambe le operazioni di backup e ripristino sono principalmente guidate dal richiedente, che controlla il comportamento del writer e del provider generando eventi COM a livello di sistema che il writer deve elaborare. Poiché i metodi di generazione di eventi sono asincroni, i writer hanno un controllo limitato sullo stato del richiedente tramite i gestori asincroni disponibili per VSS (vedere [**IVssAsync).**](/windows/desktop/api/Vss/nn-vss-ivssasync)

Questa interazione richiede strutture di dati di base che descrivono file e gruppi di file ([*componenti*](vssgloss-c.md)), nonché un modello di metadati per consentire l'archiviazione delle informazioni di backup e consentire la comunicazione tra writer e richiedente.

-   [Compatibilità delle applicazioni VSS](usage-conventions.md)
-   [Configurazione di VSS](configuring-vss.md)
-   [Metadati di VSS](vss-metadata.md)
-   [Uso della selezionabilità e dei percorsi logici](working-with-selectability-and-logical-paths.md)
-   [Panoramica dell'elaborazione di un backup in VSS](overview-of-processing-a-backup-under-vss.md)
-   [Panoramica dell'elaborazione di un ripristino in VSS](overview-of-processing-a-restore-under-vss.md)

 

 




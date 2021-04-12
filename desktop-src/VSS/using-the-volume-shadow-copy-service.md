---
description: Le operazioni di backup e ripristino VSS utilizzano ogni protocollo per l'interazione dei sistemi che utilizzano l'archiviazione di massa (writer) e quelli che eseguono il backup (richiedenti).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Uso della Servizio Copia Shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a1c81d79de30085f783feb02b7a7d47d5dc765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526304"
---
# <a name="using-the-volume-shadow-copy-service"></a>Uso della Servizio Copia Shadow del volume

Le operazioni di backup e ripristino VSS utilizzano ogni protocollo per l'interazione dei sistemi che utilizzano l'archiviazione di massa (writer) e quelli che eseguono il backup (richiedenti).

Le operazioni di backup e ripristino sono gestite principalmente dal richiedente, che controlla il comportamento del writer e del provider generando eventi COM a livello per l'elaborazione da parte del writer. Poiché i metodi per la generazione di eventi sono asincroni, i writer hanno un controllo limitato sullo stato del richiedente tramite i gestori asincroni disponibili per VSS (vedere [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).

Questa interazione richiede strutture di dati di base che descrivono file e gruppi di file ([*componenti*](vssgloss-c.md)), nonché un modello di metadati per consentire l'archiviazione delle informazioni di backup e consentire la comunicazione tra writer/richiedente.

-   [Compatibilità delle applicazioni VSS](usage-conventions.md)
-   [Configurazione di VSS](configuring-vss.md)
-   [Metadati VSS](vss-metadata.md)
-   [Uso della selezione e dei percorsi logici](working-with-selectability-and-logical-paths.md)
-   [Cenni preliminari sull'elaborazione di un backup in VSS](overview-of-processing-a-backup-under-vss.md)
-   [Panoramica dell'elaborazione di un ripristino in VSS](overview-of-processing-a-restore-under-vss.md)

 

 




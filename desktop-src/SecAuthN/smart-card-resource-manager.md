---
description: Gestione risorse smart card
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: Gestione risorse smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3ee8e0bf311539863502d3e789544717e6dff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316223"
---
# <a name="smart-card-resource-manager"></a>Gestione risorse smart card

Il [*gestore di risorse*](../secgloss/r-gly.md) della [*Smart Card*](../secgloss/s-gly.md) gestisce l'accesso ai [*lettori*](../secgloss/r-gly.md) e alle *Smart Card*. Per gestire queste risorse, vengono eseguite le funzioni seguenti.

-   Identifica e tiene traccia delle risorse.
-   Alloca Reader e risorse tra più applicazioni.
-   Supporta le primitive [*delle transazioni*](../secgloss/t-gly.md) per accedere ai servizi disponibili in una scheda specifica.
    > [!Note]  
    > Si tratta di un punto importante perché le schede correnti sono dispositivi a thread singolo che richiedono spesso l'esecuzione di più comandi per completare una singola funzione. [*Le transazioni*](../secgloss/t-gly.md) consentono l'esecuzione di più comandi senza interruzioni, assicurando che le informazioni [*sullo stato*](../secgloss/s-gly.md) intermedio non siano danneggiate.

     

È possibile accedere a Resource Manager direttamente tramite l'API di Resource Manager o indirettamente tramite qualsiasi [*provider di servizi*](../secgloss/s-gly.md)smart card.

L'API di Resource Manager è un set di funzioni di Windows che consentono l'accesso diretto ai servizi di Resource Manager. Per una panoramica delle funzioni di Windows fornite dall'API, vedere [Smart Card gestione risorse API](smart-card-resource-manager-api.md). In confronto, i provider di servizi Smart Card utilizzano le interfacce COM.

Molte delle funzioni di Windows nell'API di Resource Manager hanno equivalenti nelle proprietà e nei metodi delle interfacce COM dei provider di servizi Smart Card. Anche se la maggior parte degli sviluppatori di applicazioni troverà COM più semplice da usare, alcune applicazioni dovranno ancora usare le funzioni di Windows per eseguire determinate attività. Ad esempio, le applicazioni che devono modificare l'elenco di Reader o gruppi di lettori nel [*database delle smart card*](../secgloss/s-gly.md)e quelle che richiedono il controllo diretto di un lettore devono usare l'API di Resource Manager. I servizi che forniscono queste funzionalità sono disponibili solo nelle funzioni di Windows e non nel COM fornito dai provider di servizi.

Per informazioni sulle modalità di implementazione di [*Resource Manager*](../secgloss/r-gly.md) in Windows, vedere [Gestione risorse implementazione](resource-manager-implementation.md).

 

 

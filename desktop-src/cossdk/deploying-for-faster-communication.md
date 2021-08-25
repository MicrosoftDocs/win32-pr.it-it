---
description: Distribuzione per una comunicazione più veloce
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Distribuzione per una comunicazione più veloce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201185878a6d3fc041512b41fd3f51975ae5e0988f853dbbbcb77b716ea4cebe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070781"
---
# <a name="deploying-for-faster-communication"></a>Distribuzione per una comunicazione più veloce

Le prestazioni sono una considerazione fondamentale quando si distribuisce un'applicazione COM+ e la posizione dei componenti è la chiave per ottenere prestazioni ottimali da un'applicazione ben progettata.

Una volta era ampiamente noto che con le architetture di applicazioni scalabili, le prestazioni potevano essere migliorate semplicemente spostando i componenti primari dell'applicazione in hardware più veloce. Questo ha dimostrato di non essere vero. I problemi di prestazioni non derivano dalle prestazioni dei singoli componenti, ma dai collegamenti che connettono i componenti.

Il fattore principale per l'esito positivo è la posizione. Prossimità o posizione fisica, tempo, capacità e scopo sono aspetti distinti della posizione che si applicano alla distribuzione di un'applicazione COM+, che influiscono tutte sulle prestazioni.

Le prestazioni migliori si verificano quando i componenti e le risorse dell'applicazione vengono progettati e distribuiti in base alle esigenze poste dal carico di lavoro dell'applicazione.

In generale, è consigliabile distribuire i componenti per ridurre al minimo la comunicazione tra i componenti, in particolare tra computer. Se la progettazione dell'applicazione è efficiente, le classi all'interno di un componente vengono raggruppate in base all'uso e alla funzione per ottimizzare le comunicazioni all'interno dei componenti. Nella distribuzione dei componenti è necessario assicurarsi che i componenti si trovino logicamente per usare le relazioni tra i componenti e per ridurre la quantità di messaggistica tra i componenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione per la distribuzione](designing-for-deployment.md)
</dt> </dl>

 

 




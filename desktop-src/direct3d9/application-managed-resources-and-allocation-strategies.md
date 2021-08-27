---
description: Le risorse vertex-buffer o index-buffer gestite non possono essere dichiarate dinamiche specificando D3DUSAGE DYNAMIC al \_ momento della creazione.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Application-Managed risorse e strategie di allocazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86eabccde7fef025c952c869a30fdeff8cf5316ceb0316b513692175d8581a01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119431"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a>Application-Managed risorse e strategie di allocazione (Direct3D 9)

Le risorse vertex-buffer o index-buffer gestite non possono essere dichiarate dinamiche specificando D3DUSAGE DYNAMIC al \_ momento della creazione. Questa operazione richiederebbe una copia aggiuntiva per ogni modifica al contenuto del vertex buffer. I buffer dei vertici dinamici sono destinati al rendering della geometria dinamica e dei dati estratti da alberi partizionati dello spazio binario o da altre strutture di dati di visibilità. Questa operazione può essere eseguita pre-allocando i buffer del formato desiderato. Queste risorse vengono quindi selezionate per supportare le esigenze dell'applicazione da parte di un gestore di risorse all'interno dell'applicazione. Il numero totale di buffer dei vertici dinamici è ridotto perché un'applicazione userà contemporaneamente solo pochi stride di vertice diversi e perché è necessario un buffer dei vertici diverso solo per stride univoci. Quando si gestiscono le risorse dinamiche in questo modo, assicurarsi che le richieste ad alta frequenza sulle risorse non diminuiscono significativamente le prestazioni dell'applicazione.

Quando si usano risorse gestite da Direct3D e dalle applicazioni, allocare le risorse gestite dall'applicazione nella memoria D3DPOOL DEFAULT prima di creare \_ risorse gestite da Direct3D. Ciò consente al gestore della memoria di mantenere un conteggio accurato della memoria disponibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse Direct3D](direct3d-resources.md)
</dt> </dl>

 

 




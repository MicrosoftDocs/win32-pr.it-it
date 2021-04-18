---
description: Non è possibile dichiarare dinamicamente le risorse del buffer di vertex o del buffer gestito specificando \_ la dinamica D3DUSAGE al momento della creazione.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Risorse Application-Managed e strategie di allocazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f5ce23cac4bf46b8580a31d7c6d71fdc3de15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304551"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a>Risorse Application-Managed e strategie di allocazione (Direct3D 9)

Non è possibile dichiarare dinamicamente le risorse del buffer di vertex o del buffer gestito specificando \_ la dinamica D3DUSAGE al momento della creazione. Questa operazione richiede una copia aggiuntiva per ogni modifica apportata al contenuto del buffer dei vertici. I buffer dei vertici dinamici sono progettati per il rendering di geometria dinamica e dati estratti da alberi partizionati di spazio binario o altre strutture di dati di visibilità. Questa operazione può essere eseguita tramite la pre-allocazione dei buffer del formato desiderato. Queste risorse vengono quindi suddivise per supportare le esigenze dell'applicazione da parte di un gestore di risorse all'interno dell'applicazione. Il numero totale di buffer dei vertici dinamici è ridotto perché un'applicazione utilizzerà simultaneamente solo alcuni stride del vertice diversi e perché è necessario un buffer del vertice diverso solo per gli stride univoci. Quando si gestiscono le risorse dinamiche in questo modo, assicurarsi che le richieste con frequenza elevata sulle risorse non diminuiscano in modo significativo le prestazioni dell'applicazione.

Quando si usano risorse gestite da Direct3D e dalle applicazioni, allocare risorse gestite dall'applicazione nella \_ memoria predefinita di D3DPOOL prima di creare risorse gestite da Direct3D. Questo consente al gestore della memoria di mantenere un conteggio accurato della memoria disponibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse Direct3D](direct3d-resources.md)
</dt> </dl>

 

 




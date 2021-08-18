---
title: Ritaglio automatico
description: Ritaglio automatico
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dabc3fd7ece50250ee9e1fea89ff23dd23db533dfcc90d5a939ce1b563ce764
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551237"
---
# <a name="automatic-clipping"></a>Ritaglio automatico

È consigliabile che un contenitore di controlli ActiveX supporti il ritaglio automatico dei relativi controlli. Ciò comporta un funzionamento più efficiente per la maggior parte dei controlli. Se il ritaglio automatico è supportato, la proprietà di ambiente AutoClip deve essere supportata e avere il valore **TRUE.**

Il ritaglio automatico è la capacità di un contenitore di garantire che l'output disegnato di un controllo vada solo all'area di ritaglio corrente del contenitore. In un contenitore che supporta il ritaglio automatico, un controllo può disegnare indipendentemente dall'area di ritaglio, perché il contenitore ritaglierà automaticamente qualsiasi disegno che si verifica all'esterno dell'area del controllo. Se un contenitore non supporta il ritaglio automatico, i controlli generati da CDK creeranno una finestra padre aggiuntiva se viene passata un'area di ritaglio non Null.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

 





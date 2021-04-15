---
title: Ritaglio automatico
description: Ritaglio automatico
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331271"
---
# <a name="automatic-clipping"></a>Ritaglio automatico

Si consiglia vivamente che un contenitore di controlli ActiveX supporti il ritaglio automatico dei controlli. Questa operazione comporterà una maggiore efficienza per la maggior parte dei controlli. Se il ritaglio automatico è supportato, la proprietà di ambiente AutoClip deve essere supportata e avere un valore **true**.

Il ritaglio automatico è la capacità di un contenitore di garantire che l'output disegnato di un controllo venga inserito solo nell'area di visualizzazione corrente del contenitore. In un contenitore che supporta il ritaglio automatico, un controllo può disegnare senza considerare l'area di ritaglio, perché il contenitore ridurrà automaticamente qualsiasi disegno che si verifica all'esterno dell'area del controllo. Se un contenitore non supporta il ritaglio automatico, i controlli generati da CDK creerà una finestra padre aggiuntiva se viene passata un'area di ridimensionamento non null.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

 





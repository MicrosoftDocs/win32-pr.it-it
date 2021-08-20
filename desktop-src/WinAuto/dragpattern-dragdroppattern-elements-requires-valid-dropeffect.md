---
title: Gli elementi DragPattern/DragDropPattern richiedono un oggetto DropEffect valido
description: Gli elementi DragPattern/DragDropPattern richiedono un oggetto DropEffect valido
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd95e1da2d3d05c7499f72c86d454da2832947cafd0150e8f62b2f3e8d56af2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115679"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a>Gli elementi DragPattern/DragDropPattern richiedono un oggetto DropEffect valido

## <a name="text"></a>Testo

Gli elementi che supportano il trascinamento della selezione devono avere un set 'DropEffect' valido

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

L'elemento supporta [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) o [**IUIAutomationDropTargetPattern,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern)ma non dispone di una proprietà [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) valida impostata.

Questo problema causa problemi per gli utenti che si basano su un'utilità per la lettura dello schermo. L'utente non sarà in grado di indicare l'effetto di questo oggetto durante il trascinamento.

## <a name="possible-causes"></a>Possibili cause

-   L'elemento o il relativo elemento padre non ha creato [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) o [**DropEffects come**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) nome o etichetta assegnati in modo non corretto.
-   Uno sviluppatore non è a conoscenza del fatto che le utilità per la lettura dello schermo leggono DropEffect.

 

 





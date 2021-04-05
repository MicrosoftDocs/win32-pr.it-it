---
title: Gli elementi DragPattern/DragDropPattern richiedono un DropEffect valido
description: Gli elementi DragPattern/DragDropPattern richiedono un DropEffect valido
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33acda19732e2ebd96182023fce9641012b50d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707165"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a>Gli elementi DragPattern/DragDropPattern richiedono un DropEffect valido

## <a name="text"></a>Testo

Gli elementi che supportano il trascinamento della selezione devono avere un set ' DropEffect ' valido

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

L'elemento supporta [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) o [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), ma non ha un set di proprietà [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) valido.

Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate. L'utente non sarà in grado di stabilire l'effetto di questo oggetto durante il trascinamento.

## <a name="possible-causes"></a>Possibili cause

-   L'elemento, o il relativo padre, non ha creato [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) o [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) un'etichetta o un nome assegnato erroneamente.
-   Uno sviluppatore non è A conoscenza del DropEffect di lettura dello schermo.

 

 





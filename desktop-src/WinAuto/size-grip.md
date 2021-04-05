---
title: Grip dimensioni (riferimento all'elemento MSAA UI)
description: Il grip dimensioni è uno speciale puntatore del mouse nell'angolo inferiore destro di una finestra che consente a un utente di fare clic e trascinare il riquadro dimensioni per ridimensionare la finestra.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb7180a8936aff46903257e6be8ca4ab7f0e5b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714134"
---
# <a name="size-grip-msaa-ui-element-reference"></a>Grip dimensioni (riferimento all'elemento MSAA UI)

Il grip dimensioni è uno speciale puntatore del mouse nell'angolo inferiore destro di una finestra che consente a un utente di fare clic e trascinare il riquadro dimensioni per ridimensionare la finestra.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Il grip dimensioni supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Il grip dimensioni supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                   | Commenti                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | La proprietà **Description** è "può essere usata per ridimensionare la larghezza e l'altezza di una finestra".                                                                                   |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | La proprietà **Name** è "size box".                                                                                                                                   |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | Finestra che contiene il riquadro delle dimensioni.                                                                                                                                |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | La proprietà **Role** è [**il \_ \_ grip del sistema Role**](object-roles.md).                                                                                  |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | Il valore della proprietà **state** è zero, che indica che l'oggetto è visibile oppure che il [**sistema di stato è \_ \_ invisibile**](object-state-constants.md). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





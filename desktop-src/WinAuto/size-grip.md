---
title: Ridimensionare il controllo (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)
description: Il riquadro dimensioni è uno speciale puntatore del mouse nell'angolo inferiore destro di una finestra che consente all'utente di fare clic e trascinare il riquadro dimensioni per ridimensionare la finestra.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7315425720ddee8beaf0f7c1f1b2ecbd8ba0fada51e64dc70453f3bb477e1f6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795645"
---
# <a name="size-grip-msaa-ui-element-reference"></a>Ridimensionare il controllo (informazioni di riferimento per gli elementi dell'interfaccia utente MSAA)

Il riquadro dimensioni è uno speciale puntatore del mouse nell'angolo inferiore destro di una finestra che consente all'utente di fare clic e trascinare il riquadro dimensioni per ridimensionare la finestra.

## <a name="iaccessible-methods"></a>Metodi IAccessible

Il controllo dimensioni supporta i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Proprietà IAccessible

Il riquadro dimensioni supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:



| Proprietà                                                                   | Commenti                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | La **proprietà Description** è "Può essere usata per ridimensionare la larghezza e l'altezza di una finestra".                                                                                   |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | La **proprietà Name** è "Size box".                                                                                                                                   |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | Finestra che contiene il controllo delle dimensioni.                                                                                                                                |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | La **proprietà Role** è ROLE SYSTEM [**\_ \_ GRIP.**](object-roles.md)                                                                                  |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | Il valore della proprietà **State** è zero, ovvero l'oggetto è visibile o [**STATE SYSTEM \_ \_ INVISIBLE.**](object-state-constants.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Iaccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





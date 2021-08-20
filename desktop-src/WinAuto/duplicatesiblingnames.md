---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d18f0e04ed0b2aba3b0637ca8535e2ca5a18110ee29edb397fc250944035f895
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115331"
---
# <a name="duplicatesiblingnames"></a>DuplicateSiblingNames

## <a name="text"></a>Testo

Il nome e il ruolo di pari livello \\ {0} \\ duplicati " " causeranno ambiguità tra gli elementi.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento ha lo stesso Name e Role/ControlType di un altro elemento.

Questo problema può causare confusione perché le utilità per la lettura dello schermo leggeranno lo stesso testo per tutti gli elementi con lo stesso Nome e Ruolo/ControlType.

## <a name="possible-causes"></a>Possibili cause

-   Il nome dell'elemento contiene il testo Role/ControlType.
-   Il nome dell'elemento o il nome dell'elemento padre non è impostato o non è impostato correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Proprietà Name](name-property.md)
</dt> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 





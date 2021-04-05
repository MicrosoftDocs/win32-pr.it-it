---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed5a7caeadc34519988fe8a4a1f12ec4e05ce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714512"
---
# <a name="duplicatesiblingnames"></a>DuplicateSiblingNames

## <a name="text"></a>Testo

Il nome di pari livello e il ruolo \\ "" duplicati {0} \\ provocheranno ambiguità tra gli elementi.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento ha lo stesso nome e lo stesso ruolo/ControlType di un altro elemento.

Questo problema può causare confusione perché le utilità per la lettura dello schermo leggono lo stesso testo per tutti gli elementi con lo stesso nome e lo stesso ruolo/ControlType.

## <a name="possible-causes"></a>Possibili cause

-   Il nome dell'elemento contiene il testo Role/ControlType.
-   Il nome dell'elemento o il nome dell'elemento padre non è impostato o è impostato in modo errato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Proprietà Name](name-property.md)
</dt> <dt>

[**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement. currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 





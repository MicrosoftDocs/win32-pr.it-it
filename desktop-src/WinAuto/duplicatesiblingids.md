---
title: DuplicateSiblingIDs
description: DuplicateSiblingIDs
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ba2ccca45234bb49fc782c5522b4e446d77a2c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298965"
---
# <a name="duplicatesiblingids"></a>DuplicateSiblingIDs

## <a name="text"></a>Testo

L'ID di automazione duplicato \\ "" provocherà {0} \\ ambiguità tra gli elementi.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento ha lo stesso ID di automazione di un altro elemento.

Questo problema può causare problemi di automazione che impediscono al codice di test di fare riferimento all'elemento corretto.

## <a name="possible-causes"></a>Possibili cause

-   Gli elementi di pari livello hanno lo stesso ID di automazione.
-   Implementazione non corretta della proprietà AutomationId di UIA.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentAutomationId**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentautomationid)
</dt> </dl>

 

 





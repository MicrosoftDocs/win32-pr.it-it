---
title: DuplicateSiblingIDs
description: DuplicateSiblingIDs
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd9bb311d4aafdf1f509d3404cfe057f96f6bf378b822f6f77cab4943cea097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115358"
---
# <a name="duplicatesiblingids"></a>DuplicateSiblingIDs

## <a name="text"></a>Testo

L'ID di \\ automazione {0} \\ duplicato " " causerà ambiguità tra gli elementi.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Un elemento ha lo stesso ID di automazione di un altro elemento.

Questo problema può causare problemi di automazione che impediscono al codice di test di fare riferimento all'elemento corretto.

## <a name="possible-causes"></a>Possibili cause

-   Gli elementi di pari livello hanno lo stesso ID di automazione.
-   Implementazione non corretta della proprietà AutomationId dell'interfaccia utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentAutomationId**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentautomationid)
</dt> </dl>

 

 





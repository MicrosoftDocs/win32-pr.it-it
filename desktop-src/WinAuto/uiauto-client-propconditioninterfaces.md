---
title: Interfacce delle condizioni di proprietà per i client
description: Questa sezione descrive le interfacce delle condizioni delle proprietà per Automazione interfaccia utente client per le applicazioni Microsoft Win32.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447c2bf9a67a5fc9cbd303e86599502e2b6154f53485af5a57bf13a6268fa930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133484"
---
# <a name="property-condition-interfaces-for-clients"></a>Interfacce delle condizioni di proprietà per i client

Questa sezione descrive le interfacce delle condizioni delle proprietà per Automazione interfaccia utente client per le applicazioni Microsoft Win32.

## <a name="in-this-section"></a>Contenuto della sezione



| Interfaccia                                                                                  | Descrizione                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationAndCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | Espone proprietà e metodi che Microsoft Automazione interfaccia utente applicazioni client possono usare per recuperare informazioni su una condizione di proprietà basata su AND. <br/> |
| [**IUIAutomationBoolCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | Rappresenta una condizione che può essere **TRUE** (seleziona tutti gli elementi) o **FALSE** (non seleziona alcun elemento).<br/>                                           |
| [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | Questa è l'interfaccia principale per le condizioni usate nel filtro durante la ricerca di elementi nell'Automazione interfaccia utente albero.<br/>                                   |
| [**IUIAutomationNotCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | Rappresenta una condizione che è il negativo di un'altra condizione.<br/>                                                                                       |
| [**IUIAutomationOrCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | Rappresenta una condizione che è costituito da più condizioni, almeno una delle quali deve essere true.<br/>                                                              |
| [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | Rappresenta una condizione basata su un valore della proprietà utilizzato per trovare Automazione interfaccia utente elementi.<br/>                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Automazione interfaccia utente client](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 


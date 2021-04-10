---
title: Interfacce di condizione delle proprietà per i client
description: Questa sezione descrive le interfacce della condizione di proprietà per i client di automazione interfaccia utente per le applicazioni Microsoft Win32.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f840706d4f9e340cae86813a4992400791dccd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046833"
---
# <a name="property-condition-interfaces-for-clients"></a>Interfacce di condizione delle proprietà per i client

Questa sezione descrive le interfacce della condizione di proprietà per i client di automazione interfaccia utente per le applicazioni Microsoft Win32.

## <a name="in-this-section"></a>Contenuto della sezione



| Interfaccia                                                                                  | Descrizione                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationAndCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | Espone proprietà e metodi che possono essere usati dalle applicazioni client di automazione interfaccia utente Microsoft per recuperare informazioni su una condizione di proprietà basata su e. <br/> |
| [**IUIAutomationBoolCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | Rappresenta una condizione che può essere **true** (Seleziona tutti gli elementi) o **false** (non seleziona elementi).<br/>                                           |
| [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | Si tratta dell'interfaccia principale per le condizioni utilizzate nel filtro durante la ricerca di elementi nell'albero di automazione interfaccia utente.<br/>                                   |
| [**IUIAutomationNotCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | Rappresenta una condizione negativa di un'altra condizione.<br/>                                                                                       |
| [**IUIAutomationOrCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | Rappresenta una condizione costituita da più condizioni, almeno una delle quali deve essere true.<br/>                                                              |
| [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | Rappresenta una condizione basata su un valore della proprietà usato per trovare gli elementi di automazione interfaccia utente.<br/>                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client di automazione interfaccia utente](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 


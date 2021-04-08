---
title: Interfacce Factory proxy per i client
description: Questa sezione descrive le interfacce di Factory proxy per le applicazioni client di automazione interfaccia utente non gestite.
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc1827ab36a221dcd7f27e5b2a05de91931b0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045210"
---
# <a name="proxy-factory-interfaces-for-clients"></a>Interfacce Factory proxy per i client

Questa sezione descrive le interfacce di Factory proxy per le applicazioni client di automazione interfaccia utente non gestite.

## <a name="in-this-section"></a>Contenuto della sezione



| Interfaccia                                                                                      | Descrizione                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | Espone le proprietà e i metodi di un oggetto che crea un provider di automazione interfaccia utente Microsoft per gli elementi dell'interfaccia utente che non dispongono del supporto nativo per l'automazione interfaccia utente. Questa interfaccia viene implementata dai proxy.<br/>                                                                          |
| [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | Rappresenta una factory proxy nella tabella gestita dall'automazione interfaccia utente ed espone proprietà e metodi che possono essere utilizzati dalle applicazioni client per interagire con gli oggetti [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) .<br/>                                   |
| [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | Espone proprietà e metodi per una tabella di Factory proxy. Ogni voce di tabella è rappresentata da un'interfaccia [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) . Le voci si trovano nell'ordine in cui il sistema tenterà di utilizzare i proxy.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client di automazione interfaccia utente](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 






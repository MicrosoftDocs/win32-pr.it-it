---
title: Interfacce factory proxy per i client
description: In questa sezione vengono descritte le interfacce della factory proxy per le applicazioni client Automazione interfaccia utente non gestite.
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e92264691c35cefe3ffaf246d2e73bac5ea7dc3363a4f220eb0ddecb9f15030
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614360"
---
# <a name="proxy-factory-interfaces-for-clients"></a>Interfacce factory proxy per i client

In questa sezione vengono descritte le interfacce della factory proxy per le applicazioni client Automazione interfaccia utente non gestite.

## <a name="in-this-section"></a>Contenuto della sezione



| Interfaccia                                                                                      | Descrizione                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | Espone proprietà e metodi di un oggetto che crea un provider microsoft Automazione interfaccia utente per gli elementi dell'interfaccia utente che non dispongono del supporto nativo per Automazione interfaccia utente. Questa interfaccia viene implementata dai proxy.<br/>                                                                          |
| [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | Rappresenta una factory proxy nella tabella gestita da Automazione interfaccia utente ed espone proprietà e metodi che possono essere usati dalle applicazioni client per interagire con gli [**oggetti IUIAutomationProxyFactory.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>                                   |
| [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | Espone proprietà e metodi per una tabella di proxy factory. Ogni voce di tabella è rappresentata da [**un'interfaccia IUIAutomationProxyFactoryEntry.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) Le voci sono nell'ordine in cui il sistema tenterà di usare i proxy.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Automazione interfaccia utente client](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 






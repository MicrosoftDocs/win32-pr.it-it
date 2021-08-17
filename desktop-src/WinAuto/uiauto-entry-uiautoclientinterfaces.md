---
title: Automazione interfaccia utente interfacce degli elementi per i client
description: Questa sezione descrive le interfacce usate da Microsoft Automazione interfaccia utente client per individuare, accedere ed eseguire query Automazione interfaccia utente elementi.
ms.assetid: dd7cdcf1-3511-424f-b729-b71a7e11cdd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356bd61a3f4a4626c8cc382c924b62967c01ddb201b8411eaa5451c822ede38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133414"
---
# <a name="ui-automation-element-interfaces-for-clients"></a>Automazione interfaccia utente interfacce degli elementi per i client

Questa sezione descrive le interfacce usate da Microsoft Automazione interfaccia utente client per individuare, accedere ed eseguire query Automazione interfaccia utente elementi.

## <a name="in-this-section"></a>Contenuto della sezione



| Interfaccia                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)<br/>                         | Espone metodi che consentono alle Automazione interfaccia utente client di individuare, accedere e filtrare Automazione interfaccia utente elementi. Automazione interfaccia utente espone ogni elemento del Automazione interfaccia utente come oggetto rappresentato [**dall'interfaccia IUIAutomation.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) I membri di questa interfaccia non sono specifici di un particolare elemento.<br/> |
| [**IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2)<br/>                       | Estende [**l'interfaccia IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) per esporre metodi aggiuntivi per il controllo Automazione interfaccia utente funzionalità.<br/>                                                                                                                                                                                                   |
| [**IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3)<br/>                       | Estende [**l'interfaccia IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2) per esporre metodi aggiuntivi per il controllo Automazione interfaccia utente funzionalità.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4)<br/>                       | Estende [**l'interfaccia IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3) per esporre metodi aggiuntivi per il controllo Automazione interfaccia utente funzionalità.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5)<br/>                       | Estende [**l'interfaccia IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4) per esporre metodi aggiuntivi per il controllo Automazione interfaccia utente funzionalità.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation6)<br/>                       | Estende [**l'interfaccia IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5) per esporre metodi aggiuntivi per il controllo Automazione interfaccia utente funzionalità.<br/>                                                                                                                                                                                                 |
| [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest)<br/> | Espone le proprietà e i metodi di una richiesta di cache. Le applicazioni client usano questa interfaccia per specificare le proprietà e i pattern di controllo da memorizzare nella cache quando Automazione interfaccia utente viene ottenuto un elemento .<br/>                                                                                                                                                 |
| [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)<br/>           | Espone metodi e proprietà per un elemento Automazione interfaccia utente, che rappresenta un elemento dell'interfaccia utente. <br/>                                                                                                                                                                                                                                                        |
| [**IUIAutomationElement2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2)<br/>         | Estende [**l'interfaccia IUIAutomationElement.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) <br/>                                                                                                                                                                                                                                                             |
| [**IUIAutomationElement3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3)<br/>         | Estende [**l'interfaccia IUIAutomationElement2.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2) <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4)<br/>         | Estende [**l'interfaccia IUIAutomationElement3.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3) <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5)<br/>         | Estende [**l'interfaccia IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) per fornire l'accesso ai dati dei punti di riferimento correnti e memorizzati nella cache.<br/>                                                                                                                                                                                                      |
| [**IUIAutomationElement6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6)<br/>         | Estende [**l'interfaccia IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5) per fornire l'accesso alle descrizioni complete correnti e memorizzate nella cache.<br/>                                                                                                                                                                                                  |
| [**IUIAutomationElement7**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7)<br/>         | Estende [**l'interfaccia IUIAutomationElement6.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6)<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement8**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8)<br/>         | Estende [**l'interfaccia IUIAutomationElement7.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7)<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement9**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/>         | Estende [**l'interfaccia IUIAutomationElement8.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8)<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray)<br/> | Rappresenta una raccolta di Automazione interfaccia utente personalizzati.<br/>                                                                                                                                                                                                                                                                                              |
| [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar)<br/>       | Espone metodi per la registrazione di nuovi pattern di controllo, proprietà ed eventi.<br/>                                                                                                                                                                                                                                                                   |
| [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)<br/>     | Espone proprietà e metodi che Automazione interfaccia utente applicazioni client usano per visualizzare ed esplorare Automazione interfaccia utente elementi sul desktop. <br/>                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Automazione interfaccia utente client](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 






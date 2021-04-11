---
title: Pattern di controllo CustomNavigation
description: Vengono descritte le linee guida e le convenzioni per l'implementazione dell'interfaccia ICustomNavigationProvider, incluse informazioni su proprietà e metodi.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221377"
---
# <a name="customnavigation-control-pattern"></a>Pattern di controllo CustomNavigation

Vengono descritte le linee guida e le convenzioni per l'implementazione dell'interfaccia **ICustomNavigationProvider** , incluse informazioni su proprietà e metodi. Il pattern di controllo **CustomNavigation** viene usato per abilitare la navigazione personalizzata tra i controlli in strutture di tipo gerarchia, ad esempio voci di elenco, elenchi puntati, elenchi numerati e intestazioni. Questo consente ai provider di descrivere le strutture o definire le relazioni navigabili usando solo l'elemento e non solo il controllo contenitore.

Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ICustomNavigationProvider**](#required-members-for-icustomnavigationprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il provider **CustomNavigation** , tenere presenti le linee guida e le convenzioni seguenti:

-   I valori delle proprietà per **PositionInSet**, **SizeOfSet** e **Level** sono valori integer in base uno.
-   **ICustomNavigationProvider** non fornisce la manipolazione attiva del controllo, ad esempio lo sviluppo di posizioni, l'aggiunta e la rimozione di elementi o la promozione e il abbassamento dei livelli.
-   I controlli che implementano **ICustomNavigationProvider** in genere hanno una struttura gerarchica, ma possono ignorare i livelli usando il metodo **Navigate** . Le proprietà **PositionInSet**, **SizeOfSet** e **Level** sono necessarie per il modello.

## <a name="required-members-for-icustomnavigationprovider"></a>Membri obbligatori per **ICustomNavigationProvider**

Le proprietà seguenti sono necessarie per l'implementazione dell'interfaccia **ICustomNavigationProvider** .



| Membri obbligatori                                                                  | Tipo di membro | Note                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [**CachedLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | Proprietà    | Si trova nell'interfaccia [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CachedPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | Proprietà    | Si trova nell'interfaccia [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CachedSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | Proprietà    | Si trova nell'interfaccia [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CurrentLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | Proprietà    | Si trova nell'interfaccia [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CurrentPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | Proprietà    | Si trova nell'interfaccia [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CurrentSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | Proprietà    | Si trova nell'interfaccia [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**Navigare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | Metodo      | nessuno                                                                                |



 

Questo pattern di controllo non è associato a metodi o eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[ListItem (controllo)](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[Controllo HeaderItem](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[DataItem (controllo)](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 





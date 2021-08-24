---
title: Pattern di controllo CustomNavigation
description: Vengono descritte le linee guida e le convenzioni per l'implementazione dell'interfaccia ICustomNavigationProvider, incluse informazioni su proprietà e metodi.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4499f5b031b5b5a9391f0c0078cb64c4c2715b61052c324cc2c2b19ccb2f5d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899557"
---
# <a name="customnavigation-control-pattern"></a>Pattern di controllo CustomNavigation

Vengono descritte le linee guida e le convenzioni per l'implementazione **dell'interfaccia ICustomNavigationProvider,** incluse informazioni su proprietà e metodi. Il **pattern di controllo CustomNavigation** viene usato per abilitare lo spostamento personalizzato tra controlli in strutture simili a gerarchia, ad esempio elementi elenco, elenchi puntati, elenchi numerati e intestazioni. In questo modo i provider possono descrivere le strutture o definire le relazioni esplorabili usando solo l'elemento e non solo il controllo contenitore.

Per esempi di controlli che implementano questo pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **ICustomNavigationProvider**](#required-members-for-icustomnavigationprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il provider **CustomNavigation,** tenere presente le linee guida e le convenzioni seguenti:

-   I valori **delle proprietà positionInSet,** **SizeOfSet** e **Level** sono valori integer in base uno.
-   **ICustomNavigationProvider** non fornisce la manipolazione attiva del controllo, ad esempio lo spostamento di posizioni, l'aggiunta e la rimozione di elementi o l'innalzamento di livello e l'abbassamento di livello dei livelli.
-   I controlli che **implementano ICustomNavigationProvider** hanno in genere una struttura gerarchica, ma possono ignorare i livelli usando il **metodo Navigate.** Le proprietà **PositionInSet,** **SizeOfSet** e **Level** sono obbligatorie nel modello.

## <a name="required-members-for-icustomnavigationprovider"></a>Membri obbligatori per **ICustomNavigationProvider**

Per l'implementazione **dell'interfaccia ICustomNavigationProvider** sono necessarie le proprietà seguenti.



| Membri obbligatori                                                                  | Tipo di membro | Note                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [**CachedLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | Proprietà    | Si trova [**nell'interfaccia IUIAutomationElement4.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CachedPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | Proprietà    | Si trova [**nell'interfaccia IUIAutomationElement4.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CachedSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | Proprietà    | Si trova [**nell'interfaccia IUIAutomationElement4.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CurrentLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | Proprietà    | Si trova [**nell'interfaccia IUIAutomationElement4.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CurrentPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | Proprietà    | Si trova [**nell'interfaccia IUIAutomationElement4.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**CurrentSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | Proprietà    | Si trova [**nell'interfaccia IUIAutomationElement4.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) |
| [**Navigare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | Metodo      | Nessuno                                                                                |



 

Questo pattern di controllo non è associato a metodi o eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e relativi pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Controllo ListItem](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[Controllo HeaderItem](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[Controllo DataItem](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 





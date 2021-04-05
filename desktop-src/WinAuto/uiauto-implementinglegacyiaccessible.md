---
title: Pattern di controllo LegacyIAccessible
description: Vengono descritte le linee guida e le convenzioni per l'utilizzo di ILegacyIAccessibleProvider, incluse informazioni su proprietà, metodi ed eventi.
ms.assetid: 4d66b9b8-ddbe-4bbc-b475-72dad1fe9393
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo LegacyIAccessible
- Automazione interfaccia utente, pattern di controllo LegacyIAccessible
- Automazione interfaccia utente, ILegacyIAccessibleProvider
- ILegacyIAccessibleProvider
- implementazione di pattern di controllo LegacyIAccessible di automazione interfaccia utente
- Pattern di controllo LegacyIAccessible
- pattern di controllo, ILegacyIAccessibleProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente LegacyIAccessible
- pattern di controllo, LegacyIAccessible
- interfacce, ILegacyIAccessibleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cffbd205b072f6f900ea5b5eb5a9f6ddfb5ddc5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712175"
---
# <a name="legacyiaccessible-control-pattern"></a>Pattern di controllo LegacyIAccessible

Vengono descritte le linee guida e le convenzioni per l'utilizzo di [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider), incluse informazioni su proprietà, metodi ed eventi. Il pattern di controllo **LegacyIAccessible** è supportato da Microsoft Active Accessibility al proxy di automazione interfaccia utente Microsoft.

I provider di applicazioni e controlli non implementano mai l'interfaccia [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider) .

Il pattern di controllo **LegacyIAccessible** espone l'interfaccia [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) ai client di automazione interfaccia utente, consentendo loro di accedere all'implementazione [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sottostante per determinati elementi dell'interfaccia utente. Tuttavia, **IUIAutomationLegacyIAccessiblePattern** non supporta metodi obsoleti o ridondanti con le funzionalità di automazione interfaccia utente.

In questo argomento sono incluse le sezioni seguenti:

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri del pattern di controllo **LegacyIAccessible**](#members-of-the-legacyiaccessible-control-pattern)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Nessuna applicazione o controllo implementa [**ILegacyIAccessibleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider). Il Framework di automazione interfaccia utente fornisce automaticamente l'implementazione del provider per un server Microsoft Active Accessibility nativo.

Il pattern di controllo **LegacyIAccessible** non è disponibile per i controlli basati sull'automazione dell'interfaccia utente.

## <a name="members-of-the-legacyiaccessible-control-pattern"></a>Membri del pattern di controllo **LegacyIAccessible**

Le proprietà, i metodi e gli eventi seguenti sono membri del pattern di controllo **LegacyIAccessible** . Le note sono relative ai client di automazione interfaccia utente.



| Membri                                                                        | Tipo di membro | Note                                                                                                                                |
|--------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**ChildId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_childid)                   | Proprietà    | Restituisce **CHILDID \_ self** (0) per un oggetto non figlio.                                                                                |
| [**DefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_defaultaction)       | Proprietà    | nessuno                                                                                                                                 |
| [**Descrizione**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_description)           | Proprietà    | nessuno                                                                                                                                 |
| [**Guida**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_help)                         | Proprietà    | nessuno                                                                                                                                 |
| [**KeyboardShortcut**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_keyboardshortcut) | Proprietà    | nessuno                                                                                                                                 |
| [**Nome**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_name)                         | Proprietà    | nessuno                                                                                                                                 |
| [**Role**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_role)                         | Proprietà    | Utilizzare la funzione [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) per recuperare la stringa localizzata.                                                    |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getselection)         | Metodo      | Recupera un puntatore all'interfaccia [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) .                                |
| [**Stato**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_state)                       | Proprietà    | Utilizzare la funzione [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) per recuperare la stringa localizzata.                                                  |
| [**Valore**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_value)                       | Proprietà    | nessuno                                                                                                                                 |
| [**DoDefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-dodefaultaction)   | Metodo      | nessuno                                                                                                                                 |
| [**GetIAccessible**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getiaccessible)     | Metodo      | nessuno                                                                                                                                 |
| [**Selezionare**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-select)                     | Metodo      | Il flag di selezione è un valore di Microsoft Active Accessibility **SELFLAG** . Per altre informazioni, vedere [costanti SELFLAG](selflag.md). |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-setvalue)                 | Metodo      | nessuno                                                                                                                                 |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 





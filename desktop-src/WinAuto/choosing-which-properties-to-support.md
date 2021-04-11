---
title: Scelta delle proprietà da supportare
description: Le proprietà IAccessible forniscono agli sviluppatori di server un modo per descrivere un'ampia gamma di elementi dell'interfaccia utente.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c88a808889403f88d414f7ad950b3e431c00e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330919"
---
# <a name="choosing-which-properties-to-support"></a>Scelta delle proprietà da supportare

Le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) forniscono agli sviluppatori di server un modo per descrivere un'ampia gamma di elementi dell'interfaccia utente. Tuttavia, non tutte le proprietà sono applicabili per ogni tipo di elemento dell'interfaccia utente. Alcune proprietà, inoltre, forniscono informazioni descrittive utili ma non essenziali.

Per ogni oggetto è necessario che i server supportino le proprietà e i metodi seguenti:

-   [**Nome**](name-property.md)
-   [**Role**](role-property.md)
-   [**State**](state-property.md)
-   [**Percorso**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) e [ **IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) e [ **IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

Le proprietà e il metodo seguenti devono essere supportati se sono applicabili all'oggetto:

-   [**KeyboardShortcut**](keyboardshortcut-property.md)
-   [**Valore**](value-property.md)

Se l'oggetto dispone di elementi figlio, è necessario che le proprietà e il metodo seguenti siano supportati:

-   [**Figlio**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) e [ **childCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**Focus, Selection**](selection-and-focus-properties-and-methods.md)e [ **IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

Le proprietà seguenti sono facoltative, ma forniscono utili informazioni descrittive sull'oggetto. La proprietà [**Description**](description-property.md) viene implementata per descrivere le bitmap e altre immagini.

-   [**Descrizione**](description-property.md)
-   [**DefaultAction**](defaultaction-property.md) e [ **IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**Help**](help-property.md)
-   [**HelpTopic**](helptopic-property.md)

 

 





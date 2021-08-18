---
title: Scelta delle proprietà da supportare
description: Le proprietà IAccessible consentono agli sviluppatori di server di descrivere un'ampia gamma di elementi dell'interfaccia utente.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a3c9ef5d56c6d963a05ac84b5e2cacafde488c377ebcc73fa1e2c4be1adab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133964"
---
# <a name="choosing-which-properties-to-support"></a>Scelta delle proprietà da supportare

Le [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) consentono agli sviluppatori di server di descrivere un'ampia gamma di elementi dell'interfaccia utente. Ma non tutte le proprietà sono applicabili per ogni tipo di elemento dell'interfaccia utente. Inoltre, alcune proprietà forniscono informazioni descrittive utili ma non essenziali.

I server devono supportare le proprietà e i metodi seguenti per ogni oggetto:

-   [**Nome**](name-property.md)
-   [**Role**](role-property.md)
-   [**Stato**](state-property.md)
-   [**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) e [ **IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Padre**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) e [ **IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

Le proprietà e il metodo seguenti devono essere supportati se sono applicabili all'oggetto :

-   [**KeyboardShortcut**](keyboardshortcut-property.md)
-   [**Valore**](value-property.md)

Le proprietà e il metodo seguenti devono essere supportati se l'oggetto dispone di elementi figlio:

-   [**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) e [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**Stato attivo, Selezione**](selection-and-focus-properties-and-methods.md)e [ **IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

Le proprietà seguenti sono facoltative, ma forniscono informazioni descrittive utili sull'oggetto . La [**proprietà Description**](description-property.md) viene implementata per descrivere bitmap e altre immagini.

-   [**Descrizione**](description-property.md)
-   [**DefaultAction**](defaultaction-property.md) e [ **IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**Help**](help-property.md)
-   [**HelpTopic**](helptopic-property.md)

 

 





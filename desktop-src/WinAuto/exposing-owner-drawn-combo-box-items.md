---
title: Esposizione di Owner-Drawn elementi della casella combinata
description: Gli sviluppatori di applicazioni non devono implementare IAccessible per esporre gli elementi in una casella combinata creata dal proprietario con lo stile CBS \_ HASSTRINGS perché Microsoft Active Accessibility espone gli elementi nelle caselle combinate con questo stile.
ms.assetid: 9ff14b2f-ae09-4839-b281-fba46addaf5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364dccaf21927e2d0092fc744d501f47830c6eeb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300244"
---
# <a name="exposing-owner-drawn-combo-box-items"></a>Esposizione di Owner-Drawn elementi della casella combinata

Gli sviluppatori di applicazioni non devono implementare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per esporre gli elementi in una casella combinata creata dal proprietario con lo stile **CBS \_ HASSTRINGS** perché Microsoft Active Accessibility espone gli elementi nelle caselle combinate con questo stile. Gli elementi in una casella combinata creata dal proprietario con lo stile **CBS \_ HASSTRINGS** vengono visualizzati come testo. Questo stile viene tuttavia utilizzato anche con le caselle combinate create dal proprietario che non visualizzano testo, in modo che gli elementi della casella combinata siano esposti da Microsoft Active Accessibility.

Per consentire a Microsoft Active Accessibility di esporre gli elementi in una casella combinata creata dal proprietario che non Visualizza il testo:

-   Usare lo stile **CBS \_ HASSTRINGS** durante la creazione della casella combinata.
-   Creare una controparte testuale che denomina o descriva ogni elemento nella casella combinata.
-   Quando si aggiungono elementi alla casella combinata creata dal proprietario, usare il \_ messaggio CB ADDSTRING per aggiungere il testo che si vuole esporre a Microsoft Active Accessibility. Questo testo non viene visualizzato, quindi non deve far parte dei dati creati dal proprietario. Aggiungere i dati degli elementi creati dal proprietario usando il \_ messaggio CB SETITEMDATA.

Quando si usa il metodo precedente, tenere presente quanto segue:

-   Se si usa lo stile di **\_ ordinamento CBS** , la casella combinata viene ordinata con le stringhe fornite e non con la procedura di callback [WM \_ COMPAREITEM](../controls/wm-compareitem.md) .
-   Con le caselle combinate delle variabili create dal proprietario create con lo stile **CBS \_ OwnerDrawVariable**, usare una variabile globale o un altro meccanismo per tenere traccia del momento in cui il membro **ItemData** di [MEASUREITEMSTRUCT](/windows/win32/api/winuser/ns-winuser-measureitemstruct) è valido. La variabile globale è obbligatoria perché il sistema invia il messaggio [WM \_ MeasureItem](../controls/wm-measureitem.md) non appena la stringa viene aggiunta ma prima che i dati dell'elemento siano collegati e a questo punto il membro **ItemData** non è valido.
-   Per modificare la stringa per un elemento in una casella combinata con lo stile **CBS \_ HASSTRINGS** , eliminare l'elemento con il messaggio [CB \_ DELETESTRING](../controls/cb-deletestring.md) e aggiungere la nuova stringa con il messaggio [CB \_ ADDSTRING](../controls/cb-addstring.md) .

 

 
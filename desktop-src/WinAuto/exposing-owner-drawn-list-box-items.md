---
title: Esposizione di Owner-Drawn casella di riepilogo
description: Gli sviluppatori di applicazioni non devono implementare IAccessible per esporre gli elementi in una casella di riepilogo disegnata dal proprietario con lo stile HASSTRINGS di LBS perché Microsoft Active Accessibility espone gli elementi nelle caselle di riepilogo con questo \_ stile.
ms.assetid: d54ce297-ce8a-46c0-a86d-4acffa1eda27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fed68477680376373da6c16f59b3fb556b6a435f15f04daae8f3f1262829dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115274"
---
# <a name="exposing-owner-drawn-list-box-items"></a>Esposizione di Owner-Drawn casella di riepilogo

Gli sviluppatori di applicazioni non devono implementare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per esporre gli elementi in una casella di riepilogo disegnata dal proprietario con lo stile **\_ HASSTRINGS** di LBS perché Microsoft Active Accessibility espone gli elementi nelle caselle di riepilogo con questo stile. Gli elementi in una casella di riepilogo disegnata dal proprietario con lo stile **\_ HASSTRINGS** di LBS vengono visualizzati come testo. Tuttavia, questo stile viene utilizzato anche con caselle di riepilogo disegnate dal proprietario che non visualizzano testo in modo che gli elementi della casella di riepilogo siano esposti da Microsoft Active Accessibility.

Per consentire Microsoft Active Accessibility esporre gli elementi in una casella di riepilogo disegnata dal proprietario che non visualizza testo:

-   Usare lo **stile \_ HASSTRINGS di LBS** durante la creazione della casella di riepilogo.
-   Creare una controparte testuale che nomi o descriva ogni elemento nella casella di riepilogo.
-   Quando si aggiungono elementi alla casella di riepilogo disegnata dal proprietario, usare il messaggio [ \_ LB ADDSTRING](../controls/lb-addstring.md) per aggiungere il testo che si Microsoft Active Accessibility esporre. Questo testo non viene visualizzato, quindi non fa parte dei dati disegnati dal proprietario. Aggiungere i dati dell'elemento disegnati dal proprietario usando il [messaggio \_ LB SETITEMDATA.](../controls/lb-setitemdata.md)

Quando si usa il metodo precedente, tenere presente quanto segue:

-   Se si usa lo stile **\_ LBS SORT,** la casella di riepilogo viene ordinata usando le stringhe fornite e non la routine di callback [ \_ COMPAREITEM di WM.](../controls/wm-compareitem.md)
-   Con le caselle di riepilogo delle variabili create dal proprietario con lo stile **LBS \_ OWNERDRAWVARIABLE**, usare una variabile globale o un altro meccanismo per tenere traccia di quando il membro **itemData** di [MEASUREITEMSTRUCT](/windows/win32/api/winuser/ns-winuser-measureitemstruct) è valido. La variabile globale è necessaria perché il sistema invia il messaggio [WM \_ MEASUREITEM](../controls/wm-measureitem.md) non appena viene aggiunta la stringa ma prima che i dati dell'elemento siano collegati e a questo punto il membro **itemData** non è valido.
-   Per modificare la stringa per un elemento in una casella di riepilogo con lo stile **\_ HASSTRINGS di LBS,** eliminare l'elemento con il messaggio [ \_ LB DELETESTRING](../controls/lb-deletestring.md) e aggiungere la nuova stringa con il messaggio LB \_ ADDSTRING.

 

 
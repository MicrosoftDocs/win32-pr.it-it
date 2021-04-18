---
title: Esposizione Owner-Drawn elementi della casella di riepilogo
description: Gli sviluppatori di applicazioni non devono implementare IAccessible per esporre gli elementi in una casella di riepilogo creata dal proprietario con lo stile LBS \_ HASSTRINGS perché Microsoft Active Accessibility espone gli elementi nelle caselle di riepilogo con questo stile.
ms.assetid: d54ce297-ce8a-46c0-a86d-4acffa1eda27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbb72285f55796a285cd6e1a8838a629218659b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399486"
---
# <a name="exposing-owner-drawn-list-box-items"></a>Esposizione Owner-Drawn elementi della casella di riepilogo

Gli sviluppatori di applicazioni non devono implementare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per esporre gli elementi in una casella di riepilogo creata dal proprietario con lo stile **lbs \_ HASSTRINGS** perché Microsoft Active Accessibility espone gli elementi nelle caselle di riepilogo con questo stile. Gli elementi in una casella di riepilogo creata dal proprietario con lo stile **\_ HASSTRINGS lbs** vengono visualizzati come testo. Questo stile viene tuttavia utilizzato anche con caselle di riepilogo create dal proprietario che non visualizzano testo, in modo che gli elementi della casella di riepilogo siano esposti da Microsoft Active Accessibility.

Per consentire a Microsoft Active Accessibility di esporre gli elementi in una casella di riepilogo creata dal proprietario che non Visualizza il testo:

-   Usare lo **stile \_ HASSTRINGS di lbs** durante la creazione della casella di riepilogo.
-   Creare una controparte testuale che denomina o descriva ogni elemento nella casella di riepilogo.
-   Quando si aggiungono elementi alla casella di riepilogo creata dal proprietario, usare il messaggio [lb \_ ADDSTRING](../controls/lb-addstring.md) per aggiungere il testo che si vuole esporre a Microsoft Active Accessibility. Questo testo non viene visualizzato, quindi non fa parte dei dati creati dal proprietario. Aggiungere i dati dell'elemento creati dal proprietario usando il messaggio [lb \_ SETITEMDATA](../controls/lb-setitemdata.md) .

Quando si usa il metodo precedente, tenere presente quanto segue:

-   Se si usa lo stile di **\_ ordinamento lbs** , la casella di riepilogo viene ordinata con le stringhe fornite e non con la procedura di callback [WM \_ COMPAREITEM](../controls/wm-compareitem.md) .
-   Con le caselle di riepilogo delle variabili disegnate dal proprietario create con lo stile **lbs \_ OwnerDrawVariable**, usare una variabile globale o un altro meccanismo per tenere traccia del momento in cui il **membro ItemData** di [MEASUREITEMSTRUCT](/windows/win32/api/winuser/ns-winuser-measureitemstruct) è valido. La variabile globale è necessaria perché il sistema invia il messaggio [WM \_ MeasureItem](../controls/wm-measureitem.md) non appena la stringa viene aggiunta ma prima che i dati dell'elemento siano collegati e a questo punto il membro **ItemData** non è valido.
-   Per modificare la stringa per un elemento in una casella di riepilogo con lo stile **\_ HASSTRINGS lbs** , eliminare l'elemento con il messaggio [lb \_ DELETESTRING](../controls/lb-deletestring.md) e aggiungere la nuova stringa con il \_ messaggio lb ADDSTRING.

 

 
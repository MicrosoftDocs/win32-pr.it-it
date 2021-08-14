---
title: Proprietà DefaultAction
description: La proprietà DefaultAction di un oggetto descrive il metodo principale di manipolazione dell'oggetto dal punto di vista dell'utente. La proprietà DefaultAction di un oggetto deve essere un verbo o una breve frase di verbo.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd5aa70e0c6c633aa5b0ca3fe5c40049dbeb8cf2496c7785eea513821e1d5ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325755"
---
# <a name="defaultaction-property"></a>Proprietà DefaultAction

La proprietà **DefaultAction** di un oggetto descrive il metodo principale di manipolazione dell'oggetto dal punto di vista dell'utente. La proprietà **DefaultAction** di un oggetto deve essere un verbo o una breve frase di verbo.

La **proprietà DefaultAction** viene recuperata chiamando [**IAccessible::get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).

Per eseguire l'azione predefinita di un oggetto, i client chiamano [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).

Non tutti gli oggetti hanno azioni predefinite e alcuni oggetti hanno un'azione predefinita correlata alla relativa proprietà [**Value,**](value-property.md) come negli esempi seguenti:

-   Una casella di controllo selezionata ha un'azione predefinita "Deseleziona" e il valore "Checked".
-   Una casella di controllo deselezionata ha un'azione predefinita "Check" e il valore "Unchecked".
-   Un pulsante con etichetta "Stampa" ha un'azione predefinita "Press", senza alcun valore.
-   Un controllo di testo statico o un controllo di modifica che mostra "Printer" non ha alcuna azione predefinita, ma ha il valore "Printer".

 

 





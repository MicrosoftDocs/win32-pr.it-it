---
title: Proprietà DefaultAction
description: La proprietà DefaultAction di un oggetto descrive il metodo principale di manipolazione dell'oggetto dal punto di vista dell'utente. La proprietà DefaultAction di un oggetto deve essere un verbo o una frase verbo breve.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc032037c331a2022f227cb8e8547dd8bce9d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328847"
---
# <a name="defaultaction-property"></a>Proprietà DefaultAction

La proprietà **DefaultAction** di un oggetto descrive il metodo principale di manipolazione dell'oggetto dal punto di vista dell'utente. La proprietà **DefaultAction** di un oggetto deve essere un verbo o una frase verbo breve.

La proprietà **DefaultAction** viene recuperata chiamando [**IAccessible:: Get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).

Per eseguire l'azione predefinita di un oggetto, i client chiamano [**IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).

Non tutti gli oggetti hanno azioni predefinite e alcuni oggetti hanno un'azione predefinita correlata alla relativa proprietà [**value**](value-property.md) , come negli esempi seguenti:

-   Una casella di controllo selezionata ha un'azione predefinita "deseleziona" e un valore "checked".
-   Una casella di controllo deselezionata ha un'azione predefinita "verifica" e un valore "deselezionato".
-   Un pulsante con etichetta "stampa" ha un'azione predefinita "premere", senza alcun valore.
-   Un controllo testo statico o un controllo di modifica che mostra "stampante" non ha un'azione predefinita, ma ha un valore "Printer".

 

 





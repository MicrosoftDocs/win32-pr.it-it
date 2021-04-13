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
# <a name="defaultaction-property"></a><span data-ttu-id="4fdfe-104">Proprietà DefaultAction</span><span class="sxs-lookup"><span data-stu-id="4fdfe-104">DefaultAction Property</span></span>

<span data-ttu-id="4fdfe-105">La proprietà **DefaultAction** di un oggetto descrive il metodo principale di manipolazione dell'oggetto dal punto di vista dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4fdfe-105">An object's **DefaultAction** property describes the object's primary method of manipulation from the user's viewpoint.</span></span> <span data-ttu-id="4fdfe-106">La proprietà **DefaultAction** di un oggetto deve essere un verbo o una frase verbo breve.</span><span class="sxs-lookup"><span data-stu-id="4fdfe-106">An object's **DefaultAction** property should be a verb or a short verb phrase.</span></span>

<span data-ttu-id="4fdfe-107">La proprietà **DefaultAction** viene recuperata chiamando [**IAccessible:: Get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).</span><span class="sxs-lookup"><span data-stu-id="4fdfe-107">The **DefaultAction** property is retrieved by calling [**IAccessible::get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).</span></span>

<span data-ttu-id="4fdfe-108">Per eseguire l'azione predefinita di un oggetto, i client chiamano [**IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).</span><span class="sxs-lookup"><span data-stu-id="4fdfe-108">To perform an object's default action, clients call [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).</span></span>

<span data-ttu-id="4fdfe-109">Non tutti gli oggetti hanno azioni predefinite e alcuni oggetti hanno un'azione predefinita correlata alla relativa proprietà [**value**](value-property.md) , come negli esempi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4fdfe-109">Not all objects have default actions, and some objects have a default action that is related to its [**Value**](value-property.md) property, such as in the following examples:</span></span>

-   <span data-ttu-id="4fdfe-110">Una casella di controllo selezionata ha un'azione predefinita "deseleziona" e un valore "checked".</span><span class="sxs-lookup"><span data-stu-id="4fdfe-110">A selected check box has a default action of "Uncheck" and a value of "Checked."</span></span>
-   <span data-ttu-id="4fdfe-111">Una casella di controllo deselezionata ha un'azione predefinita "verifica" e un valore "deselezionato".</span><span class="sxs-lookup"><span data-stu-id="4fdfe-111">A cleared check box has a default action of "Check" and a value of "Unchecked."</span></span>
-   <span data-ttu-id="4fdfe-112">Un pulsante con etichetta "stampa" ha un'azione predefinita "premere", senza alcun valore.</span><span class="sxs-lookup"><span data-stu-id="4fdfe-112">A button labeled "Print" has a default action of "Press," with no value.</span></span>
-   <span data-ttu-id="4fdfe-113">Un controllo testo statico o un controllo di modifica che mostra "stampante" non ha un'azione predefinita, ma ha un valore "Printer".</span><span class="sxs-lookup"><span data-stu-id="4fdfe-113">A static text control or an edit control that shows "Printer" has no default action, but has a value of "Printer."</span></span>

 

 





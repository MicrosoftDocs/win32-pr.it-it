---
title: Errore di ARIA TabIndex
description: Errore di ARIA TabIndex
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- AriaTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acfec56fe1f9f6074579a8b84bccc9dfdef2e1da
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104047533"
---
# <a name="aria-tabindex-error"></a><span data-ttu-id="e0ad6-104">Errore di ARIA TabIndex</span><span class="sxs-lookup"><span data-stu-id="e0ad6-104">ARIA Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="e0ad6-105">Testo</span><span class="sxs-lookup"><span data-stu-id="e0ad6-105">Text</span></span>

<span data-ttu-id="e0ad6-106">L'elemento non è disabilitato e ha un gestore dell'evento **Click** , ma contiene **TabIndex** < 0 e non è nell'ordine di tabulazione per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e0ad6-106">Element is not disabled and has a **click** event handler but it has **tabIndex** < 0 and is not in the tab order by default.</span></span>

## <a name="type"></a><span data-ttu-id="e0ad6-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0ad6-107">Type</span></span>

<span data-ttu-id="e0ad6-108">Errore</span><span class="sxs-lookup"><span data-stu-id="e0ad6-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="e0ad6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0ad6-109">Description</span></span>

<span data-ttu-id="e0ad6-110">Questo errore si applica agli elementi che dispongono di un gestore dell'evento click e che non sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="e0ad6-110">This error applies to elements that have a click event handler and are not disabled.</span></span> <span data-ttu-id="e0ad6-111">Questi elementi devono essere nell'ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="e0ad6-111">These elements must be in the tab order.</span></span> <span data-ttu-id="e0ad6-112">In questo modo si garantisce che un elemento possa essere raggiunto usando il tasto TAB, che è il modo in cui gli utenti dello screen reader navigano in genere nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="e0ad6-112">This ensures that an element can be reached using the Tab key, which is how screen reader users typically navigate the UI.</span></span>

<span data-ttu-id="e0ad6-113">Per correggere l'errore, impostare l'attributo [**TabIndex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) su un valore uguale o maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="e0ad6-113">To fix this error, set the [**tabindex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) attribute to a value that is equal to or greater than 0.</span></span> <span data-ttu-id="e0ad6-114">Non è necessario impostare in modo esplicito l' **attributo tabIndex** per i tag presenti nell'ordine di tabulazione per impostazione predefinita, ad esempio un (con attributo [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) ), un [**pulsante**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**un**](https://developer.mozilla.org/docs/Web/HTML/Element/a) [**input**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (escluso "hidden"), [**Select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)e [**area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (come parte della mappa immagine).</span><span class="sxs-lookup"><span data-stu-id="e0ad6-114">You do not need to explicitly set the **tabindex** attribute for tags that are in the tab order by default, such as [**a**](https://developer.mozilla.org/docs/Web/HTML/Element/a) (with [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) attribute), [**button**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**input**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (excluding "hidden"), [**select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea), and [**area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (as part of the image map).</span></span>

## <a name="example"></a><span data-ttu-id="e0ad6-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="e0ad6-115">Example</span></span>


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 





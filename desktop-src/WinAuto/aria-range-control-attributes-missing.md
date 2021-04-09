---
title: Attributi controllo intervallo ARIA mancanti
description: Attributi controllo intervallo ARIA mancanti
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- AriaRangeControlAttributesAbsentId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cd32a7a4807f06c26bd013ee3fd294d33cc57
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104047529"
---
# <a name="aria-range-control-attributes-missing"></a><span data-ttu-id="a71bd-104">Attributi controllo intervallo ARIA mancanti</span><span class="sxs-lookup"><span data-stu-id="a71bd-104">ARIA Range Control Attributes Missing</span></span>

## <a name="text"></a><span data-ttu-id="a71bd-105">Testo</span><span class="sxs-lookup"><span data-stu-id="a71bd-105">Text</span></span>

<span data-ttu-id="a71bd-106">L'elemento ha un ruolo **ProgressBar** o **Slider** ma non espone gli attributi **aria-valuemin** , **aria-valuemax** e **aria-valuenow** corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="a71bd-106">Element has **progressbar** or **slider** role but is not exposing corresponding **aria-valuemin** , **aria-valuemax** , and **aria-valuenow** attributes.</span></span>

## <a name="type"></a><span data-ttu-id="a71bd-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="a71bd-107">Type</span></span>

<span data-ttu-id="a71bd-108">Errore</span><span class="sxs-lookup"><span data-stu-id="a71bd-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="a71bd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a71bd-109">Description</span></span>

<span data-ttu-id="a71bd-110">Questo errore si applica a elementi con un [**ruolo**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicito o esplicito) uguale a **ProgressBar**, **Slider** o **SpinButton**.</span><span class="sxs-lookup"><span data-stu-id="a71bd-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) that is equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="a71bd-111">Secondo le specifiche delle applicazioni Internet (WAI-ARIA) accessibili per Web Accessibility Initiative, gli elementi che hanno il ruolo **ProgressBar**, **Slider** o **SpinButton** devono esporre gli attributi [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)e [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="a71bd-111">According to the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) specification, elements that have the **progressbar**, **slider**, or **spinbutton** role must expose the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="a71bd-112">Per correggere l'errore, impostare gli [**attributi aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)e [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e mantenere dinamicamente il valore **aria-valuenow** per assicurarsi che il valore corrente venga esposto.</span><span class="sxs-lookup"><span data-stu-id="a71bd-112">To fix this error, set the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes, and dynamically maintain the **aria-valuenow** value to ensure that the current value is exposed.</span></span> <span data-ttu-id="a71bd-113">È anche necessario impostare l'attributo [**aria-ValueText**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) per aggiungere altro significato al valore **aria-valuenow** esposto.</span><span class="sxs-lookup"><span data-stu-id="a71bd-113">You should also set the [**aria-valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to add more meaning to the exposed **aria-valuenow** value.</span></span>

## <a name="example"></a><span data-ttu-id="a71bd-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="a71bd-114">Example</span></span>


```HTML
<div role="slider" id="sl" aria-valuemin="1" aria-valuemax="5" aria-valuenow="3" aria-valuetext="good"…>
</div>

<script>
  // This function should be triggered when the slider value changes.
  function manageValue()
  {
    ...
    sl.setAttribute("aria-valuenow", currentValue);
    sl.setAttribute("aria-valuetext", currentValueText);
    ...
  }
</script>
```



## <a name="related-topics"></a><span data-ttu-id="a71bd-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a71bd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a71bd-116">Attributi di controllo intervallo ARIA incompatibili</span><span class="sxs-lookup"><span data-stu-id="a71bd-116">ARIA Range Control Attributes Incompatible</span></span>](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 





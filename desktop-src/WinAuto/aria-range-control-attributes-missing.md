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
# <a name="aria-range-control-attributes-missing"></a>Attributi controllo intervallo ARIA mancanti

## <a name="text"></a>Testo

L'elemento ha un ruolo **ProgressBar** o **Slider** ma non espone gli attributi **aria-valuemin** , **aria-valuemax** e **aria-valuenow** corrispondenti.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica a elementi con un [**ruolo**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicito o esplicito) uguale a **ProgressBar**, **Slider** o **SpinButton**.

Secondo le specifiche delle applicazioni Internet (WAI-ARIA) accessibili per Web Accessibility Initiative, gli elementi che hanno il ruolo **ProgressBar**, **Slider** o **SpinButton** devono esporre gli attributi [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)e [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .

Per correggere l'errore, impostare gli [**attributi aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)e [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e mantenere dinamicamente il valore **aria-valuenow** per assicurarsi che il valore corrente venga esposto. È anche necessario impostare l'attributo [**aria-ValueText**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) per aggiungere altro significato al valore **aria-valuenow** esposto.

## <a name="example"></a>Esempio


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi di controllo intervallo ARIA incompatibili](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 





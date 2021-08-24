---
title: Attributi di controllo dell'intervallo ARIA mancanti
description: Attributi di controllo dell'intervallo ARIA mancanti
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- AriaRangeControlAttributesAbsentId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44e4e5c69ea6971846ed9ef5f3a6108bb488c6effb21a6cbc75953ed1bb780e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645120"
---
# <a name="aria-range-control-attributes-missing"></a>Attributi di controllo dell'intervallo ARIA mancanti

## <a name="text"></a>Testo

L'elemento ha  **il ruolo** di indicatore di stato o dispositivo di scorrimento, ma non espone gli attributi **aria-valuemin** , **aria-valuemax** e **aria-valuenow** corrispondenti.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica agli elementi con un [**ruolo**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicito o esplicito) uguale all'indicatore di stato **,** al dispositivo di **scorrimento** o al pulsante **di selezione**.

In base alla specifica WAI-ARIA (Web Accessibility Initiative - Accessible Rich Internet Applications), gli elementi con il ruolo indicatore di **stato,** dispositivo di scorrimento o **pulsante** di selezione devono esporre gli attributi [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)e [**aria-valuenow.**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)

Per correggere l'errore, impostare gli attributi [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)e [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e mantenere dinamicamente il valore **aria-valuenow** per assicurarsi che il valore corrente sia esposto. È anche necessario impostare [**l'attributo aria-valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) per aggiungere più significato al **valore aria-valuenow** esposto.

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

[Attributi di controllo dell'intervallo ARIA incompatibili](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 





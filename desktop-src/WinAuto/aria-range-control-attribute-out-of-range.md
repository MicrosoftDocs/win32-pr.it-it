---
title: Attributi di controllo intervallo ARIA incompatibili
description: Attributi di controllo intervallo ARIA incompatibili
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- AriaRangeControlAttributesIncompatibleId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef55ee57c4966896e666dd5a7ac1d20eb5257c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104517188"
---
# <a name="aria-range-control-attributes-incompatible"></a>Attributi di controllo intervallo ARIA incompatibili

## <a name="text"></a>Testo

L'elemento ha un ruolo **ProgressBar** o **Slider** , ma il valore **aria-valuenow** esposto è esterno all'intervallo aria- **valuemin** **aria-valuemax** .

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica a elementi con un [**ruolo**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicito o esplicito) uguale a **ProgressBar**, **Slider** o **SpinButton**.

Questo errore indica che il valore [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) esposto non è compreso nell'intervallo definito dagli attributi [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .

Per correggere l'errore, controllare l'implementazione per assicurarsi che gli attributi [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) siano impostati correttamente e che il valore dell'attributo [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) sia gestito correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi controllo intervallo ARIA mancanti](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 





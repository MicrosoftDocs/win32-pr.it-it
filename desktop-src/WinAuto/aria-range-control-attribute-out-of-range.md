---
title: Attributi del controllo intervallo ARIA incompatibili
description: Attributi del controllo intervallo ARIA incompatibili
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- AriaRangeControlAttributesIncompatibleId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f5de18be88682046cac6c4d4156f48fd3e4994d2e7b9ab1bbdc52f0a2e768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326750"
---
# <a name="aria-range-control-attributes-incompatible"></a>Attributi del controllo intervallo ARIA incompatibili

## <a name="text"></a>Testo

L'elemento **ha il ruolo progressbar** **o slider,** ma il valore **aria-valuenow** esposto non è compreso nell'intervallo **aria-valuemin** **aria-valuemax.**

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica agli elementi con [**un**](https://developer.mozilla.org/docs/Web/HTML/Reference) ruolo (implicito o esplicito) uguale a **progressbar,** **slider** o **spinbutton.**

Questo errore indica che il valore [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) esposto non è compreso nell'intervallo definito dagli attributi [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e [**aria-valuemax.**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)

Per correggere questo errore, controllare l'implementazione per assicurarsi che gli attributi [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) siano impostati correttamente e che il valore dell'attributo [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) sia mantenuto correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi del controllo intervallo ARIA mancanti](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 





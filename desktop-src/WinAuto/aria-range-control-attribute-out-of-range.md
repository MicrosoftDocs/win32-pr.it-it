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
# <a name="aria-range-control-attributes-incompatible"></a><span data-ttu-id="58231-104">Attributi di controllo intervallo ARIA incompatibili</span><span class="sxs-lookup"><span data-stu-id="58231-104">ARIA Range Control Attributes Incompatible</span></span>

## <a name="text"></a><span data-ttu-id="58231-105">Testo</span><span class="sxs-lookup"><span data-stu-id="58231-105">Text</span></span>

<span data-ttu-id="58231-106">L'elemento ha un ruolo **ProgressBar** o **Slider** , ma il valore **aria-valuenow** esposto è esterno all'intervallo aria- **valuemin** **aria-valuemax** .</span><span class="sxs-lookup"><span data-stu-id="58231-106">Element has **progressbar** or **slider** role but exposed **aria-valuenow** value is outside of **aria-valuemin** **aria-valuemax** range.</span></span>

## <a name="type"></a><span data-ttu-id="58231-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="58231-107">Type</span></span>

<span data-ttu-id="58231-108">Errore</span><span class="sxs-lookup"><span data-stu-id="58231-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="58231-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58231-109">Description</span></span>

<span data-ttu-id="58231-110">Questo errore si applica a elementi con un [**ruolo**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicito o esplicito) uguale a **ProgressBar**, **Slider** o **SpinButton**.</span><span class="sxs-lookup"><span data-stu-id="58231-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="58231-111">Questo errore indica che il valore [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) esposto non è compreso nell'intervallo definito dagli attributi [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="58231-111">This error indicates that the exposed [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) value is not in the range defined by the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="58231-112">Per correggere l'errore, controllare l'implementazione per assicurarsi che gli attributi [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) siano impostati correttamente e che il valore dell'attributo [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) sia gestito correttamente.</span><span class="sxs-lookup"><span data-stu-id="58231-112">To fix this error, check your implementation to ensure that the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes are correctly set, and that the [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute value is properly maintained.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58231-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58231-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58231-114">Attributi controllo intervallo ARIA mancanti</span><span class="sxs-lookup"><span data-stu-id="58231-114">ARIA Range Control Attributes Missing</span></span>](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 





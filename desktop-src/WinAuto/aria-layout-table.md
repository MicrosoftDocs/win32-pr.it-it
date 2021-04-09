---
title: Errore della tabella di presentazione ARIA
description: Errore della tabella di presentazione ARIA
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- AriaLayoutTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1ef7cae971e6dc365bd3f8ebe6135561f3ff3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734586"
---
# <a name="aria-presentation-table-error"></a><span data-ttu-id="1cb2a-104">Errore della tabella di presentazione ARIA</span><span class="sxs-lookup"><span data-stu-id="1cb2a-104">ARIA Presentation Table Error</span></span>

## <a name="text"></a><span data-ttu-id="1cb2a-105">Testo</span><span class="sxs-lookup"><span data-stu-id="1cb2a-105">Text</span></span>

<span data-ttu-id="1cb2a-106">Per la tabella usata per il layout non devono essere definite intestazioni, nome accessibile o informazioni di riepilogo (**th**, **Summary**, **aria-describedby**, **aria-labelledby**, **aria-etichetta**, **titolo**, attributi **didascalia** ).</span><span class="sxs-lookup"><span data-stu-id="1cb2a-106">Table used for layout must not have header, accessible name or summary information defined (**th**, **summary**, **aria-describedby**, **aria-labelledby**, **aria-label**, **title**, **caption** attributes).</span></span>

## <a name="type"></a><span data-ttu-id="1cb2a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="1cb2a-107">Type</span></span>

<span data-ttu-id="1cb2a-108">Errore</span><span class="sxs-lookup"><span data-stu-id="1cb2a-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="1cb2a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cb2a-109">Description</span></span>

<span data-ttu-id="1cb2a-110">Questo errore si applica ai tag della tabella HTML con l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) impostato su "Presentation" o con una tabella con una sola cella (1 × 1 tabella).</span><span class="sxs-lookup"><span data-stu-id="1cb2a-110">This error applies to HTML table tags that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set to "presentation", or with a table that has a single cell (1×1 table).</span></span>

<span data-ttu-id="1cb2a-111">Questo errore indica che una tabella è contrassegnata come solo layout (ha `role="presentation"` ), ma contiene anche informazioni sull'accessibilità come se si trattasse di una tabella di dati, che può essere confusa per gli utenti di lettura schermo.</span><span class="sxs-lookup"><span data-stu-id="1cb2a-111">This error indicates that a table is marked as layout only (has `role="presentation"`), but it also contains accessibility information as if it was a data table, which can be confusing for screen reader users.</span></span>

<span data-ttu-id="1cb2a-112">Per risolvere questo errore, determinare se la tabella è effettivamente semplicemente una tabella di layout e, in caso affermativo, rimuovere il markup accessibile:</span><span class="sxs-lookup"><span data-stu-id="1cb2a-112">To address this error, determine whether the table actually is just a layout table and, if so, remove the accessible markup:</span></span>

-   <span data-ttu-id="1cb2a-113">Elemento [**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) , [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-etichetta**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)o [**titolo**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributi.</span><span class="sxs-lookup"><span data-stu-id="1cb2a-113">[**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) element, [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span>
-   <span data-ttu-id="1cb2a-114">attributi [**Summary**](https://www.bing.com/search?q=**summary**) o [**aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="1cb2a-114">[**summary**](https://www.bing.com/search?q=**summary**) or [**aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>
-   <span data-ttu-id="1cb2a-115">Tag [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) .</span><span class="sxs-lookup"><span data-stu-id="1cb2a-115">[**THEAD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags.</span></span>

## <a name="example"></a><span data-ttu-id="1cb2a-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="1cb2a-116">Example</span></span>

![<span data-ttu-id="1cb2a-117">HTML per un elemento Table, con attributi, ad esempio Riepilogo, che attivano l'errore della tabella di presentazione aria mostrata come markup HTML sottoposta a indisponibilità</span><span class="sxs-lookup"><span data-stu-id="1cb2a-117">html for a table element, with attributes such as summary that trigger the aria presentation table error shown as struck-out html markup</span></span> ](images/aria-layout-table.png)

## <a name="remarks"></a><span data-ttu-id="1cb2a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cb2a-118">Remarks</span></span>

<span data-ttu-id="1cb2a-119">Se si determina che una tabella necessita di informazioni sull'accessibilità, rimuovere l'attributo [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) o impostarlo su un valore diverso da "Presentation".</span><span class="sxs-lookup"><span data-stu-id="1cb2a-119">If you determine that a table does need accessibility information, remove the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute or set it to a value other than "presentation".</span></span>

 

 





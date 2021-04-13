---
title: Errore di tabella dati ARIA
description: Errore di tabella dati ARIA
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- AriaDataTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286f88a0b3a0d962fd6ac45581f94bc351cb507
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399844"
---
# <a name="aria-data-table-error"></a><span data-ttu-id="093e2-104">Errore di tabella dati ARIA</span><span class="sxs-lookup"><span data-stu-id="093e2-104">ARIA Data Table Error</span></span>

## <a name="text"></a><span data-ttu-id="093e2-105">Testo</span><span class="sxs-lookup"><span data-stu-id="093e2-105">Text</span></span>

<span data-ttu-id="093e2-106">La tabella contiene dati ma non ha un markup accessibile definito anche se **aria-label**, **aria-labelledby**, **titolo**, **didascalia** **o elementi** .</span><span class="sxs-lookup"><span data-stu-id="093e2-106">Table contains data but doesn't have accessible markup defined though **aria-label**, **aria-labelledby**, **title**, **caption** or **th** elements.</span></span>

## <a name="type"></a><span data-ttu-id="093e2-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="093e2-107">Type</span></span>

<span data-ttu-id="093e2-108">Errore</span><span class="sxs-lookup"><span data-stu-id="093e2-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="093e2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="093e2-109">Description</span></span>

<span data-ttu-id="093e2-110">Questo errore si applica alle tabelle HTML con più di una cella.</span><span class="sxs-lookup"><span data-stu-id="093e2-110">This error applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="093e2-111">Questo errore non si applica alle tabelle con `role="presentation"` perché sono considerate tabelle di layout.</span><span class="sxs-lookup"><span data-stu-id="093e2-111">This error does not apply to tables with `role="presentation"` because these are considered to be layout tables.</span></span>

<span data-ttu-id="093e2-112">Questo errore indica che una tabella dati non ha un nome accessibile o informazioni di intestazione.</span><span class="sxs-lookup"><span data-stu-id="093e2-112">This error indicates that a data table doesn’t have an accessible name or header information.</span></span>

<span data-ttu-id="093e2-113">Per correggere l'errore, definire un nome accessibile usando il tag [**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) oppure gli attributi [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)o [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) .</span><span class="sxs-lookup"><span data-stu-id="093e2-113">To fix this error, define an accessible name by using the [**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) tag, or the [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span> <span data-ttu-id="093e2-114">Se nella tabella mancano informazioni di intestazione, utilizzare i tag [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) per contrassegnare le celle di intestazione.</span><span class="sxs-lookup"><span data-stu-id="093e2-114">If the table is missing header information, use [**THead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags to mark header cells.</span></span>

## <a name="example"></a><span data-ttu-id="093e2-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="093e2-115">Example</span></span>


```HTML
<!-- Data tables must contain an accessibile name and header information. -->
<table>
  <caption>ARIA Examples</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      ...
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Accessible tables</td>
      <td>This example illustrates how to make data tables accessible using ARIA</td>
      ...
    </tr>
  </tbody>
</table>
```



 

 





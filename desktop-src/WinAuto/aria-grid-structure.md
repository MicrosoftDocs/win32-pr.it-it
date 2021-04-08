---
title: Errore struttura griglia ARIA
description: Errore struttura griglia ARIA
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- AriaGridStructureErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd692c5fb82675b8fdcc6bf88fe35695113c9ef0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734594"
---
# <a name="aria-grid-structure-error"></a><span data-ttu-id="e282c-104">Errore struttura griglia ARIA</span><span class="sxs-lookup"><span data-stu-id="e282c-104">ARIA Grid Structure Error</span></span>

## <a name="text"></a><span data-ttu-id="e282c-105">Testo</span><span class="sxs-lookup"><span data-stu-id="e282c-105">Text</span></span>

<span data-ttu-id="e282c-106">L'elemento con il ruolo **Grid** non dispone di una struttura di griglia o di un markup accessibile corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e282c-106">Element with the **grid** role doesn't have a corresponding grid structure or accessible markup.</span></span>

## <a name="type"></a><span data-ttu-id="e282c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e282c-107">Type</span></span>

<span data-ttu-id="e282c-108">Errore</span><span class="sxs-lookup"><span data-stu-id="e282c-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="e282c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e282c-109">Description</span></span>

<span data-ttu-id="e282c-110">Questo errore si applica agli elementi personalizzati per i quali l'attributo **Role** è impostato su "Grid".</span><span class="sxs-lookup"><span data-stu-id="e282c-110">This error applies to custom elements that have the **role** attribute set to "grid".</span></span> <span data-ttu-id="e282c-111">Non si applica ai tag di tabella HTML con **ruolo** implicito "Grid".</span><span class="sxs-lookup"><span data-stu-id="e282c-111">It does not apply to HTML table tags that have an implicit **role** of "grid".</span></span>

<span data-ttu-id="e282c-112">Un elemento il cui attributo **Role** è impostato su "Grid" deve avere la struttura definita dal ruolo Grid (Wai-aria) accessibile Web Accessibility Initiative, incluso il nome accessibile per la griglia e i relativi sottoelementi di intestazione.</span><span class="sxs-lookup"><span data-stu-id="e282c-112">An element that has its **role** attribute set to "grid" must have the structure defined by the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) grid role, including the accessible name for the grid and its header subelements.</span></span>

<span data-ttu-id="e282c-113">Per correggere l'errore, esaminare l'implementazione per assicurarsi che sia conforme alla specifica WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="e282c-113">To fix this error, review your implementation to ensure that it complies with the WAI-ARIA specification.</span></span> <span data-ttu-id="e282c-114">In particolare, assicurarsi che la struttura soddisfi le regole seguenti.</span><span class="sxs-lookup"><span data-stu-id="e282c-114">Specifically, ensure that the structure meets the following rules.</span></span>

-   <span data-ttu-id="e282c-115">la **griglia** contiene elementi **Row** o **rowgroup** .</span><span class="sxs-lookup"><span data-stu-id="e282c-115">**grid** contains **row** or **rowgroup** elements.</span></span>
-   <span data-ttu-id="e282c-116">**rowgroup** contiene elementi **Row** .</span><span class="sxs-lookup"><span data-stu-id="e282c-116">**rowgroup** contains **row** elements.</span></span>
-   <span data-ttu-id="e282c-117">gli elementi **Row** contengono elementi **ColumnHeader** o **GridCell** o **RowHeader** .</span><span class="sxs-lookup"><span data-stu-id="e282c-117">**row** elements contain **columnheader** or **gridcell** or **rowheader** elements.</span></span>

<span data-ttu-id="e282c-118">Per gli elementi **Grid**, **ColumnHeader**, **GridCell** e **RowHeader** è necessario definire un nome accessibile utilizzando uno degli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e282c-118">An accessible name should be defined for **grid**, **columnheader**, **gridcell** and **rowheader** elements by using one of the following attributes.</span></span>

-   <span data-ttu-id="e282c-119">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributo per fare riferimento all'elemento contenente il testo.</span><span class="sxs-lookup"><span data-stu-id="e282c-119">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute for referencing the element containing text.</span></span>
-   <span data-ttu-id="e282c-120">[**aria-etichetta**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributo per impostare direttamente il nome accessibile.</span><span class="sxs-lookup"><span data-stu-id="e282c-120">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to set the accessible name directly.</span></span>
-   <span data-ttu-id="e282c-121">[**titolo**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) per la creazione di una descrizione comando che viene utilizzata allo stesso tempo come nome.</span><span class="sxs-lookup"><span data-stu-id="e282c-121">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) for creating a tooltip which is at the same time used as a name.</span></span>

 

 





---
description: Contiene la classificazione di confidenza restituita da Journal Ink Analyzer per InkWord.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Elemento Confidence
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cef4869776a6cafc4e6ef4758649b918e0b5988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128131"
---
# <a name="confidence-element"></a><span data-ttu-id="7058e-103">Elemento Confidence</span><span class="sxs-lookup"><span data-stu-id="7058e-103">Confidence Element</span></span>

<span data-ttu-id="7058e-104">Contiene la classificazione di confidenza restituita da Journal Ink Analyzer per [**InkWord**](inkword-element.md).</span><span class="sxs-lookup"><span data-stu-id="7058e-104">Contains the confidence rating returned by the Journal ink analyzer for the [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="7058e-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="7058e-105">Definition</span></span>

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="7058e-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="7058e-106">Parent Elements</span></span>

[<span data-ttu-id="7058e-107">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="7058e-107">**InkWord**</span></span>](inkword-element.md)

## <a name="values"></a><span data-ttu-id="7058e-108">Valori</span><span class="sxs-lookup"><span data-stu-id="7058e-108">Values</span></span>

<span data-ttu-id="7058e-109">I valori validi per questo campo sono "0", "1" e "2".</span><span class="sxs-lookup"><span data-stu-id="7058e-109">Valid values for this field include "0", "1", and "2".</span></span> <span data-ttu-id="7058e-110">0 indica una confidenza elevata, 1 indica una confidenza intermedia e 2 indica una scarsa confidenza.</span><span class="sxs-lookup"><span data-stu-id="7058e-110">0 indicates Strong confidence, 1 indicates Intermediate confidence, and 2 indicates Poor confidence.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7058e-111">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7058e-111">Child Elements</span></span>

<span data-ttu-id="7058e-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="7058e-112">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="7058e-113">Attributi</span><span class="sxs-lookup"><span data-stu-id="7058e-113">Attributes</span></span>

<span data-ttu-id="7058e-114">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="7058e-114">None.</span></span>

## <a name="element-information"></a><span data-ttu-id="7058e-115">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="7058e-115">Element Information</span></span>



|              |                                            |
|--------------|--------------------------------------------|
| <span data-ttu-id="7058e-116">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="7058e-116">Element type</span></span> | <span data-ttu-id="7058e-117">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="7058e-117">**xs:string**</span></span>                              |
| <span data-ttu-id="7058e-118">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7058e-118">Namespace</span></span>    | <span data-ttu-id="7058e-119">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="7058e-119">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="7058e-120">Nome schema</span><span class="sxs-lookup"><span data-stu-id="7058e-120">Schema name</span></span>  | <span data-ttu-id="7058e-121">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="7058e-121">Journal Reader</span></span>                             |



 

 

 




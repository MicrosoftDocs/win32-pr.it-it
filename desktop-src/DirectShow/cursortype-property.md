---
description: La proprietà CursorType imposta o Recupera il tipo di cursore corrente.
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: Proprietà CursorType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876585"
---
# <a name="cursortype-property"></a><span data-ttu-id="ed369-103">Proprietà CursorType</span><span class="sxs-lookup"><span data-stu-id="ed369-103">CursorType Property</span></span>

> [!Note]  
> <span data-ttu-id="ed369-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ed369-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ed369-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="ed369-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ed369-106">La `CursorType` proprietà imposta o Recupera il tipo di cursore corrente.</span><span class="sxs-lookup"><span data-stu-id="ed369-106">The `CursorType` property sets or retrieves the current cursor type.</span></span>

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a><span data-ttu-id="ed369-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed369-107">Return Value</span></span>

<span data-ttu-id="ed369-108">Restituisce un valore intero che rappresenta il tipo di cursore.</span><span class="sxs-lookup"><span data-stu-id="ed369-108">Returns an integer value representing the cursor type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed369-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed369-109">Remarks</span></span>

<span data-ttu-id="ed369-110">I valori possibili per questa proprietà sono:</span><span class="sxs-lookup"><span data-stu-id="ed369-110">The possible values for this property are:</span></span>



| <span data-ttu-id="ed369-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ed369-111">Value</span></span> | <span data-ttu-id="ed369-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed369-112">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="ed369-113">0</span><span class="sxs-lookup"><span data-stu-id="ed369-113">0</span></span>     | <span data-ttu-id="ed369-114">Freccia</span><span class="sxs-lookup"><span data-stu-id="ed369-114">Arrow</span></span>       |
| <span data-ttu-id="ed369-115">1</span><span class="sxs-lookup"><span data-stu-id="ed369-115">1</span></span>     | <span data-ttu-id="ed369-116">Zoom avanti</span><span class="sxs-lookup"><span data-stu-id="ed369-116">Zoom In</span></span>     |
| <span data-ttu-id="ed369-117">2</span><span class="sxs-lookup"><span data-stu-id="ed369-117">2</span></span>     | <span data-ttu-id="ed369-118">Zoom indietro</span><span class="sxs-lookup"><span data-stu-id="ed369-118">Zoom Out</span></span>    |
| <span data-ttu-id="ed369-119">3</span><span class="sxs-lookup"><span data-stu-id="ed369-119">3</span></span>     | <span data-ttu-id="ed369-120">A sinistra</span><span class="sxs-lookup"><span data-stu-id="ed369-120">Hand</span></span>        |
| <span data-ttu-id="ed369-121">-1</span><span class="sxs-lookup"><span data-stu-id="ed369-121">-1</span></span>    | <span data-ttu-id="ed369-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="ed369-122">None</span></span>        |



 

<span data-ttu-id="ed369-123">Questa proprietà è di lettura/scrittura e il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="ed369-123">This property is read/write with a default value of zero.</span></span> <span data-ttu-id="ed369-124">Quando l'immagine viene ingrandita, l'impostazione `CursorType` su **Hand** (0x3) consente di attivare la modalità di trascinamento dell'applicazione, consentendo all'utente di spostare l'immagine all'interno dell'area di visualizzazione del video.</span><span class="sxs-lookup"><span data-stu-id="ed369-124">When the picture is zoomed in, setting `CursorType` to **Hand** (0x3) puts the application into drag mode, enabling the user to move the image inside the video display area.</span></span>

 

 




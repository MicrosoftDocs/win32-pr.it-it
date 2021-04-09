---
description: La proprietà CurrentCCService imposta o Recupera il servizio di Captioning chiuso corrente.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Proprietà CurrentCCService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5c1ddf243b0ec943be1f22930a8802d28d1bda
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876705"
---
# <a name="currentccservice-property"></a><span data-ttu-id="87200-103">Proprietà CurrentCCService</span><span class="sxs-lookup"><span data-stu-id="87200-103">CurrentCCService Property</span></span>

> [!Note]  
> <span data-ttu-id="87200-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="87200-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="87200-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="87200-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="87200-106">La `CurrentCCService` proprietà imposta o Recupera il servizio di didascalia corrente chiuso.</span><span class="sxs-lookup"><span data-stu-id="87200-106">The `CurrentCCService` property sets or retrieves the current closed captioning service.</span></span>

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a><span data-ttu-id="87200-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87200-107">Return Value</span></span>

<span data-ttu-id="87200-108">Restituisce un valore integer che indica il tipo di servizio di didascalia chiuso abilitato.</span><span class="sxs-lookup"><span data-stu-id="87200-108">Returns an integer value indicating the type of closed captioning service enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="87200-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="87200-109">Remarks</span></span>

<span data-ttu-id="87200-110">I valori possibili di questa proprietà sono:</span><span class="sxs-lookup"><span data-stu-id="87200-110">The possible values of this property are:</span></span>



| <span data-ttu-id="87200-111">Valore</span><span class="sxs-lookup"><span data-stu-id="87200-111">Value</span></span> | <span data-ttu-id="87200-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87200-112">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="87200-113">0x0</span><span class="sxs-lookup"><span data-stu-id="87200-113">0x0</span></span>   | <span data-ttu-id="87200-114">Nessun servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="87200-114">No current service.</span></span> <span data-ttu-id="87200-115">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="87200-115">This is the default value.</span></span>                       |
| <span data-ttu-id="87200-116">0x1</span><span class="sxs-lookup"><span data-stu-id="87200-116">0x1</span></span>   | <span data-ttu-id="87200-117">Didascalia vera, primo campo.</span><span class="sxs-lookup"><span data-stu-id="87200-117">True captioning, first field.</span></span> <span data-ttu-id="87200-118">Servizio predefinito.</span><span class="sxs-lookup"><span data-stu-id="87200-118">Default service.</span></span>                       |
| <span data-ttu-id="87200-119">0x2</span><span class="sxs-lookup"><span data-stu-id="87200-119">0x2</span></span>   | <span data-ttu-id="87200-120">Didascalia per lingua secondaria, secondo campo.</span><span class="sxs-lookup"><span data-stu-id="87200-120">Captioning for secondary language, second field.</span></span> <span data-ttu-id="87200-121">Generalmente non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="87200-121">Generally not used.</span></span> |



 

<span data-ttu-id="87200-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="87200-122">This property is read/write.</span></span>

## <a name="see-also"></a><span data-ttu-id="87200-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87200-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87200-124">**CCActive**</span><span class="sxs-lookup"><span data-stu-id="87200-124">**CCActive**</span></span>](ccactive-property.md)
</dt> </dl>

 

 




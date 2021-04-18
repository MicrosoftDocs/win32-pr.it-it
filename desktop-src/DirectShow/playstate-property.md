---
description: La proprietà riproduzione recupera lo stato corrente dell'oggetto MSWebDVD.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Proprietà riproduzione
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8c699ce3f232f9afc14472f0308fa65adc6abb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303985"
---
# <a name="playstate-property"></a><span data-ttu-id="954ba-103">Proprietà riproduzione</span><span class="sxs-lookup"><span data-stu-id="954ba-103">PlayState Property</span></span>

> [!Note]  
> <span data-ttu-id="954ba-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="954ba-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="954ba-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="954ba-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="954ba-106">La `PlayState` proprietà recupera lo stato corrente dell'oggetto **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="954ba-106">The `PlayState` property retrieves the current state of the **MSWebDVD** object.</span></span>

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a><span data-ttu-id="954ba-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="954ba-107">Return Value</span></span>

<span data-ttu-id="954ba-108">Restituisce un valore intero che rappresenta lo stato corrente del navigatore DVD.</span><span class="sxs-lookup"><span data-stu-id="954ba-108">Returns an Integer value representing the current state of the DVD Navigator.</span></span>



| <span data-ttu-id="954ba-109">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="954ba-109">Return code</span></span> | <span data-ttu-id="954ba-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="954ba-110">Description</span></span>   |
|-------------|---------------|
| <span data-ttu-id="954ba-111">-2</span><span class="sxs-lookup"><span data-stu-id="954ba-111">-2</span></span>          | <span data-ttu-id="954ba-112">Non definito</span><span class="sxs-lookup"><span data-stu-id="954ba-112">Undefined</span></span>     |
| <span data-ttu-id="954ba-113">-1</span><span class="sxs-lookup"><span data-stu-id="954ba-113">-1</span></span>          | <span data-ttu-id="954ba-114">Inizializzazione annullata</span><span class="sxs-lookup"><span data-stu-id="954ba-114">Uninitialized</span></span> |
| <span data-ttu-id="954ba-115">0</span><span class="sxs-lookup"><span data-stu-id="954ba-115">0</span></span>           | <span data-ttu-id="954ba-116">Arrestato</span><span class="sxs-lookup"><span data-stu-id="954ba-116">Stopped</span></span>       |
| <span data-ttu-id="954ba-117">1</span><span class="sxs-lookup"><span data-stu-id="954ba-117">1</span></span>           | <span data-ttu-id="954ba-118">Paused</span><span class="sxs-lookup"><span data-stu-id="954ba-118">Paused</span></span>        |
| <span data-ttu-id="954ba-119">2</span><span class="sxs-lookup"><span data-stu-id="954ba-119">2</span></span>           | <span data-ttu-id="954ba-120">In esecuzione</span><span class="sxs-lookup"><span data-stu-id="954ba-120">Running</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="954ba-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="954ba-121">Remarks</span></span>

<span data-ttu-id="954ba-122">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="954ba-122">This property is read-only with no default value.</span></span>

<span data-ttu-id="954ba-123">L'oggetto **mswebdvd** controlla il filtro del navigatore DirectShow DVD, che esegue il lavoro effettivo della navigazione in DVD.</span><span class="sxs-lookup"><span data-stu-id="954ba-123">The **MSWebDVD** object controls the DirectShow DVD Navigator filter, which does the actual work of DVD navigation.</span></span> <span data-ttu-id="954ba-124">Si tratta in realtà dello stato del navigatore DVD a cui questa proprietà fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="954ba-124">It is actually the state of the DVD Navigator that this property refers to.</span></span> <span data-ttu-id="954ba-125">Il navigatore DVD può trovarsi in uno dei diversi Stati, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="954ba-125">The DVD Navigator can be in one of several states, as described above.</span></span> <span data-ttu-id="954ba-126">La `PlayState` proprietà può essere utile come strumento di diagnostica, ma in genere non dovrebbe essere necessario che un'applicazione di scripting monitori lo stato del navigatore DVD.</span><span class="sxs-lookup"><span data-stu-id="954ba-126">The `PlayState` property can be useful as a diagnostic tool, but generally there should be no reason for a scripting application to monitor the state of the DVD Navigator.</span></span>

 

 




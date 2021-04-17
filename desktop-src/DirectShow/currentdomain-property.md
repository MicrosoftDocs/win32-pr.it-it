---
description: La proprietà CurrentDomain Recupera il dominio DVD in cui si trova l'oggetto MSWebDVD.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: Proprietà CurrentDomain
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead6d61cd622fceac2a4d133a0297892992e763a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481861"
---
# <a name="currentdomain-property"></a><span data-ttu-id="84761-103">Proprietà CurrentDomain</span><span class="sxs-lookup"><span data-stu-id="84761-103">CurrentDomain Property</span></span>

> [!Note]  
> <span data-ttu-id="84761-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="84761-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="84761-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="84761-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="84761-106">La `CurrentDomain` proprietà recupera il dominio DVD in cui si trova l'oggetto mswebdvd.</span><span class="sxs-lookup"><span data-stu-id="84761-106">The `CurrentDomain` property retrieves the DVD domain that the MSWebDVD object is in.</span></span>

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a><span data-ttu-id="84761-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84761-107">Return Value</span></span>

<span data-ttu-id="84761-108">Restituisce un valore intero che rappresenta il dominio corrente.</span><span class="sxs-lookup"><span data-stu-id="84761-108">Returns an integer value representing the current domain.</span></span>

## <a name="remarks"></a><span data-ttu-id="84761-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="84761-109">Remarks</span></span>

<span data-ttu-id="84761-110">I valori possibili della proprietà sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="84761-110">The possible values of the property are:</span></span>



| <span data-ttu-id="84761-111">Valore</span><span class="sxs-lookup"><span data-stu-id="84761-111">Value</span></span> | <span data-ttu-id="84761-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84761-112">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="84761-113">1</span><span class="sxs-lookup"><span data-stu-id="84761-113">1</span></span>     | <span data-ttu-id="84761-114">Prima riproduzione</span><span class="sxs-lookup"><span data-stu-id="84761-114">First play</span></span>           |
| <span data-ttu-id="84761-115">2</span><span class="sxs-lookup"><span data-stu-id="84761-115">2</span></span>     | <span data-ttu-id="84761-116">Menu di gestione video</span><span class="sxs-lookup"><span data-stu-id="84761-116">Video Manager Menu</span></span>   |
| <span data-ttu-id="84761-117">3</span><span class="sxs-lookup"><span data-stu-id="84761-117">3</span></span>     | <span data-ttu-id="84761-118">Menu set del titolo del video</span><span class="sxs-lookup"><span data-stu-id="84761-118">Video Title Set Menu</span></span> |
| <span data-ttu-id="84761-119">4</span><span class="sxs-lookup"><span data-stu-id="84761-119">4</span></span>     | <span data-ttu-id="84761-120">Titolo</span><span class="sxs-lookup"><span data-stu-id="84761-120">Title</span></span>                |
| <span data-ttu-id="84761-121">5</span><span class="sxs-lookup"><span data-stu-id="84761-121">5</span></span>     | <span data-ttu-id="84761-122">Interrompere</span><span class="sxs-lookup"><span data-stu-id="84761-122">Stop</span></span>                 |



 

<span data-ttu-id="84761-123">Chiamare questo metodo per assicurarsi che il navigatore DVD si trovi in un dominio valido per il metodo che si sta per chiamare.</span><span class="sxs-lookup"><span data-stu-id="84761-123">Call this method to ensure that the DVD Navigator is in a valid domain for the method you are about to call.</span></span> <span data-ttu-id="84761-124">Ad esempio, prima di chiamare [**PlayTitle**](playtitle-method.md), controllare la `CurrentDomain` proprietà per verificare che il navigatore DVD non sia presente nel dominio stop o First Play.</span><span class="sxs-lookup"><span data-stu-id="84761-124">For example, before calling [**PlayTitle**](playtitle-method.md), check the `CurrentDomain` property to make sure that the DVD Navigator is not in the Stop or First Play domain.</span></span>

 

 




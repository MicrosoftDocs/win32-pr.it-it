---
description: Il metodo GetTitleParentalLevels recupera i livelli di gestione padre per il titolo specificato.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: Metodo GetTitleParentalLevels
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db82ca21c2fdd023aa472e4c3428260464a8612
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401210"
---
# <a name="gettitleparentallevels-method"></a><span data-ttu-id="3d0e5-103">Metodo GetTitleParentalLevels</span><span class="sxs-lookup"><span data-stu-id="3d0e5-103">GetTitleParentalLevels Method</span></span>

> [!Note]  
> <span data-ttu-id="3d0e5-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3d0e5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="3d0e5-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="3d0e5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="3d0e5-106">Il `GetTitleParentalLevels` metodo recupera i livelli di gestione padre per il titolo specificato.</span><span class="sxs-lookup"><span data-stu-id="3d0e5-106">The `GetTitleParentalLevels` method retrieves the parental management levels for the specified title.</span></span>

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a><span data-ttu-id="3d0e5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d0e5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d0e5-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="3d0e5-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="3d0e5-109">Specifica il titolo come intero.</span><span class="sxs-lookup"><span data-stu-id="3d0e5-109">Specifies the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d0e5-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d0e5-110">Return Value</span></span>

<span data-ttu-id="3d0e5-111">Restituisce un valore intero i cui singoli bit indicano i livelli di gestione padre (PML) impostati nel titolo specificato.</span><span class="sxs-lookup"><span data-stu-id="3d0e5-111">Returns an integer value whose individual bits indicate which parental management levels (PML) are set in the specified title.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d0e5-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d0e5-112">Remarks</span></span>

<span data-ttu-id="3d0e5-113">Un titolo può includere capitoli o segmenti brevi che hanno un PML diverso dal totale di PML per il titolo.</span><span class="sxs-lookup"><span data-stu-id="3d0e5-113">A title may have chapters or even short segments that have a PML different from the overall PML for the title.</span></span> <span data-ttu-id="3d0e5-114">Utilizzare questo metodo per determinare tutti gli PMLs che verranno rilevati durante la riproduzione di un titolo specificato.</span><span class="sxs-lookup"><span data-stu-id="3d0e5-114">Use this method to determine all the PMLs that will be encountered when playing a specified title.</span></span> <span data-ttu-id="3d0e5-115">Il numero intero restituito è un set di flag di bit definiti come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3d0e5-115">The returned integer is a set of bit flags that are defined as shown in the table below.</span></span> <span data-ttu-id="3d0e5-116">Eseguire un'operazione con AND bit per bit su *iLevels* e ogni valore possibile.</span><span class="sxs-lookup"><span data-stu-id="3d0e5-116">Perform a bitwise AND operation on *iLevels* and each possible value.</span></span> <span data-ttu-id="3d0e5-117">Se l'operazione restituisce **true**, il valore PML verrà rilevato in un determinato punto del titolo.</span><span class="sxs-lookup"><span data-stu-id="3d0e5-117">If the operation returns **true**, it means that PML will be encountered at some point in this title.</span></span>



| <span data-ttu-id="3d0e5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3d0e5-118">Value</span></span>  | <span data-ttu-id="3d0e5-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d0e5-119">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="3d0e5-120">0x100</span><span class="sxs-lookup"><span data-stu-id="3d0e5-120">0x100</span></span>  | <span data-ttu-id="3d0e5-121">Livello padre 1 DVD</span><span class="sxs-lookup"><span data-stu-id="3d0e5-121">DVD Parental Level 1</span></span> |
| <span data-ttu-id="3d0e5-122">0x200</span><span class="sxs-lookup"><span data-stu-id="3d0e5-122">0x200</span></span>  | <span data-ttu-id="3d0e5-123">Livello parentale DVD 2</span><span class="sxs-lookup"><span data-stu-id="3d0e5-123">DVD Parental Level 2</span></span> |
| <span data-ttu-id="3d0e5-124">0x400</span><span class="sxs-lookup"><span data-stu-id="3d0e5-124">0x400</span></span>  | <span data-ttu-id="3d0e5-125">Livello parentale DVD 3</span><span class="sxs-lookup"><span data-stu-id="3d0e5-125">DVD Parental Level 3</span></span> |
| <span data-ttu-id="3d0e5-126">0x800</span><span class="sxs-lookup"><span data-stu-id="3d0e5-126">0x800</span></span>  | <span data-ttu-id="3d0e5-127">Livello parentale DVD 4</span><span class="sxs-lookup"><span data-stu-id="3d0e5-127">DVD Parental Level 4</span></span> |
| <span data-ttu-id="3d0e5-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="3d0e5-128">0x1000</span></span> | <span data-ttu-id="3d0e5-129">Livello parentale DVD 5</span><span class="sxs-lookup"><span data-stu-id="3d0e5-129">DVD Parental Level 5</span></span> |
| <span data-ttu-id="3d0e5-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="3d0e5-130">0x2000</span></span> | <span data-ttu-id="3d0e5-131">DVD padre livello 6</span><span class="sxs-lookup"><span data-stu-id="3d0e5-131">DVD Parental Level 6</span></span> |
| <span data-ttu-id="3d0e5-132">0x4000</span><span class="sxs-lookup"><span data-stu-id="3d0e5-132">0x4000</span></span> | <span data-ttu-id="3d0e5-133">Livello parentale DVD 7</span><span class="sxs-lookup"><span data-stu-id="3d0e5-133">DVD Parental Level 7</span></span> |
| <span data-ttu-id="3d0e5-134">0x8000</span><span class="sxs-lookup"><span data-stu-id="3d0e5-134">0x8000</span></span> | <span data-ttu-id="3d0e5-135">Livello parentale DVD 8</span><span class="sxs-lookup"><span data-stu-id="3d0e5-135">DVD Parental Level 8</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="3d0e5-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d0e5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d0e5-137">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="3d0e5-137">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="3d0e5-138">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="3d0e5-138">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="3d0e5-139">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="3d0e5-139">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="3d0e5-140">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="3d0e5-140">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 




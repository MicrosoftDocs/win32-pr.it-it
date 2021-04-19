---
title: Proprietà di dominio IWMPDVD
description: La proprietà del dominio ottiene il dominio corrente del DVD.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- Proprietà del dominio Media Player Windows
- Proprietà del dominio Media Player Windows, interfaccia IWMPDVD
- Interfaccia IWMPDVD Windows Media Player, proprietà del dominio
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332449"
---
# <a name="iwmpdvddomain-property"></a><span data-ttu-id="02f8f-106">IWMPDVD::d proprietà ominio</span><span class="sxs-lookup"><span data-stu-id="02f8f-106">IWMPDVD::domain property</span></span>

<span data-ttu-id="02f8f-107">La proprietà del **dominio** ottiene il dominio corrente del DVD.</span><span class="sxs-lookup"><span data-stu-id="02f8f-107">The **domain** property gets the current domain of the DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f8f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02f8f-108">Syntax</span></span>


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a><span data-ttu-id="02f8f-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="02f8f-109">Property value</span></span>

<span data-ttu-id="02f8f-110">**System. String** che corrisponde a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="02f8f-110">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="02f8f-111">Valore</span><span class="sxs-lookup"><span data-stu-id="02f8f-111">Value</span></span>                                                                                        | <span data-ttu-id="02f8f-112">Significato</span><span class="sxs-lookup"><span data-stu-id="02f8f-112">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02f8f-113"><dt>firstPlay</dt></span><span class="sxs-lookup"><span data-stu-id="02f8f-113"><dt>firstPlay</dt></span></span> </dl>         | <span data-ttu-id="02f8f-114">Esecuzione dell'inizializzazione predefinita di un disco DVD.</span><span class="sxs-lookup"><span data-stu-id="02f8f-114">Performing default initialization of a DVD disc.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="02f8f-115"><dt>videoManagerMenu</dt></span><span class="sxs-lookup"><span data-stu-id="02f8f-115"><dt>videoManagerMenu</dt></span></span> </dl>  | <span data-ttu-id="02f8f-116">Visualizzazione dei menu per l'intero disco. Noto anche come menu di scelta rapida per Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="02f8f-116">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="02f8f-117">Comunemente chiamato menu titolo o menu in alto.</span><span class="sxs-lookup"><span data-stu-id="02f8f-117">Commonly called the title menu or the top menu.</span></span><br/> |
| <dl> <span data-ttu-id="02f8f-118"><dt>videoTitleSetMenu</dt></span><span class="sxs-lookup"><span data-stu-id="02f8f-118"><dt>videoTitleSetMenu</dt></span></span> </dl> | <span data-ttu-id="02f8f-119">Visualizzazione dei menu per il set di titoli corrente.</span><span class="sxs-lookup"><span data-stu-id="02f8f-119">Displaying menus for the current title set.</span></span> <span data-ttu-id="02f8f-120">Noto anche come titleMenu per Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="02f8f-120">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="02f8f-121">Comunemente chiamato menu radice.</span><span class="sxs-lookup"><span data-stu-id="02f8f-121">Commonly called the root menu.</span></span><br/>          |
| <dl> <span data-ttu-id="02f8f-122"><dt>title</dt></span><span class="sxs-lookup"><span data-stu-id="02f8f-122"><dt>title</dt></span></span> </dl>             | <span data-ttu-id="02f8f-123">In genere, viene visualizzato il titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="02f8f-123">Usually, displaying the current title.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="02f8f-124"><dt>stop</dt></span><span class="sxs-lookup"><span data-stu-id="02f8f-124"><dt>stop</dt></span></span> </dl>              | <span data-ttu-id="02f8f-125">Il navigatore DVD si trova nel dominio di arresto DVD.</span><span class="sxs-lookup"><span data-stu-id="02f8f-125">The DVD Navigator is in the DVD Stop domain.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="02f8f-126"><dt>non definito</dt></span><span class="sxs-lookup"><span data-stu-id="02f8f-126"><dt>undefined</dt></span></span> </dl>         | <span data-ttu-id="02f8f-127">Windows Media Player non è in alcun dominio DVD.</span><span class="sxs-lookup"><span data-stu-id="02f8f-127">Windows Media Player is not in any DVD domain.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="02f8f-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="02f8f-128">Remarks</span></span>

<span data-ttu-id="02f8f-129">Ogni DVD viene creato in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="02f8f-129">Every DVD is authored differently.</span></span> <span data-ttu-id="02f8f-130">Alcuni DVD non contengono i domini firstPlay, videoManagerMenu o videoTitleSetMenu.</span><span class="sxs-lookup"><span data-stu-id="02f8f-130">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f8f-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02f8f-131">Requirements</span></span>



| <span data-ttu-id="02f8f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="02f8f-132">Requirement</span></span> | <span data-ttu-id="02f8f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="02f8f-133">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02f8f-134">Versione</span><span class="sxs-lookup"><span data-stu-id="02f8f-134">Version</span></span><br/>   | <span data-ttu-id="02f8f-135">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="02f8f-135">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="02f8f-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="02f8f-136">Namespace</span></span><br/> | <span data-ttu-id="02f8f-137">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="02f8f-137">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="02f8f-138">Assembly</span><span class="sxs-lookup"><span data-stu-id="02f8f-138">Assembly</span></span><br/>  | <dl> <span data-ttu-id="02f8f-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="02f8f-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02f8f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02f8f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f8f-141">**Interfaccia IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="02f8f-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 






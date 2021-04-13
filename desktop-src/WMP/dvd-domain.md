---
title: DVD. dominio
description: La proprietà del dominio recupera il dominio corrente del DVD.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD. dominio Windows Media Player
topic_type:
- apiref
api_name:
- DVD.domain
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4a2af92abe533fed7a13e48cb7c0724223bbc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340593"
---
# <a name="dvddomain"></a><span data-ttu-id="ad5ef-104">DVD. dominio</span><span class="sxs-lookup"><span data-stu-id="ad5ef-104">DVD.domain</span></span>

<span data-ttu-id="ad5ef-105">La proprietà del **dominio** Recupera il dominio corrente del DVD.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-105">The **domain** property retrieves the current domain of the DVD.</span></span>

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a><span data-ttu-id="ad5ef-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="ad5ef-106">Possible Values</span></span>

<span data-ttu-id="ad5ef-107">Questa proprietà è una **stringa** di sola lettura contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-107">This property is a read-only **String** containing one of the following values.</span></span>



| <span data-ttu-id="ad5ef-108">string</span><span class="sxs-lookup"><span data-stu-id="ad5ef-108">String</span></span>            | <span data-ttu-id="ad5ef-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad5ef-109">Description</span></span>                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad5ef-110">firstPlay</span><span class="sxs-lookup"><span data-stu-id="ad5ef-110">firstPlay</span></span>         | <span data-ttu-id="ad5ef-111">Esecuzione dell'inizializzazione predefinita di un disco DVD.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-111">Performing default initialization of a DVD disc.</span></span>                                                                                      |
| <span data-ttu-id="ad5ef-112">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="ad5ef-112">videoManagerMenu</span></span>  | <span data-ttu-id="ad5ef-113">Visualizzazione dei menu per l'intero disco. Noto anche come menu di scelta rapida per Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-113">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="ad5ef-114">Comunemente chiamato menu titolo o menu in alto.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-114">Commonly called the title menu or the top menu.</span></span> |
| <span data-ttu-id="ad5ef-115">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="ad5ef-115">videoTitleSetMenu</span></span> | <span data-ttu-id="ad5ef-116">Visualizzazione dei menu per il set di titoli corrente.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-116">Displaying menus for current title set.</span></span> <span data-ttu-id="ad5ef-117">Noto anche come titleMenu per Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-117">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="ad5ef-118">Comunemente chiamato menu radice.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-118">Commonly called the root menu.</span></span>              |
| <span data-ttu-id="ad5ef-119">title</span><span class="sxs-lookup"><span data-stu-id="ad5ef-119">title</span></span>             | <span data-ttu-id="ad5ef-120">In genere viene visualizzato il titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-120">Usually displaying the current title.</span></span>                                                                                                 |
| <span data-ttu-id="ad5ef-121">stop</span><span class="sxs-lookup"><span data-stu-id="ad5ef-121">stop</span></span>              | <span data-ttu-id="ad5ef-122">Il navigatore DVD si trova nel dominio di arresto DVD.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-122">The DVD Navigator is in the DVD Stop domain.</span></span>                                                                                          |
| <span data-ttu-id="ad5ef-123">Non definito</span><span class="sxs-lookup"><span data-stu-id="ad5ef-123">undefined</span></span>         | <span data-ttu-id="ad5ef-124">Il lettore non è in nessun dominio DVD.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-124">Player is not in any DVD domain.</span></span>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="ad5ef-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad5ef-125">Remarks</span></span>

<span data-ttu-id="ad5ef-126">Ogni DVD viene creato in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-126">Every DVD is authored differently.</span></span> <span data-ttu-id="ad5ef-127">Alcuni DVD non contengono i domini firstPlay, videoManagerMenu o videoTitleSetMenu.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-127">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

<span data-ttu-id="ad5ef-128">**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="ad5ef-128">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad5ef-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad5ef-129">Requirements</span></span>



| <span data-ttu-id="ad5ef-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad5ef-130">Requirement</span></span> | <span data-ttu-id="ad5ef-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ad5ef-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad5ef-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad5ef-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ad5ef-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ad5ef-133">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ad5ef-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad5ef-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ad5ef-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ad5ef-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ad5ef-136">Versione</span><span class="sxs-lookup"><span data-stu-id="ad5ef-136">Version</span></span><br/>                  | <span data-ttu-id="ad5ef-137">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ad5ef-137">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="ad5ef-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ad5ef-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad5ef-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad5ef-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad5ef-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad5ef-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad5ef-141">**Oggetto DVD**</span><span class="sxs-lookup"><span data-stu-id="ad5ef-141">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 






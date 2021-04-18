---
title: Funzioni di controllo
description: Funzioni di controllo
ms.assetid: 9774a320-1d00-48a4-ba13-fb1cd683a635
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7099afab5c035e394eafc30c4475dbe6bc97cec5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321965"
---
# <a name="control-functions"></a><span data-ttu-id="12cb0-103">Funzioni di controllo</span><span class="sxs-lookup"><span data-stu-id="12cb0-103">Control Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="12cb0-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="12cb0-104">In This Section</span></span>

-   [<span data-ttu-id="12cb0-105">**DoReaderMode**</span><span class="sxs-lookup"><span data-stu-id="12cb0-105">**DoReaderMode**</span></span>](doreadermode.md)
-   [<span data-ttu-id="12cb0-106">**\_Clone DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-106">**DPA\_Clone**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_clone)
-   [<span data-ttu-id="12cb0-107">**\_Creazione DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-107">**DPA\_Create**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_create)
-   [<span data-ttu-id="12cb0-108">**\_CREATEEX DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-108">**DPA\_CreateEx**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_createex)
-   [<span data-ttu-id="12cb0-109">**\_DELETEALLPTRS DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-109">**DPA\_DeleteAllPtrs**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_deleteallptrs)
-   [<span data-ttu-id="12cb0-110">**\_DELETEPTR DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-110">**DPA\_DeletePtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_deleteptr)
-   [<span data-ttu-id="12cb0-111">**Eliminazione del DPA \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-111">**DPA\_Destroy**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_destroy)
-   [<span data-ttu-id="12cb0-112">**\_DESTROYCALLBACK DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-112">**DPA\_DestroyCallback**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_destroycallback)
-   [<span data-ttu-id="12cb0-113">**\_ENUMCALLBACK DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-113">**DPA\_EnumCallback**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_enumcallback)
-   [<span data-ttu-id="12cb0-114">**\_GETPTR DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-114">**DPA\_GetPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getptr)
-   [<span data-ttu-id="12cb0-115">**\_GETPTRINDEX DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-115">**DPA\_GetPtrIndex**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getptrindex)
-   [<span data-ttu-id="12cb0-116">**GetSize DPA \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-116">**DPA\_GetSize**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getsize)
-   [<span data-ttu-id="12cb0-117">**Aumento del DPA \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-117">**DPA\_Grow**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_grow)
-   [<span data-ttu-id="12cb0-118">**\_INSERTPTR DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-118">**DPA\_InsertPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_insertptr)
-   [<span data-ttu-id="12cb0-119">**\_LOADSTREAM DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-119">**DPA\_LoadStream**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_loadstream)
-   [<span data-ttu-id="12cb0-120">**\_Unione DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-120">**DPA\_Merge**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_merge)
-   [<span data-ttu-id="12cb0-121">**\_SAVESTREAM DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-121">**DPA\_SaveStream**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_savestream)
-   [<span data-ttu-id="12cb0-122">**\_Ricerca DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-122">**DPA\_Search**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_search)
-   [<span data-ttu-id="12cb0-123">**\_SETPTR DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-123">**DPA\_SetPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_setptr)
-   [<span data-ttu-id="12cb0-124">**\_Ordinamento DPA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-124">**DPA\_Sort**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_sort)
-   [<span data-ttu-id="12cb0-125">**DrawShadowText**</span><span class="sxs-lookup"><span data-stu-id="12cb0-125">**DrawShadowText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-drawshadowtext)
-   [<span data-ttu-id="12cb0-126">**DrawTextExPrivWrap**</span><span class="sxs-lookup"><span data-stu-id="12cb0-126">**DrawTextExPrivWrap**</span></span>](drawtextexprivwrap.md)
-   [<span data-ttu-id="12cb0-127">**DrawTextWrap**</span><span class="sxs-lookup"><span data-stu-id="12cb0-127">**DrawTextWrap**</span></span>](drawtextwrap.md)
-   [<span data-ttu-id="12cb0-128">**\_Clone DSA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-128">**DSA\_Clone**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_clone)
-   [<span data-ttu-id="12cb0-129">**Creazione di DSA \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-129">**DSA\_Create**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_create)
-   [<span data-ttu-id="12cb0-130">**\_DELETEALLITEMS DSA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-130">**DSA\_DeleteAllItems**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_deleteallitems)
-   [<span data-ttu-id="12cb0-131">**\_DeleteItem DSA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-131">**DSA\_DeleteItem**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_deleteitem)
-   [<span data-ttu-id="12cb0-132">**\_Distruzione DSA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-132">**DSA\_Destroy**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_destroy)
-   [<span data-ttu-id="12cb0-133">**\_DESTROYCALLBACK DSA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-133">**DSA\_DestroyCallback**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_destroycallback)
-   [<span data-ttu-id="12cb0-134">**\_ENUMCALLBACK DSA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-134">**DSA\_EnumCallback**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_enumcallback)
-   [<span data-ttu-id="12cb0-135">**DSA \_ GetItem**</span><span class="sxs-lookup"><span data-stu-id="12cb0-135">**DSA\_GetItem**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getitem)
-   [<span data-ttu-id="12cb0-136">**\_GETITEMPTR DSA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-136">**DSA\_GetItemPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getitemptr)
-   [<span data-ttu-id="12cb0-137">**DSA \_ GetSize**</span><span class="sxs-lookup"><span data-stu-id="12cb0-137">**DSA\_GetSize**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getsize)
-   [<span data-ttu-id="12cb0-138">**InsertItem (DSA) \_**</span><span class="sxs-lookup"><span data-stu-id="12cb0-138">**DSA\_InsertItem**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_insertitem)
-   [<span data-ttu-id="12cb0-139">**\_Elemento DSA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-139">**DSA\_SetItem**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_setitem)
-   [<span data-ttu-id="12cb0-140">**\_Ordinamento DSA**</span><span class="sxs-lookup"><span data-stu-id="12cb0-140">**DSA\_Sort**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_sort)
-   [<span data-ttu-id="12cb0-141">**ExtTextOutWrap**</span><span class="sxs-lookup"><span data-stu-id="12cb0-141">**ExtTextOutWrap**</span></span>](exttextoutwrap.md)
-   [<span data-ttu-id="12cb0-142">**GetEffectiveClientRect**</span><span class="sxs-lookup"><span data-stu-id="12cb0-142">**GetEffectiveClientRect**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-geteffectiveclientrect)
-   [<span data-ttu-id="12cb0-143">**GetMUILanguage**</span><span class="sxs-lookup"><span data-stu-id="12cb0-143">**GetMUILanguage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage)
-   [<span data-ttu-id="12cb0-144">**GetTextExtentPoint32Wrap**</span><span class="sxs-lookup"><span data-stu-id="12cb0-144">**GetTextExtentPoint32Wrap**</span></span>](gettextextentpoint32wrap.md)
-   [<span data-ttu-id="12cb0-145">**InitCommonControls**</span><span class="sxs-lookup"><span data-stu-id="12cb0-145">**InitCommonControls**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)
-   [<span data-ttu-id="12cb0-146">**InitCommonControlsEx**</span><span class="sxs-lookup"><span data-stu-id="12cb0-146">**InitCommonControlsEx**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)
-   [<span data-ttu-id="12cb0-147">**InitMUILanguage**</span><span class="sxs-lookup"><span data-stu-id="12cb0-147">**InitMUILanguage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage)
-   [<span data-ttu-id="12cb0-148">**LoadIconMetric**</span><span class="sxs-lookup"><span data-stu-id="12cb0-148">**LoadIconMetric**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-loadiconmetric)
-   [<span data-ttu-id="12cb0-149">**LoadIconWithScaleDown**</span><span class="sxs-lookup"><span data-stu-id="12cb0-149">**LoadIconWithScaleDown**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-loadiconwithscaledown)
-   [<span data-ttu-id="12cb0-150">**MirrorIcon**</span><span class="sxs-lookup"><span data-stu-id="12cb0-150">**MirrorIcon**</span></span>](mirroricon.md)
-   [<span data-ttu-id="12cb0-151">**PFNDACOMPARE**</span><span class="sxs-lookup"><span data-stu-id="12cb0-151">**PFNDACOMPARE**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare)
-   [<span data-ttu-id="12cb0-152">**PFNDACOMPARECONST**</span><span class="sxs-lookup"><span data-stu-id="12cb0-152">**PFNDACOMPARECONST**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompareconst)
-   [<span data-ttu-id="12cb0-153">**PFNDAENUMCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="12cb0-153">**PFNDAENUMCALLBACK**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallback)
-   [<span data-ttu-id="12cb0-154">**PFNDAENUMCALLBACKCONST**</span><span class="sxs-lookup"><span data-stu-id="12cb0-154">**PFNDAENUMCALLBACKCONST**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallbackconst)
-   <span data-ttu-id="12cb0-155">[**PFNDPACOMPARE**](/previous-versions/windows/desktop/legacy/bb775715(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="12cb0-155">[**PFNDPACOMPARE**](/previous-versions/windows/desktop/legacy/bb775715(v=vs.85))</span></span>
-   <span data-ttu-id="12cb0-156">[**PFNDPACOMPARECONST**](/previous-versions/windows/desktop/legacy/bb775717(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="12cb0-156">[**PFNDPACOMPARECONST**](/previous-versions/windows/desktop/legacy/bb775717(v=vs.85))</span></span>
-   <span data-ttu-id="12cb0-157">[**PFNDPAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775719(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="12cb0-157">[**PFNDPAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775719(v=vs.85))</span></span>
-   [<span data-ttu-id="12cb0-158">**PFNDPAMERGE**</span><span class="sxs-lookup"><span data-stu-id="12cb0-158">**PFNDPAMERGE**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamerge)
-   [<span data-ttu-id="12cb0-159">**PFNDPAMERGECONST**</span><span class="sxs-lookup"><span data-stu-id="12cb0-159">**PFNDPAMERGECONST**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamergeconst)
-   [<span data-ttu-id="12cb0-160">**PFNDPASTREAM**</span><span class="sxs-lookup"><span data-stu-id="12cb0-160">**PFNDPASTREAM**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpastream)
-   <span data-ttu-id="12cb0-161">[**PFNDSAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="12cb0-161">[**PFNDSAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775727(v=vs.85))</span></span>
-   [<span data-ttu-id="12cb0-162">**ReaderScroll**</span><span class="sxs-lookup"><span data-stu-id="12cb0-162">**ReaderScroll**</span></span>](readerscroll.md)
-   [<span data-ttu-id="12cb0-163">**ShowHideMenuCtl**</span><span class="sxs-lookup"><span data-stu-id="12cb0-163">**ShowHideMenuCtl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-showhidemenuctl)
-   [<span data-ttu-id="12cb0-164">**\_Getptr Str**</span><span class="sxs-lookup"><span data-stu-id="12cb0-164">**Str\_GetPtr**</span></span>](str-getptr.md)
-   [<span data-ttu-id="12cb0-165">**\_SetPtr Str**</span><span class="sxs-lookup"><span data-stu-id="12cb0-165">**Str\_SetPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-str_setptrw)
-   [<span data-ttu-id="12cb0-166">**TranslateDispatch**</span><span class="sxs-lookup"><span data-stu-id="12cb0-166">**TranslateDispatch**</span></span>](translatedispatch.md)

 

 

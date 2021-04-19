---
title: Funzioni (STG)
description: Le funzioni sono routine o subroutine che restituiscono un valore o valori specifici. Le funzioni di archiviazione strutturata sono descritte nelle sezioni seguenti.
ms.assetid: 5fbb05ae-594d-4fa5-97d2-a2371e94c054
keywords:
- Archiviazione strutturata Strctd STG, informazioni di riferimento, funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f49c091b5ba9619b649e620da7b436ebac4ccb
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334001"
---
# <a name="structured-storage-functions"></a><span data-ttu-id="b3746-105">Funzioni di archiviazione strutturate</span><span class="sxs-lookup"><span data-stu-id="b3746-105">Structured Storage functions</span></span>

<span data-ttu-id="b3746-106">Le funzioni sono routine o subroutine che restituiscono un valore o valori specifici.</span><span class="sxs-lookup"><span data-stu-id="b3746-106">Functions are routines or subroutines that return a specific value or values.</span></span> <span data-ttu-id="b3746-107">Le funzioni di archiviazione strutturata sono descritte nelle sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3746-107">Structured Storage functions are described in the following sections:</span></span>

-   [<span data-ttu-id="b3746-108">**CreateILockBytesOnHGlobal**</span><span class="sxs-lookup"><span data-stu-id="b3746-108">**CreateILockBytesOnHGlobal**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-createilockbytesonhglobal)
-   [<span data-ttu-id="b3746-109">**CreateStreamOnHGlobal**</span><span class="sxs-lookup"><span data-stu-id="b3746-109">**CreateStreamOnHGlobal**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
-   [<span data-ttu-id="b3746-110">**FmtIdToPropStgName**</span><span class="sxs-lookup"><span data-stu-id="b3746-110">**FmtIdToPropStgName**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-fmtidtopropstgname)
-   [<span data-ttu-id="b3746-111">**FreePropVariantArray**</span><span class="sxs-lookup"><span data-stu-id="b3746-111">**FreePropVariantArray**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [<span data-ttu-id="b3746-112">**GetConvertStg**</span><span class="sxs-lookup"><span data-stu-id="b3746-112">**GetConvertStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-getconvertstg)
-   [<span data-ttu-id="b3746-113">**GetHGlobalFromILockBytes**</span><span class="sxs-lookup"><span data-stu-id="b3746-113">**GetHGlobalFromILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-gethglobalfromilockbytes)
-   [<span data-ttu-id="b3746-114">**GetHGlobalFromStream**</span><span class="sxs-lookup"><span data-stu-id="b3746-114">**GetHGlobalFromStream**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-gethglobalfromstream)
-   [<span data-ttu-id="b3746-115">**OleConvertIStorageToOLESTREAM**</span><span class="sxs-lookup"><span data-stu-id="b3746-115">**OleConvertIStorageToOLESTREAM**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestream)
-   [<span data-ttu-id="b3746-116">**OleConvertIStorageToOLESTREAMEx**</span><span class="sxs-lookup"><span data-stu-id="b3746-116">**OleConvertIStorageToOLESTREAMEx**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestreamex)
-   [<span data-ttu-id="b3746-117">**OleConvertOLESTREAMToIStorage**</span><span class="sxs-lookup"><span data-stu-id="b3746-117">**OleConvertOLESTREAMToIStorage**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorage)
-   [<span data-ttu-id="b3746-118">**OleConvertOLESTREAMToIStorageEx**</span><span class="sxs-lookup"><span data-stu-id="b3746-118">**OleConvertOLESTREAMToIStorageEx**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorageex)
-   [<span data-ttu-id="b3746-119">**PropStgNameToFmtId**</span><span class="sxs-lookup"><span data-stu-id="b3746-119">**PropStgNameToFmtId**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-propstgnametofmtid)
-   [<span data-ttu-id="b3746-120">**PropVariantClear**</span><span class="sxs-lookup"><span data-stu-id="b3746-120">**PropVariantClear**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [<span data-ttu-id="b3746-121">**PropVariantCopy**</span><span class="sxs-lookup"><span data-stu-id="b3746-121">**PropVariantCopy**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)
-   [<span data-ttu-id="b3746-122">**PropVariantInit**</span><span class="sxs-lookup"><span data-stu-id="b3746-122">**PropVariantInit**</span></span>](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [<span data-ttu-id="b3746-123">**ReadClassStg**</span><span class="sxs-lookup"><span data-stu-id="b3746-123">**ReadClassStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-readclassstg)
-   [<span data-ttu-id="b3746-124">**ReadClassStm**</span><span class="sxs-lookup"><span data-stu-id="b3746-124">**ReadClassStm**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-readclassstm)
-   [<span data-ttu-id="b3746-125">**ReadFmtUserTypeStg**</span><span class="sxs-lookup"><span data-stu-id="b3746-125">**ReadFmtUserTypeStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg)
-   [<span data-ttu-id="b3746-126">**StgConvertPropertyToVariant**</span><span class="sxs-lookup"><span data-stu-id="b3746-126">**StgConvertPropertyToVariant**</span></span>](/windows/desktop/api/Propidl/nf-propidl-stgconvertpropertytovariant)
-   [<span data-ttu-id="b3746-127">**SetConvertStg**</span><span class="sxs-lookup"><span data-stu-id="b3746-127">**SetConvertStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-setconvertstg)
-   [<span data-ttu-id="b3746-128">**StgConvertVariantToProperty**</span><span class="sxs-lookup"><span data-stu-id="b3746-128">**StgConvertVariantToProperty**</span></span>](/windows/desktop/api/Propidl/nf-propidl-stgconvertvarianttoproperty)
-   [<span data-ttu-id="b3746-129">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="b3746-129">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
-   [<span data-ttu-id="b3746-130">**StgCreateDocfileOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="b3746-130">**StgCreateDocfileOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
-   [<span data-ttu-id="b3746-131">**StgCreatePropSetStg**</span><span class="sxs-lookup"><span data-stu-id="b3746-131">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
-   [<span data-ttu-id="b3746-132">**StgCreatePropStg**</span><span class="sxs-lookup"><span data-stu-id="b3746-132">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
-   [<span data-ttu-id="b3746-133">**StgCreateStorageEx**</span><span class="sxs-lookup"><span data-stu-id="b3746-133">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
-   [<span data-ttu-id="b3746-134">**StgDeserializePropVariant**</span><span class="sxs-lookup"><span data-stu-id="b3746-134">**StgDeserializePropVariant**</span></span>](/windows/desktop/api/Propvarutil/nf-propvarutil-stgdeserializepropvariant)
-   [<span data-ttu-id="b3746-135">**StgGetIFillLockBytesOnFile**</span><span class="sxs-lookup"><span data-stu-id="b3746-135">**StgGetIFillLockBytesOnFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile)
-   [<span data-ttu-id="b3746-136">**StgGetIFillLockBytesOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="b3746-136">**StgGetIFillLockBytesOnILockBytes**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes)
-   [<span data-ttu-id="b3746-137">**StgIsStorageFile**</span><span class="sxs-lookup"><span data-stu-id="b3746-137">**StgIsStorageFile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile)
-   [<span data-ttu-id="b3746-138">**StgIsStorageILockBytes**</span><span class="sxs-lookup"><span data-stu-id="b3746-138">**StgIsStorageILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgisstorageilockbytes)
-   [<span data-ttu-id="b3746-139">**StgOpenAsyncDocfileOnIFillLockBytes**</span><span class="sxs-lookup"><span data-stu-id="b3746-139">**StgOpenAsyncDocfileOnIFillLockBytes**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes)
-   [<span data-ttu-id="b3746-140">**StgOpenLayoutDocfile**</span><span class="sxs-lookup"><span data-stu-id="b3746-140">**StgOpenLayoutDocfile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stgopenlayoutdocfile)
-   [<span data-ttu-id="b3746-141">**StgOpenPropStg**</span><span class="sxs-lookup"><span data-stu-id="b3746-141">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
-   [<span data-ttu-id="b3746-142">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="b3746-142">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
-   [<span data-ttu-id="b3746-143">**StgOpenStorageEx**</span><span class="sxs-lookup"><span data-stu-id="b3746-143">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
-   [<span data-ttu-id="b3746-144">**StgOpenStorageOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="b3746-144">**StgOpenStorageOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
-   [<span data-ttu-id="b3746-145">**StgPropertyLengthAsVariant**</span><span class="sxs-lookup"><span data-stu-id="b3746-145">**StgPropertyLengthAsVariant**</span></span>](/windows/desktop/api/Propapi/nf-propapi-stgpropertylengthasvariant)
-   [<span data-ttu-id="b3746-146">**StgSerializePropVariant**</span><span class="sxs-lookup"><span data-stu-id="b3746-146">**StgSerializePropVariant**</span></span>](/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant)
-   [<span data-ttu-id="b3746-147">**StgSetTimes**</span><span class="sxs-lookup"><span data-stu-id="b3746-147">**StgSetTimes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgsettimes)
-   [<span data-ttu-id="b3746-148">**WriteClassStg**</span><span class="sxs-lookup"><span data-stu-id="b3746-148">**WriteClassStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg)
-   [<span data-ttu-id="b3746-149">**WriteClassStm**</span><span class="sxs-lookup"><span data-stu-id="b3746-149">**WriteClassStm**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-writeclassstm)
-   [<span data-ttu-id="b3746-150">**WriteFmtUserTypeStg**</span><span class="sxs-lookup"><span data-stu-id="b3746-150">**WriteFmtUserTypeStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg)

 

 

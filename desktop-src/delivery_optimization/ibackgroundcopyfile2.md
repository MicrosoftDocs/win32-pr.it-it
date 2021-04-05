---
title: Interfaccia IBackgroundCopyFile2 (Deliveryoptimization. h)
description: Usare l'interfaccia IBackgroundCopyFile2 per specificare un nuovo nome remoto per il file e recuperare l'elenco di intervalli da scaricare.
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- Interfaccia IBackgroundCopyFile2
- Interfaccia IBackgroundCopyFile2, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a866c8f18ee1dfb57f32ac3b2b9999e10106522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048276"
---
# <a name="ibackgroundcopyfile2-interface"></a><span data-ttu-id="2d2f9-105">Interfaccia IBackgroundCopyFile2</span><span class="sxs-lookup"><span data-stu-id="2d2f9-105">IBackgroundCopyFile2 interface</span></span>

<span data-ttu-id="2d2f9-106">Usare l'interfaccia **IBackgroundCopyFile2** per specificare un nuovo nome remoto per il file e recuperare l'elenco di intervalli da scaricare.</span><span class="sxs-lookup"><span data-stu-id="2d2f9-106">Use the **IBackgroundCopyFile2** interface to specify a new remote name for the file and retrieve the list of ranges to download.</span></span>

<span data-ttu-id="2d2f9-107">L'interfaccia **IBackgroundCopyFile2** eredita dall'interfaccia [**IBackgroundCopyFile**](ibackgroundcopyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="2d2f9-107">The **IBackgroundCopyFile2** interface inherits from the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface.</span></span>

<span data-ttu-id="2d2f9-108">Per ottenere un puntatore a interfaccia **IBackgroundCopyFile2** , chiamare il metodo **IBackgroundCopyFile:: QueryInterface** usando __uuidof (IBackgroundCopyFile2) per l'identificatore di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="2d2f9-108">To get an **IBackgroundCopyFile2** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile2) for the interface identifier.</span></span> <span data-ttu-id="2d2f9-109">Usare il puntatore all'interfaccia **IBackgroundCopyFile2** per chiamare entrambi i metodi [**IBackgroundCopyFile**](ibackgroundcopyfile.md) e **IBackgroundCopyFile2** .</span><span class="sxs-lookup"><span data-stu-id="2d2f9-109">Use the **IBackgroundCopyFile2** interface pointer to call both the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) and **IBackgroundCopyFile2** methods.</span></span>

## <a name="members"></a><span data-ttu-id="2d2f9-110">Membri</span><span class="sxs-lookup"><span data-stu-id="2d2f9-110">Members</span></span>

<span data-ttu-id="2d2f9-111">L'interfaccia **IBackgroundCopyFile2** eredita da [**IBackgroundCopyFile**](ibackgroundcopyfile.md).</span><span class="sxs-lookup"><span data-stu-id="2d2f9-111">The **IBackgroundCopyFile2** interface inherits from [**IBackgroundCopyFile**](ibackgroundcopyfile.md).</span></span> <span data-ttu-id="2d2f9-112">**IBackgroundCopyFile2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2d2f9-112">**IBackgroundCopyFile2** also has these types of members:</span></span>

-   [<span data-ttu-id="2d2f9-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="2d2f9-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2d2f9-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="2d2f9-114">Methods</span></span>

<span data-ttu-id="2d2f9-115">L'interfaccia **IBackgroundCopyFile2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2d2f9-115">The **IBackgroundCopyFile2** interface has these methods.</span></span>



| <span data-ttu-id="2d2f9-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="2d2f9-116">Method</span></span>                                                             | <span data-ttu-id="2d2f9-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d2f9-117">Description</span></span>                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="2d2f9-118">**GetFileRanges**</span><span class="sxs-lookup"><span data-stu-id="2d2f9-118">**GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md) | <span data-ttu-id="2d2f9-119">Recupera la matrice di intervalli che si desidera scaricare dall'URL.</span><span class="sxs-lookup"><span data-stu-id="2d2f9-119">Retrieves the array of ranges that you want to download from the URL.</span></span><br/> |
| [<span data-ttu-id="2d2f9-120">**Seremotename**</span><span class="sxs-lookup"><span data-stu-id="2d2f9-120">**SetRemoteName**</span></span>](ibackgroundcopyfile2-setremotename-method.md) | <span data-ttu-id="2d2f9-121">Consente di modificare il nome remoto in un nuovo URL.</span><span class="sxs-lookup"><span data-stu-id="2d2f9-121">Changes the remote name to a new URL.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="2d2f9-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d2f9-122">Requirements</span></span>



| <span data-ttu-id="2d2f9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d2f9-123">Requirement</span></span> | <span data-ttu-id="2d2f9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="2d2f9-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d2f9-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d2f9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2d2f9-126">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="2d2f9-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2d2f9-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d2f9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2d2f9-128">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d2f9-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2d2f9-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d2f9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d2f9-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d2f9-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d2f9-131">IDL</span><span class="sxs-lookup"><span data-stu-id="2d2f9-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d2f9-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d2f9-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2d2f9-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d2f9-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="2d2f9-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d2f9-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2d2f9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2d2f9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d2f9-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d2f9-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2d2f9-137">IID</span><span class="sxs-lookup"><span data-stu-id="2d2f9-137">IID</span></span><br/>                      | <span data-ttu-id="2d2f9-138">IID_IBackgroundCopyFile2 viene definito come 83E81B93-0873-474D-8A8C-F2018B1A939C</span><span class="sxs-lookup"><span data-stu-id="2d2f9-138">IID_IBackgroundCopyFile2 is defined as 83E81B93-0873-474D-8A8C-F2018B1A939C</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="2d2f9-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d2f9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d2f9-140">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="2d2f9-140">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> </dl>

 

 






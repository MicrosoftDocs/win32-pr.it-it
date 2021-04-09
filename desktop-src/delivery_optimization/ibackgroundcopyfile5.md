---
title: Interfaccia IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Usare questa interfaccia per ottenere o impostare le proprietà generiche dei trasferimenti di file di ottimizzazione recapito.
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- Interfaccia IBackgroundCopyFile5
- Interfaccia IBackgroundCopyFile5, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f23fdb99ba24b4faeca7a65930bf83d4634a979
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119611"
---
# <a name="ibackgroundcopyfile5-interface"></a><span data-ttu-id="a6070-105">Interfaccia IBackgroundCopyFile5</span><span class="sxs-lookup"><span data-stu-id="a6070-105">IBackgroundCopyFile5 interface</span></span>

<span data-ttu-id="a6070-106">Usare questa interfaccia per ottenere o impostare le proprietà generiche dei trasferimenti di file di ottimizzazione recapito.</span><span class="sxs-lookup"><span data-stu-id="a6070-106">Use this interface to get or set generic properties of Delivery Optimization (DO) file transfers.</span></span>

<span data-ttu-id="a6070-107">Per ottenere un puntatore a interfaccia **IBackgroundCopyFile5** , chiamare il metodo **IBackgroundCopyFile:: QueryInterface** usando __uuidof (IBackgroundCopyFile5) per l'identificatore di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a6070-107">To get an **IBackgroundCopyFile5** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile5) for the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="a6070-108">Membri</span><span class="sxs-lookup"><span data-stu-id="a6070-108">Members</span></span>

<span data-ttu-id="a6070-109">L'interfaccia **IBackgroundCopyFile5** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a6070-109">The **IBackgroundCopyFile5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a6070-110">**IBackgroundCopyFile5** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a6070-110">**IBackgroundCopyFile5** also has these types of members:</span></span>

-   [<span data-ttu-id="a6070-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="a6070-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a6070-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a6070-112">Methods</span></span>

<span data-ttu-id="a6070-113">L'interfaccia **IBackgroundCopyFile5** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a6070-113">The **IBackgroundCopyFile5** interface has these methods.</span></span>



| <span data-ttu-id="a6070-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="a6070-114">Method</span></span>                                                  | <span data-ttu-id="a6070-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6070-115">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="a6070-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="a6070-116">**GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md) | <span data-ttu-id="a6070-117">Ottiene il valore di una proprietà BackgroundCopyFile generica.</span><span class="sxs-lookup"><span data-stu-id="a6070-117">Gets the value of a generic BackgroundCopyFile property.</span></span><br/> |
| [<span data-ttu-id="a6070-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="a6070-118">**SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md) | <span data-ttu-id="a6070-119">Imposta il valore di una proprietà BackgroundCopyFile generica.</span><span class="sxs-lookup"><span data-stu-id="a6070-119">Sets the value of a generic BackgroundCopyFile property.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a6070-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6070-120">Requirements</span></span>



| <span data-ttu-id="a6070-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6070-121">Requirement</span></span> | <span data-ttu-id="a6070-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a6070-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6070-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6070-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a6070-124">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6070-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a6070-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6070-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a6070-126">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a6070-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a6070-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6070-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6070-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6070-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6070-129">IDL</span><span class="sxs-lookup"><span data-stu-id="a6070-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6070-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6070-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a6070-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="a6070-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="a6070-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6070-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a6070-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a6070-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6070-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6070-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a6070-135">IID</span><span class="sxs-lookup"><span data-stu-id="a6070-135">IID</span></span><br/>                      | <span data-ttu-id="a6070-136">IID_IBackgroundCopyFile5 viene definito come 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="a6070-136">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="a6070-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6070-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6070-138">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="a6070-138">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="a6070-139">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="a6070-139">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 


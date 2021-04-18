---
title: Interfaccia IBackgroundCopyFile (Deliveryoptimization. h)
description: IBackgroundCopyFile contiene informazioni su un file che fa parte di un processo. È ad esempio possibile utilizzare i metodi IBackgroundCopyFile per recuperare i nomi locali e remoti del file e trasferire le informazioni sullo stato di avanzamento.
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- Interfaccia IBackgroundCopyFile
- Interfaccia IBackgroundCopyFile, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301484"
---
# <a name="ibackgroundcopyfile-interface"></a><span data-ttu-id="3704b-106">Interfaccia IBackgroundCopyFile</span><span class="sxs-lookup"><span data-stu-id="3704b-106">IBackgroundCopyFile interface</span></span>

<span data-ttu-id="3704b-107">**IBackgroundCopyFile** contiene informazioni su un file che fa parte di un processo.</span><span class="sxs-lookup"><span data-stu-id="3704b-107">**IBackgroundCopyFile** contains information about a file that is part of a job.</span></span> <span data-ttu-id="3704b-108">È ad esempio possibile utilizzare i metodi **IBackgroundCopyFile** per recuperare i nomi locali e remoti del file e trasferire le informazioni sullo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="3704b-108">For example, you can use **IBackgroundCopyFile** methods to retrieve the local and remote names of the file and transfer progress information.</span></span>

<span data-ttu-id="3704b-109">Per ottenere un puntatore a interfaccia **IBackgroundCopyFile** , chiamare il metodo [**IBackgroundCopyError:: GetFile**](ibackgroundcopyerror-getfile-method.md) o il metodo [**IEnumBackgroundCopyFiles:: Next**](ienumbackgroundcopyfiles-next.md) .</span><span class="sxs-lookup"><span data-stu-id="3704b-109">To get an **IBackgroundCopyFile** interface pointer, call the [**IBackgroundCopyError::GetFile**](ibackgroundcopyerror-getfile-method.md) method or the [**IEnumBackgroundCopyFiles::Next**](ienumbackgroundcopyfiles-next.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="3704b-110">Membri</span><span class="sxs-lookup"><span data-stu-id="3704b-110">Members</span></span>

<span data-ttu-id="3704b-111">L'interfaccia **IBackgroundCopyFile** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3704b-111">The **IBackgroundCopyFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3704b-112">**IBackgroundCopyFile** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3704b-112">**IBackgroundCopyFile** also has these types of members:</span></span>

-   [<span data-ttu-id="3704b-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="3704b-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3704b-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="3704b-114">Methods</span></span>

<span data-ttu-id="3704b-115">L'interfaccia **IBackgroundCopyFile** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3704b-115">The **IBackgroundCopyFile** interface has these methods.</span></span>



| <span data-ttu-id="3704b-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="3704b-116">Method</span></span>                                                            | <span data-ttu-id="3704b-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3704b-117">Description</span></span>                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="3704b-118">**GetLocalName**</span><span class="sxs-lookup"><span data-stu-id="3704b-118">**GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)   | <span data-ttu-id="3704b-119">Recupera il nome locale del file.</span><span class="sxs-lookup"><span data-stu-id="3704b-119">Retrieves the local name of the file.</span></span><br/>        |
| [<span data-ttu-id="3704b-120">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="3704b-120">**GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)     | <span data-ttu-id="3704b-121">Recupera lo stato di avanzamento del trasferimento di file.</span><span class="sxs-lookup"><span data-stu-id="3704b-121">Retrieves the progress of the file transfer.</span></span><br/> |
| [<span data-ttu-id="3704b-122">**GetRemoteName**</span><span class="sxs-lookup"><span data-stu-id="3704b-122">**GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md) | <span data-ttu-id="3704b-123">Recupera il nome remoto del file.</span><span class="sxs-lookup"><span data-stu-id="3704b-123">Retrieves the remote name of the file.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="3704b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3704b-124">Requirements</span></span>



| <span data-ttu-id="3704b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3704b-125">Requirement</span></span> | <span data-ttu-id="3704b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="3704b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3704b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3704b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3704b-128">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="3704b-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3704b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3704b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3704b-130">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3704b-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3704b-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3704b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3704b-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3704b-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3704b-133">IDL</span><span class="sxs-lookup"><span data-stu-id="3704b-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3704b-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3704b-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3704b-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="3704b-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="3704b-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3704b-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3704b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3704b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3704b-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3704b-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3704b-139">IID</span><span class="sxs-lookup"><span data-stu-id="3704b-139">IID</span></span><br/>                      | <span data-ttu-id="3704b-140">IID_IBackgroundCopyFile viene definito come 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="3704b-140">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="3704b-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3704b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3704b-142">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="3704b-142">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="3704b-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="3704b-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> <dt>

[<span data-ttu-id="3704b-144">**Metodo ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="3704b-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="3704b-145">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="3704b-145">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 


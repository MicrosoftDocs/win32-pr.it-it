---
title: Proprietà RemoteProgramMode di ITSRemoteProgram
description: Modalità RemoteApp di Windows Server 2008 R2.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RemoteProgramMode
- Servizi Desktop remoto proprietà RemoteProgramMode, interfaccia ITSRemoteProgram
- Interfaccia ITSRemoteProgram Servizi Desktop remoto, proprietà RemoteProgramMode
- Servizi Desktop remoto proprietà RemoteProgramMode, interfaccia ITSRemoteProgram2
- Interfaccia ITSRemoteProgram2 Servizi Desktop remoto, proprietà RemoteProgramMode
- Servizi Desktop remoto proprietà RemoteProgramMode, interfaccia ITSRemoteProgram3
- Interfaccia ITSRemoteProgram3 Servizi Desktop remoto, proprietà RemoteProgramMode
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8582824e2f6349e37b125ffd974847b602ad6fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301867"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a><span data-ttu-id="0e7fb-110">Proprietà ITSRemoteProgram:: RemoteProgramMode</span><span class="sxs-lookup"><span data-stu-id="0e7fb-110">ITSRemoteProgram::RemoteProgramMode property</span></span>

<span data-ttu-id="0e7fb-111">Modalità RemoteApp di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-111">The Windows Server 2008 R2 RemoteApp mode.</span></span>

<span data-ttu-id="0e7fb-112">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e7fb-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e7fb-113">Syntax</span></span>


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a><span data-ttu-id="0e7fb-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0e7fb-114">Property value</span></span>

<span data-ttu-id="0e7fb-115">Modalità RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-115">The RemoteApp mode.</span></span> <span data-ttu-id="0e7fb-116">Se impostato su **Variant \_ true**, la modalità RemoteApp è abilitata e la sessione remota ospiterà i programmi RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-116">If set to **VARIANT\_TRUE**, RemoteApp mode is enabled, and the remote session will host RemoteApp programs.</span></span> <span data-ttu-id="0e7fb-117">Se è impostato su **Variant \_ false** (impostazione predefinita), la modalità RemoteApp non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-117">If set to **VARIANT\_FALSE** (the default), RemoteApp mode is not enabled.</span></span> <span data-ttu-id="0e7fb-118">La sessione remota ospiterà un desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-118">The remote session will host a remote desktop.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0e7fb-119">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0e7fb-119">Error codes</span></span>

<span data-ttu-id="0e7fb-120">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0e7fb-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e7fb-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e7fb-121">Requirements</span></span>



| <span data-ttu-id="0e7fb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e7fb-122">Requirement</span></span> | <span data-ttu-id="0e7fb-123">Valore</span><span class="sxs-lookup"><span data-stu-id="0e7fb-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e7fb-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e7fb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0e7fb-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e7fb-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0e7fb-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e7fb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0e7fb-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e7fb-127">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0e7fb-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0e7fb-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e7fb-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e7fb-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0e7fb-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0e7fb-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e7fb-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e7fb-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0e7fb-132">IID</span><span class="sxs-lookup"><span data-stu-id="0e7fb-132">IID</span></span><br/>                      | <span data-ttu-id="0e7fb-133">IID \_ ITSRemoteProgram è definito come FDD029F9-467a-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="0e7fb-133">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="0e7fb-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e7fb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e7fb-135">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="0e7fb-135">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="0e7fb-136">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="0e7fb-136">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="0e7fb-137">**ITSRemoteProgram**</span><span class="sxs-lookup"><span data-stu-id="0e7fb-137">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 






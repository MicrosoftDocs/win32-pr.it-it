---
title: Metodo TestAndSetState della classe Win32_RDSHServer
description: Confronta lo stato corrente con il comparand specificato. Se le due corrispondenze, lo stato viene impostato su un nuovo valore. Indipendentemente dalla corrispondenza, viene restituito anche lo stato corrente.
ms.assetid: f1bb0076-251b-4c0d-92f9-1c460e1b26bb
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo TestAndSetState
- Metodo TestAndSetState Servizi Desktop remoto, classe Win32_RDSHServer
- Classe Win32_RDSHServer Servizi Desktop remoto, metodo TestAndSetState
topic_type:
- apiref
api_name:
- Win32_RDSHServer.TestAndSetState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4c9b616c2a288f5f39b240d71b2611e25d45f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119974"
---
# <a name="testandsetstate-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="3a6a2-107">Metodo TestAndSetState della \_ classe RDSHServer Win32</span><span class="sxs-lookup"><span data-stu-id="3a6a2-107">TestAndSetState method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="3a6a2-108">Confronta lo stato corrente con il comparand specificato. Se le due corrispondenze, lo stato viene impostato su un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-108">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="3a6a2-109">Indipendentemente dalla corrispondenza, viene restituito anche lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-109">Regardless of the match, the current state is also returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a6a2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a6a2-110">Syntax</span></span>


```mof
uint32 TestAndSetState(
  [in]  uint32 Comparand,
  [in]  uint32 NewState,
  [out] uint32 InitState
);
```



## <a name="parameters"></a><span data-ttu-id="3a6a2-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a6a2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a6a2-112">*Comparand* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a6a2-112">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a6a2-113">Valore da confrontare con lo stato corrente. Se i due valori corrispondono, lo stato viene impostato su *NewState*.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-113">A value to compare to the current state; if the two values match, the state is set to *NewState*.</span></span>

</dd> <dt>

<span data-ttu-id="3a6a2-114">*NewState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a6a2-114">*NewState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a6a2-115">Nuovo valore dello stato.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-115">The new value of the state.</span></span>

</dd> <dt>

<span data-ttu-id="3a6a2-116">*InitState* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3a6a2-116">*InitState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a6a2-117">In caso di esito positivo o negativo, restituisce lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="3a6a2-117">On success or failure, returns the current state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a6a2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a6a2-118">Requirements</span></span>



| <span data-ttu-id="3a6a2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a6a2-119">Requirement</span></span> | <span data-ttu-id="3a6a2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3a6a2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a6a2-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a6a2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a6a2-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3a6a2-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="3a6a2-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a6a2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3a6a2-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3a6a2-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="3a6a2-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3a6a2-125">Namespace</span></span><br/>                | <span data-ttu-id="3a6a2-126">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="3a6a2-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="3a6a2-127">MOF</span><span class="sxs-lookup"><span data-stu-id="3a6a2-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a6a2-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a6a2-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a6a2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3a6a2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a6a2-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a6a2-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="3a6a2-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a6a2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a6a2-132">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="3a6a2-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 






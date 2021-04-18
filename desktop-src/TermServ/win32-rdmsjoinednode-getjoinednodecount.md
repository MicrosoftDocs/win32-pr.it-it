---
title: Metodo GetJoinedNodeCount della classe Win32_RDMSJoinedNode
description: Ottenere il numero di server in cui sono installati i ruoli specificati.
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetJoinedNodeCount
- Metodo GetJoinedNodeCount Servizi Desktop remoto, classe Win32_RDMSJoinedNode
- Classe Win32_RDMSJoinedNode Servizi Desktop remoto, metodo GetJoinedNodeCount
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301448"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="891eb-106">Metodo GetJoinedNodeCount della \_ classe RDMSJoinedNode Win32</span><span class="sxs-lookup"><span data-stu-id="891eb-106">GetJoinedNodeCount method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="891eb-107">Ottenere il numero di server in cui sono installati i ruoli specificati.</span><span class="sxs-lookup"><span data-stu-id="891eb-107">Get number of servers that have the specified roles installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="891eb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="891eb-108">Syntax</span></span>


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a><span data-ttu-id="891eb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="891eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="891eb-110">*RoleType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="891eb-110">*roleType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="891eb-111">Oggetto bit che specifica i tipi di ruolo.</span><span class="sxs-lookup"><span data-stu-id="891eb-111">A bitfield that specifies the role types.</span></span>

<dt>

<span data-ttu-id="891eb-112">0</span><span class="sxs-lookup"><span data-stu-id="891eb-112">0</span></span>
</dt> <dd>

<span data-ttu-id="891eb-113">Tutti</span><span class="sxs-lookup"><span data-stu-id="891eb-113">All</span></span>

</dd> <dt>

<span data-ttu-id="891eb-114">1</span><span class="sxs-lookup"><span data-stu-id="891eb-114">1</span></span>
</dt> <dd>

<span data-ttu-id="891eb-115">Broker di Connessione Desktop remoto (RDCB)</span><span class="sxs-lookup"><span data-stu-id="891eb-115">Remote Desktop Connection Broker (RDCB)</span></span>

</dd> <dt>

<span data-ttu-id="891eb-116">2</span><span class="sxs-lookup"><span data-stu-id="891eb-116">2</span></span>
</dt> <dd>

<span data-ttu-id="891eb-117">Host sessione Desktop remoto (RDSH)</span><span class="sxs-lookup"><span data-stu-id="891eb-117">Remote Desktop Session Host (RDSH)</span></span>

</dd> <dt>

<span data-ttu-id="891eb-118">4</span><span class="sxs-lookup"><span data-stu-id="891eb-118">4</span></span>
</dt> <dd>

<span data-ttu-id="891eb-119">Host di virtualizzazione Desktop remoto (RDVH)</span><span class="sxs-lookup"><span data-stu-id="891eb-119">Remote Desktop Virtualization Host (RDVH)</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="891eb-120">*Numero* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="891eb-120">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="891eb-121">Se l'operazione riesce, restituisce il numero di server con i ruoli specificati installati.</span><span class="sxs-lookup"><span data-stu-id="891eb-121">On success, returns the number of servers with the specified roles installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="891eb-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="891eb-122">Return value</span></span>

<span data-ttu-id="891eb-123">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="891eb-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="891eb-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="891eb-124">Requirements</span></span>



| <span data-ttu-id="891eb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="891eb-125">Requirement</span></span> | <span data-ttu-id="891eb-126">Valore</span><span class="sxs-lookup"><span data-stu-id="891eb-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="891eb-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="891eb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="891eb-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="891eb-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="891eb-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="891eb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="891eb-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="891eb-130">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="891eb-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="891eb-131">Namespace</span></span><br/>                | <span data-ttu-id="891eb-132">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="891eb-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="891eb-133">MOF</span><span class="sxs-lookup"><span data-stu-id="891eb-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="891eb-134"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="891eb-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="891eb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="891eb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="891eb-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="891eb-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="891eb-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="891eb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="891eb-138">**\_RDMSJoinedNode Win32**</span><span class="sxs-lookup"><span data-stu-id="891eb-138">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 






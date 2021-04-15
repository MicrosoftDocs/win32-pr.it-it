---
title: Metodo join della classe Win32_RDMSJoinedNode
description: Aggiunge un nodo a Desktop remoto Management Services (RDBMS).
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Metodo join Servizi Desktop remoto
- Metodo join Servizi Desktop remoto, classe Win32_RDMSJoinedNode
- Classe Win32_RDMSJoinedNode Servizi Desktop remoto, metodo Join
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587e68758971453e8c4e307ccb37ce6cede262f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400372"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="6a443-106">Metodo join della classe Win32 \_ RDMSJoinedNode</span><span class="sxs-lookup"><span data-stu-id="6a443-106">Join method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="6a443-107">Aggiunge un nodo a Desktop remoto Management Services (RDBMS).</span><span class="sxs-lookup"><span data-stu-id="6a443-107">Adds a node to Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a443-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a443-108">Syntax</span></span>


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a><span data-ttu-id="6a443-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a443-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a443-110">*NodeFQDN* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a443-110">*NodeFQDN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a443-111">Nome di dominio completo del nodo.</span><span class="sxs-lookup"><span data-stu-id="6a443-111">The fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="6a443-112">*Nodesid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a443-112">*NodeSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a443-113">ID di sicurezza (SID) del nodo.</span><span class="sxs-lookup"><span data-stu-id="6a443-113">The security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a443-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a443-114">Return value</span></span>

<span data-ttu-id="6a443-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="6a443-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a443-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a443-116">Requirements</span></span>



| <span data-ttu-id="6a443-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a443-117">Requirement</span></span> | <span data-ttu-id="6a443-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6a443-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a443-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a443-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6a443-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6a443-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6a443-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a443-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6a443-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a443-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6a443-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6a443-123">Namespace</span></span><br/>                | <span data-ttu-id="6a443-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="6a443-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6a443-125">MOF</span><span class="sxs-lookup"><span data-stu-id="6a443-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a443-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a443-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a443-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6a443-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a443-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a443-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6a443-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a443-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a443-130">**\_RDMSJoinedNode Win32**</span><span class="sxs-lookup"><span data-stu-id="6a443-130">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 






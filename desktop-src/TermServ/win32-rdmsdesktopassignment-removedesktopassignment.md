---
title: Metodo RemoveDesktopAssignment della classe Win32_RDMSDesktopAssignment
description: Rimuove un'assegnazione desktop.
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveDesktopAssignment
- Metodo RemoveDesktopAssignment Servizi Desktop remoto, classe Win32_RDMSDesktopAssignment
- Classe Win32_RDMSDesktopAssignment Servizi Desktop remoto, metodo RemoveDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302569"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a><span data-ttu-id="d8047-106">Metodo RemoveDesktopAssignment della \_ classe RDMSDesktopAssignment Win32</span><span class="sxs-lookup"><span data-stu-id="d8047-106">RemoveDesktopAssignment method of the Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="d8047-107">Rimuove un'assegnazione desktop</span><span class="sxs-lookup"><span data-stu-id="d8047-107">Removes a desktop assignment</span></span>

## <a name="syntax"></a><span data-ttu-id="d8047-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8047-108">Syntax</span></span>


```mof
uint32 RemoveDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="d8047-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8047-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8047-110">*CollectionAlias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8047-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8047-111">Alias della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d8047-111">The collection alias.</span></span>

</dd> <dt>

<span data-ttu-id="d8047-112">*Desktopname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8047-112">*DesktopName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8047-113">Nome del desktop.</span><span class="sxs-lookup"><span data-stu-id="d8047-113">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="d8047-114">*UserDomain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8047-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8047-115">Nome di dominio dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="d8047-115">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="d8047-116">*Nome utente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8047-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8047-117">Nome dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="d8047-117">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8047-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8047-118">Requirements</span></span>



| <span data-ttu-id="d8047-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8047-119">Requirement</span></span> | <span data-ttu-id="d8047-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d8047-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8047-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8047-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d8047-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d8047-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="d8047-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8047-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d8047-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d8047-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="d8047-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d8047-125">Namespace</span></span><br/>                | <span data-ttu-id="d8047-126">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="d8047-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="d8047-127">MOF</span><span class="sxs-lookup"><span data-stu-id="d8047-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8047-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8047-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8047-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d8047-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8047-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8047-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="d8047-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8047-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8047-132">**\_RDMSDesktopAssignment Win32**</span><span class="sxs-lookup"><span data-stu-id="d8047-132">**Win32\_RDMSDesktopAssignment**</span></span>](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 






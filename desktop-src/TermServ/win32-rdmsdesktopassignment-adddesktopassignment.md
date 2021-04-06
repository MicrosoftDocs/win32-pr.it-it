---
title: Metodo AddDesktopAssignment della classe Win32_RDMSDesktopAssignment
description: Aggiungere un'assegnazione desktop.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddDesktopAssignment
- Metodo AddDesktopAssignment Servizi Desktop remoto, classe Win32_RDMSDesktopAssignment
- Classe Win32_RDMSDesktopAssignment Servizi Desktop remoto, metodo AddDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.AddDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571273e76b0bb45b748f1587e5a831fcf1e36b0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873626"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a><span data-ttu-id="af2ef-106">Metodo AddDesktopAssignment della \_ classe RDMSDesktopAssignment Win32</span><span class="sxs-lookup"><span data-stu-id="af2ef-106">AddDesktopAssignment method of the Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="af2ef-107">Aggiungere un'assegnazione desktop</span><span class="sxs-lookup"><span data-stu-id="af2ef-107">Add a desktop assignment</span></span>

## <a name="syntax"></a><span data-ttu-id="af2ef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af2ef-108">Syntax</span></span>


```mof
uint32 AddDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="af2ef-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="af2ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af2ef-110">*CollectionAlias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af2ef-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af2ef-111">Alias della raccolta.</span><span class="sxs-lookup"><span data-stu-id="af2ef-111">The collection alias.</span></span>

</dd> <dt>

<span data-ttu-id="af2ef-112">*Desktopname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af2ef-112">*DesktopName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af2ef-113">Nome del desktop.</span><span class="sxs-lookup"><span data-stu-id="af2ef-113">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="af2ef-114">*UserDomain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af2ef-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af2ef-115">Nome di dominio dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="af2ef-115">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="af2ef-116">*Nome utente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af2ef-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af2ef-117">Nome dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="af2ef-117">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af2ef-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af2ef-118">Requirements</span></span>



| <span data-ttu-id="af2ef-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="af2ef-119">Requirement</span></span> | <span data-ttu-id="af2ef-120">Valore</span><span class="sxs-lookup"><span data-stu-id="af2ef-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="af2ef-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af2ef-121">Minimum supported client</span></span><br/> | <span data-ttu-id="af2ef-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="af2ef-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="af2ef-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af2ef-123">Minimum supported server</span></span><br/> | <span data-ttu-id="af2ef-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="af2ef-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="af2ef-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af2ef-125">Namespace</span></span><br/>                | <span data-ttu-id="af2ef-126">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="af2ef-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="af2ef-127">MOF</span><span class="sxs-lookup"><span data-stu-id="af2ef-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af2ef-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af2ef-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="af2ef-129">DLL</span><span class="sxs-lookup"><span data-stu-id="af2ef-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af2ef-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af2ef-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="af2ef-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af2ef-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af2ef-132">**\_RDMSDesktopAssignment Win32**</span><span class="sxs-lookup"><span data-stu-id="af2ef-132">**Win32\_RDMSDesktopAssignment**</span></span>](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 






---
title: Metodo GetVirtualDesktopAssignedToUser della classe Win32_RDMSVirtualDesktop
description: Recupera il desktop virtuale assegnato all'utente specificato.
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetVirtualDesktopAssignedToUser
- Metodo GetVirtualDesktopAssignedToUser Servizi Desktop remoto, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Servizi Desktop remoto, metodo GetVirtualDesktopAssignedToUser
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopAssignedToUser
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcbbbed20b6b571e8867689ac901344af8e23b93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301112"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="b00ef-106">Metodo GetVirtualDesktopAssignedToUser della \_ classe RDMSVirtualDesktop Win32</span><span class="sxs-lookup"><span data-stu-id="b00ef-106">GetVirtualDesktopAssignedToUser method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="b00ef-107">Recupera il desktop virtuale assegnato all'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="b00ef-107">Retrieves the virtual desktop that is assigned to the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="b00ef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b00ef-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopAssignedToUser(
  [in]  string CollectionAlias,
  [in]  string UserName,
  [in]  string UserDomain,
  [out] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="b00ef-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b00ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b00ef-110">*CollectionAlias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b00ef-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b00ef-111">Alias dell'insieme di desktop virtuali che contiene il desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="b00ef-111">The alias of the virtual desktop collection that contain the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="b00ef-112">*Nome utente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b00ef-112">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b00ef-113">Nome utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b00ef-113">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="b00ef-114">*UserDomain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b00ef-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b00ef-115">Nome di dominio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b00ef-115">The domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="b00ef-116">*VMName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b00ef-116">*VMName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b00ef-117">Riceve il nome della macchina virtuale del desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="b00ef-117">Receives the virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b00ef-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b00ef-118">Return value</span></span>

<span data-ttu-id="b00ef-119">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="b00ef-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b00ef-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b00ef-120">Requirements</span></span>



| <span data-ttu-id="b00ef-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b00ef-121">Requirement</span></span> | <span data-ttu-id="b00ef-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b00ef-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b00ef-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b00ef-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b00ef-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b00ef-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b00ef-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b00ef-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b00ef-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b00ef-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b00ef-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b00ef-127">Namespace</span></span><br/>                | <span data-ttu-id="b00ef-128">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="b00ef-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b00ef-129">MOF</span><span class="sxs-lookup"><span data-stu-id="b00ef-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b00ef-130"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b00ef-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b00ef-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b00ef-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b00ef-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b00ef-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b00ef-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b00ef-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b00ef-134">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="b00ef-134">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 






---
title: Metodo RemoveUserAssignment della classe Win32_RDMSVirtualDesktop
description: Rimuove l'assegnazione utente dal desktop virtuale.
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveUserAssignment
- Metodo RemoveUserAssignment Servizi Desktop remoto, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Servizi Desktop remoto, metodo RemoveUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.RemoveUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01675c777603f0eab2d22c0136b1ef6cc3522b7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301859"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="86c4c-106">Metodo RemoveUserAssignment della \_ classe RDMSVirtualDesktop Win32</span><span class="sxs-lookup"><span data-stu-id="86c4c-106">RemoveUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="86c4c-107">Rimuove l'assegnazione utente dal desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="86c4c-107">Removes the user assignment from the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="86c4c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86c4c-108">Syntax</span></span>


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="86c4c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="86c4c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86c4c-110">*VMName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86c4c-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c4c-111">Nome della macchina virtuale del desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="86c4c-111">The virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86c4c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86c4c-112">Return value</span></span>

<span data-ttu-id="86c4c-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="86c4c-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="86c4c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86c4c-114">Requirements</span></span>



| <span data-ttu-id="86c4c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="86c4c-115">Requirement</span></span> | <span data-ttu-id="86c4c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="86c4c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="86c4c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86c4c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="86c4c-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="86c4c-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="86c4c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86c4c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="86c4c-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="86c4c-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="86c4c-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="86c4c-121">Namespace</span></span><br/>                | <span data-ttu-id="86c4c-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="86c4c-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="86c4c-123">MOF</span><span class="sxs-lookup"><span data-stu-id="86c4c-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86c4c-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86c4c-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="86c4c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="86c4c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86c4c-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86c4c-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="86c4c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86c4c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c4c-128">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="86c4c-128">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 






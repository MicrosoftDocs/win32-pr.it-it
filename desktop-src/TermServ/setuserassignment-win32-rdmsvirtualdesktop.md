---
title: Metodo SetUserAssignment della classe Win32_RDMSVirtualDesktop
description: Assegna un desktop virtuale a un utente.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetUserAssignment
- Metodo SetUserAssignment Servizi Desktop remoto, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Servizi Desktop remoto, metodo SetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f02e1cc935e344edd6a9c52016052e082e08d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302446"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="bcabf-106">Metodo SetUserAssignment della \_ classe RDMSVirtualDesktop Win32</span><span class="sxs-lookup"><span data-stu-id="bcabf-106">SetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="bcabf-107">Assegna un desktop virtuale a un utente.</span><span class="sxs-lookup"><span data-stu-id="bcabf-107">Assigns a virtual desktop to a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcabf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcabf-108">Syntax</span></span>


```mof
uint32 SetUserAssignment(
  [in] string UserName,
  [in] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="bcabf-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcabf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcabf-110">*Nome utente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bcabf-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcabf-111">Nome utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bcabf-111">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="bcabf-112">*UserDomain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bcabf-112">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcabf-113">Nome di dominio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bcabf-113">The domain name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcabf-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcabf-114">Return value</span></span>

<span data-ttu-id="bcabf-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="bcabf-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcabf-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcabf-116">Requirements</span></span>



| <span data-ttu-id="bcabf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcabf-117">Requirement</span></span> | <span data-ttu-id="bcabf-118">Valore</span><span class="sxs-lookup"><span data-stu-id="bcabf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcabf-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcabf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bcabf-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bcabf-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="bcabf-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcabf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bcabf-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bcabf-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="bcabf-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bcabf-123">Namespace</span></span><br/>                | <span data-ttu-id="bcabf-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="bcabf-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="bcabf-125">MOF</span><span class="sxs-lookup"><span data-stu-id="bcabf-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcabf-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bcabf-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcabf-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bcabf-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcabf-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcabf-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="bcabf-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcabf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcabf-130">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="bcabf-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 






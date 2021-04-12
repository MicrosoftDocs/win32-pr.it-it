---
title: Metodo GetUserAssignment della classe Win32_RDMSVirtualDesktop
description: Recupera il nome utente e il nome di dominio dell'utente assegnato al desktop virtuale.
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetUserAssignment
- Metodo GetUserAssignment Servizi Desktop remoto, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Servizi Desktop remoto, metodo GetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87293a471bb4f69b3f4c57de0f964fa0daa043cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400745"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="156aa-106">Metodo GetUserAssignment della \_ classe RDMSVirtualDesktop Win32</span><span class="sxs-lookup"><span data-stu-id="156aa-106">GetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="156aa-107">Recupera il nome utente e il nome di dominio dell'utente assegnato al desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="156aa-107">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="156aa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="156aa-108">Syntax</span></span>


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="156aa-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="156aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="156aa-110">*Nome utente* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="156aa-110">*UserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="156aa-111">Riceve il nome utente.</span><span class="sxs-lookup"><span data-stu-id="156aa-111">Receives the username.</span></span>

</dd> <dt>

<span data-ttu-id="156aa-112">*UserDomain* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="156aa-112">*UserDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="156aa-113">Riceve il nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="156aa-113">Receives the domain name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="156aa-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="156aa-114">Return value</span></span>

<span data-ttu-id="156aa-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="156aa-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="156aa-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="156aa-116">Requirements</span></span>



| <span data-ttu-id="156aa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="156aa-117">Requirement</span></span> | <span data-ttu-id="156aa-118">Valore</span><span class="sxs-lookup"><span data-stu-id="156aa-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="156aa-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="156aa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="156aa-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="156aa-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="156aa-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="156aa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="156aa-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="156aa-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="156aa-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="156aa-123">Namespace</span></span><br/>                | <span data-ttu-id="156aa-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="156aa-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="156aa-125">MOF</span><span class="sxs-lookup"><span data-stu-id="156aa-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="156aa-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="156aa-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="156aa-127">DLL</span><span class="sxs-lookup"><span data-stu-id="156aa-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="156aa-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="156aa-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="156aa-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="156aa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="156aa-130">**\_RDMSVirtualDesktop Win32**</span><span class="sxs-lookup"><span data-stu-id="156aa-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 






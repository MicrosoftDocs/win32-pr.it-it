---
title: Interfaccia INapClientManagement2 (NapManagement. h)
description: Fornisce metodi per la gestione client di protezione accesso alla rete. | Interfaccia INapClientManagement2 (NapManagement. h)
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- NAP interfaccia INapClientManagement2
- Interfaccia NAP di INapClientManagement2, descrizione
topic_type:
- apiref
api_name:
- INapClientManagement2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3441b52ddf776337765f39d23528bc223a17b1e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058560"
---
# <a name="inapclientmanagement2-interface"></a><span data-ttu-id="3ea52-106">Interfaccia INapClientManagement2</span><span class="sxs-lookup"><span data-stu-id="3ea52-106">INapClientManagement2 interface</span></span>

> [!Note]  
> <span data-ttu-id="3ea52-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="3ea52-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3ea52-108">L'interfaccia **INapClientManagement2** fornisce metodi per la gestione client di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="3ea52-108">The **INapClientManagement2** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="3ea52-109">Questa interfaccia eredita tutti i metodi di [**INapClientManagement**](inapclientmanagement.md) e deve essere usata in alternativa.</span><span class="sxs-lookup"><span data-stu-id="3ea52-109">This interface inherits all the methods of [**INapClientManagement**](inapclientmanagement.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="3ea52-110">Membri</span><span class="sxs-lookup"><span data-stu-id="3ea52-110">Members</span></span>

<span data-ttu-id="3ea52-111">L'interfaccia **INapClientManagement2** eredita da [**INapClientManagement**](inapclientmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="3ea52-111">The **INapClientManagement2** interface inherits from [**INapClientManagement**](inapclientmanagement.md).</span></span> <span data-ttu-id="3ea52-112">**INapClientManagement2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3ea52-112">**INapClientManagement2** also has these types of members:</span></span>

-   [<span data-ttu-id="3ea52-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="3ea52-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3ea52-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="3ea52-114">Methods</span></span>

<span data-ttu-id="3ea52-115">L'interfaccia **INapClientManagement2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3ea52-115">The **INapClientManagement2** interface has these methods.</span></span>



| <span data-ttu-id="3ea52-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="3ea52-116">Method</span></span>                                                                                                    | <span data-ttu-id="3ea52-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ea52-117">Description</span></span>                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ea52-118">**INapClientManagement2::GetSystemIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="3ea52-118">**INapClientManagement2::GetSystemIsolationInfoEx**</span></span>](inapclientmanagement2-getsystemisolationinfoex.md) | <span data-ttu-id="3ea52-119">Recupera le informazioni sullo stato di isolamento e sullo stato di isolamento esteso del client di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="3ea52-119">Retrieves information about the isolation state and extended isolation state of the Nap client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3ea52-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ea52-120">Requirements</span></span>



| <span data-ttu-id="3ea52-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ea52-121">Requirement</span></span> | <span data-ttu-id="3ea52-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3ea52-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ea52-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ea52-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3ea52-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ea52-124">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3ea52-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ea52-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3ea52-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ea52-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3ea52-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ea52-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ea52-128"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ea52-128"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ea52-129">IDL</span><span class="sxs-lookup"><span data-stu-id="3ea52-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ea52-130"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ea52-130"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="3ea52-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3ea52-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ea52-132"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ea52-132"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="3ea52-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ea52-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ea52-134">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="3ea52-134">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> <dt>

[<span data-ttu-id="3ea52-135">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="3ea52-135">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3ea52-136">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="3ea52-136">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 






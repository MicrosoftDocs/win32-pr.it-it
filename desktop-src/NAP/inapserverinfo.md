---
title: Interfaccia INapServerInfo (NapServerManagement. h)
description: I client di gestione (ad esempio, i provider WMI o gli strumenti da riga di comando) utilizzano per eseguire una query sullo stato del sistema server protezione accesso alla rete.
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- NAP interfaccia INapServerInfo
- Interfaccia NAP di INapServerInfo, descrizione
topic_type:
- apiref
api_name:
- INapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec17e3303fe4af4d359279de6c5fa7aa5f34d409
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301813"
---
# <a name="inapserverinfo-interface"></a><span data-ttu-id="1c5d5-105">Interfaccia INapServerInfo</span><span class="sxs-lookup"><span data-stu-id="1c5d5-105">INapServerInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="1c5d5-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="1c5d5-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1c5d5-107">**INapServerInfo** fornisce i metodi che i client di gestione (ad esempio, i provider WMI o gli strumenti da riga di comando) utilizzano per eseguire una query sullo stato del sistema server protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="1c5d5-107">The **INapServerInfo** provides methods that Management clients (for example, WMI providers or command-line tools) use to query the status of the NAP server system.</span></span>

## <a name="members"></a><span data-ttu-id="1c5d5-108">Membri</span><span class="sxs-lookup"><span data-stu-id="1c5d5-108">Members</span></span>

<span data-ttu-id="1c5d5-109">L'interfaccia **INapServerInfo** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1c5d5-109">The **INapServerInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1c5d5-110">**INapServerInfo** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1c5d5-110">**INapServerInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="1c5d5-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="1c5d5-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1c5d5-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="1c5d5-112">Methods</span></span>

<span data-ttu-id="1c5d5-113">L'interfaccia **INapServerInfo** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1c5d5-113">The **INapServerInfo** interface has these methods.</span></span>



| <span data-ttu-id="1c5d5-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="1c5d5-114">Method</span></span>                                                                                                                   | <span data-ttu-id="1c5d5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c5d5-115">Description</span></span>                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="1c5d5-116">**INapServerInfo::GetFailureCategoryMappings**</span><span class="sxs-lookup"><span data-stu-id="1c5d5-116">**INapServerInfo::GetFailureCategoryMappings**</span></span>](inapserverinfo-getfailurecategorymappings-method.md)                   | <span data-ttu-id="1c5d5-117">Recupera i mapping delle categorie di errore per un oggetto di convalida integrità specificato.</span><span class="sxs-lookup"><span data-stu-id="1c5d5-117">Retrieves the failure category mappings for a specified SHV.</span></span><br/> |
| [<span data-ttu-id="1c5d5-118">**INapServerInfo::GetNapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="1c5d5-118">**INapServerInfo::GetNapServerInfo**</span></span>](inapserverinfo-getnapserverinfo-method.md)                                       | <span data-ttu-id="1c5d5-119">Recupera le informazioni sul server NAP.</span><span class="sxs-lookup"><span data-stu-id="1c5d5-119">Retrieves information about the NAP server.</span></span><br/>                  |
| [<span data-ttu-id="1c5d5-120">**INapServerInfo::GetRegisteredSystemHealthValidators**</span><span class="sxs-lookup"><span data-stu-id="1c5d5-120">**INapServerInfo::GetRegisteredSystemHealthValidators**</span></span>](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | <span data-ttu-id="1c5d5-121">Recupera un elenco di SHV registrati.</span><span class="sxs-lookup"><span data-stu-id="1c5d5-121">Retrieves a list of registered SHVs.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="1c5d5-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c5d5-122">Remarks</span></span>

<span data-ttu-id="1c5d5-123">Questi metodi forniscono solo informazioni statiche sul server NAP e sui relativi componenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="1c5d5-123">These methods provide only static information about the NAP Server and its components on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c5d5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c5d5-124">Requirements</span></span>



| <span data-ttu-id="1c5d5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c5d5-125">Requirement</span></span> | <span data-ttu-id="1c5d5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="1c5d5-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c5d5-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c5d5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1c5d5-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1c5d5-128">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="1c5d5-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c5d5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1c5d5-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1c5d5-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1c5d5-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c5d5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c5d5-132"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c5d5-132"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c5d5-133">IDL</span><span class="sxs-lookup"><span data-stu-id="1c5d5-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1c5d5-134"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c5d5-134"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="1c5d5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1c5d5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c5d5-136"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c5d5-136"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="1c5d5-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c5d5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c5d5-138">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="1c5d5-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1c5d5-139">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="1c5d5-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 


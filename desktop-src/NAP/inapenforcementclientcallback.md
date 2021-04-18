---
title: Interfaccia INapEnforcementClientCallback (NapEnforcementClient. h)
description: I client di imposizione devono implementare per consentire a NapAgent di comunicare con loro.
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- NAP interfaccia INapEnforcementClientCallback
- Interfaccia NAP di INapEnforcementClientCallback, descrizione
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d5c7e066115a6d51879775d9b8cfab3cbe4888
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302716"
---
# <a name="inapenforcementclientcallback-interface"></a><span data-ttu-id="8bf01-105">Interfaccia INapEnforcementClientCallback</span><span class="sxs-lookup"><span data-stu-id="8bf01-105">INapEnforcementClientCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="8bf01-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="8bf01-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8bf01-107">L'interfaccia **INapEnforcementClientCallback** fornisce metodi di callback che i client di imposizione devono implementare per consentire a napagent di comunicare con essi.</span><span class="sxs-lookup"><span data-stu-id="8bf01-107">The **INapEnforcementClientCallback** interface provides callback methods that enforcement clients must implement to enable the NapAgent to communicate with them.</span></span>

## <a name="members"></a><span data-ttu-id="8bf01-108">Membri</span><span class="sxs-lookup"><span data-stu-id="8bf01-108">Members</span></span>

<span data-ttu-id="8bf01-109">L'interfaccia **INapEnforcementClientCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8bf01-109">The **INapEnforcementClientCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8bf01-110">**INapEnforcementClientCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8bf01-110">**INapEnforcementClientCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="8bf01-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="8bf01-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8bf01-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="8bf01-112">Methods</span></span>

<span data-ttu-id="8bf01-113">L'interfaccia **INapEnforcementClientCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8bf01-113">The **INapEnforcementClientCallback** interface has these methods.</span></span>



| <span data-ttu-id="8bf01-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="8bf01-114">Method</span></span>                                                                                                         | <span data-ttu-id="8bf01-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bf01-115">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="8bf01-116">**INapEnforcementClientCallback:: getconnects**</span><span class="sxs-lookup"><span data-stu-id="8bf01-116">**INapEnforcementClientCallback::GetConnections**</span></span>](inapenforcementclientcallback-getconnections-method.md)   | <span data-ttu-id="8bf01-117">Usato da NapAgent per recuperare le connessioni.</span><span class="sxs-lookup"><span data-stu-id="8bf01-117">Used by the NapAgent to retrieve connections.</span></span><br/>                         |
| [<span data-ttu-id="8bf01-118">**INapEnforcementClientCallback::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="8bf01-118">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md) | <span data-ttu-id="8bf01-119">Usato da NapAgent per informare il client di imposizione delle modifiche del rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="8bf01-119">Used by the NapAgent to inform the enforcement client of SoH changes.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8bf01-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bf01-120">Requirements</span></span>



| <span data-ttu-id="8bf01-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bf01-121">Requirement</span></span> | <span data-ttu-id="8bf01-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8bf01-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf01-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bf01-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf01-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8bf01-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8bf01-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bf01-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf01-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8bf01-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8bf01-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8bf01-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bf01-128"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bf01-128"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="8bf01-129">IDL</span><span class="sxs-lookup"><span data-stu-id="8bf01-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8bf01-130"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8bf01-130"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



 


---
title: Interfaccia INapSystemHealthValidationRequest2 (NapSystemHealthValidator. h)
description: Fornisce metodi utilizzati per supportare i validator di integrità del sistema definiti dallo sviluppatore di applicazioni.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- NAP interfaccia INapSystemHealthValidationRequest2
- Interfaccia NAP di INapSystemHealthValidationRequest2, descrizione
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12fdbfc46578a4e64a92accc46f6b910a44dd946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302714"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a><span data-ttu-id="43a20-105">Interfaccia INapSystemHealthValidationRequest2</span><span class="sxs-lookup"><span data-stu-id="43a20-105">INapSystemHealthValidationRequest2 interface</span></span>

> [!Note]  
> <span data-ttu-id="43a20-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="43a20-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="43a20-107">L'interfaccia **INapSystemHealthValidationRequest2** fornisce i metodi utilizzati per supportare i validator dell'integrità di sistema definiti dallo sviluppatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="43a20-107">The **INapSystemHealthValidationRequest2** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="43a20-108">Questa interfaccia eredita tutti i metodi di [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) e deve essere usata in alternativa.</span><span class="sxs-lookup"><span data-stu-id="43a20-108">This interface inherits all the methods of [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="43a20-109">Membri</span><span class="sxs-lookup"><span data-stu-id="43a20-109">Members</span></span>

<span data-ttu-id="43a20-110">L'interfaccia **INapSystemHealthValidationRequest2** eredita da [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).</span><span class="sxs-lookup"><span data-stu-id="43a20-110">The **INapSystemHealthValidationRequest2** interface inherits from [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).</span></span> <span data-ttu-id="43a20-111">**INapSystemHealthValidationRequest2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="43a20-111">**INapSystemHealthValidationRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="43a20-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="43a20-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="43a20-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="43a20-113">Methods</span></span>

<span data-ttu-id="43a20-114">L'interfaccia **INapSystemHealthValidationRequest2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="43a20-114">The **INapSystemHealthValidationRequest2** interface has these methods.</span></span>



| <span data-ttu-id="43a20-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="43a20-115">Method</span></span>                                                                                                    | <span data-ttu-id="43a20-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43a20-116">Description</span></span>                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="43a20-117">**INapSystemHealthValidationRequest2::GetConfigId**</span><span class="sxs-lookup"><span data-stu-id="43a20-117">**INapSystemHealthValidationRequest2::GetConfigId**</span></span>](inapsystemhealthvalidationrequest2-getconfigid.md) | <span data-ttu-id="43a20-118">Recupera l'ID configurazione in una richiesta di convalida.</span><span class="sxs-lookup"><span data-stu-id="43a20-118">Retrieves the configuration id in a validation request.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43a20-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="43a20-119">Remarks</span></span>

<span data-ttu-id="43a20-120">Se un servizio di convalida dell'integrità di sistema non supporta [**INapComponentConfig3**](inapcomponentconfig3.md), questa interfaccia non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="43a20-120">If an SHV doesn t support [**INapComponentConfig3**](inapcomponentconfig3.md), this interface doesn t apply.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a20-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43a20-121">Requirements</span></span>



| <span data-ttu-id="43a20-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a20-122">Requirement</span></span> | <span data-ttu-id="43a20-123">Valore</span><span class="sxs-lookup"><span data-stu-id="43a20-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a20-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43a20-124">Minimum supported client</span></span><br/> | <span data-ttu-id="43a20-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="43a20-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="43a20-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43a20-126">Minimum supported server</span></span><br/> | <span data-ttu-id="43a20-127">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="43a20-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="43a20-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43a20-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="43a20-129"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a20-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="43a20-130">IDL</span><span class="sxs-lookup"><span data-stu-id="43a20-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43a20-131"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43a20-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="43a20-132">DLL</span><span class="sxs-lookup"><span data-stu-id="43a20-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43a20-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43a20-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="43a20-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43a20-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a20-135">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="43a20-135">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[<span data-ttu-id="43a20-136">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="43a20-136">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="43a20-137">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="43a20-137">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 






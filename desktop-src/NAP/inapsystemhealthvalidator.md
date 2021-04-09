---
title: Interfaccia INapSystemHealthValidator (NapSystemHealthValidator. h)
description: Deve essere implementato dagli sviluppatori di servizio di convalida integrità per consentire al sistema NAP di comunicare con un servizio di convalida dell'integrità.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- NAP interfaccia INapSystemHealthValidator
- Interfaccia NAP di INapSystemHealthValidator, descrizione
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce4d47555926c2a3ad5b06315521fea23503d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740903"
---
# <a name="inapsystemhealthvalidator-interface"></a><span data-ttu-id="2617c-105">Interfaccia INapSystemHealthValidator</span><span class="sxs-lookup"><span data-stu-id="2617c-105">INapSystemHealthValidator interface</span></span>

> [!Note]  
> <span data-ttu-id="2617c-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="2617c-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2617c-107">**INapSystemHealthValidator** fornisce metodi che devono essere implementati dagli sviluppatori di servizio di convalida dell'integrità di sistema per consentire al sistema NAP di comunicare con un servizio di convalida dell'integrità</span><span class="sxs-lookup"><span data-stu-id="2617c-107">The **INapSystemHealthValidator** provides methods that must be implemented by SHV developers to enable the NAP system to communicate with an SHV.</span></span>

## <a name="members"></a><span data-ttu-id="2617c-108">Membri</span><span class="sxs-lookup"><span data-stu-id="2617c-108">Members</span></span>

<span data-ttu-id="2617c-109">L'interfaccia **INapSystemHealthValidator** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2617c-109">The **INapSystemHealthValidator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2617c-110">**INapSystemHealthValidator** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2617c-110">**INapSystemHealthValidator** also has these types of members:</span></span>

-   [<span data-ttu-id="2617c-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="2617c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2617c-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="2617c-112">Methods</span></span>

<span data-ttu-id="2617c-113">L'interfaccia **INapSystemHealthValidator** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2617c-113">The **INapSystemHealthValidator** interface has these methods.</span></span>



| <span data-ttu-id="2617c-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="2617c-114">Method</span></span>                                                                                   | <span data-ttu-id="2617c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2617c-115">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2617c-116">**INapSystemHealthValidator:: Validate**</span><span class="sxs-lookup"><span data-stu-id="2617c-116">**INapSystemHealthValidator::Validate**</span></span>](inapsystemhealthvalidator-validate-method.md) | <span data-ttu-id="2617c-117">Il sistema NAP chiama il metodo definito dall'applicazione per convalidare il [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ricevuto da un client.</span><span class="sxs-lookup"><span data-stu-id="2617c-117">The NAP system calls this application defined method to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="2617c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2617c-118">Requirements</span></span>



| <span data-ttu-id="2617c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2617c-119">Requirement</span></span> | <span data-ttu-id="2617c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2617c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2617c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2617c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2617c-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2617c-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="2617c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2617c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2617c-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2617c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2617c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2617c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2617c-126"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="2617c-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="2617c-127">IDL</span><span class="sxs-lookup"><span data-stu-id="2617c-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2617c-128"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2617c-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2617c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2617c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2617c-130">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="2617c-130">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="2617c-131">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="2617c-131">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 


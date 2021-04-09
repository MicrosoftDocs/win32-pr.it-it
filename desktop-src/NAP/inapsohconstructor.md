---
title: Interfaccia INapSoHConstructor (NapProtocol. h)
description: Vengono usati da SHAs per costruire SoHRequests e SHV per costruire SoHResponses.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- NAP interfaccia INapSoHConstructor
- Interfaccia NAP di INapSoHConstructor, descrizione
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546a6d3b4ec262fdd725af24211338e848b2b848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963821"
---
# <a name="inapsohconstructor-interface"></a><span data-ttu-id="cc0b0-105">Interfaccia INapSoHConstructor</span><span class="sxs-lookup"><span data-stu-id="cc0b0-105">INapSoHConstructor interface</span></span>

> [!Note]  
> <span data-ttu-id="cc0b0-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="cc0b0-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cc0b0-107">**INapSoHConstructor** fornisce i metodi usati da Shas per costruire [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) e SHV per costruire **SoHResponses**.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-107">The **INapSoHConstructor** provides methods that are used by SHAs to construct [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to construct **SoHResponses**.</span></span>

## <a name="members"></a><span data-ttu-id="cc0b0-108">Membri</span><span class="sxs-lookup"><span data-stu-id="cc0b0-108">Members</span></span>

<span data-ttu-id="cc0b0-109">L'interfaccia **INapSoHConstructor** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cc0b0-109">The **INapSoHConstructor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cc0b0-110">**INapSoHConstructor** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cc0b0-110">**INapSoHConstructor** also has these types of members:</span></span>

-   [<span data-ttu-id="cc0b0-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="cc0b0-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cc0b0-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="cc0b0-112">Methods</span></span>

<span data-ttu-id="cc0b0-113">L'interfaccia **INapSoHConstructor** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-113">The **INapSoHConstructor** interface has these methods.</span></span>



| <span data-ttu-id="cc0b0-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="cc0b0-114">Method</span></span>                                                                                   | <span data-ttu-id="cc0b0-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc0b0-115">Description</span></span>                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [<span data-ttu-id="cc0b0-116">**INapSoHConstructor:: AppendAttribute**</span><span class="sxs-lookup"><span data-stu-id="cc0b0-116">**INapSoHConstructor::AppendAttribute**</span></span>](inapsohconstructor-appendattribute-method.md) | <span data-ttu-id="cc0b0-117">Aggiunge un TLV alla fine del buffer del rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-117">Adds a TLV to the end of the SoH buffer.</span></span><br/> |
| [<span data-ttu-id="cc0b0-118">**INapSoHConstructor::GetSoH**</span><span class="sxs-lookup"><span data-stu-id="cc0b0-118">**INapSoHConstructor::GetSoH**</span></span>](inapsohconstructor-getsoh-method.md)                   | <span data-ttu-id="cc0b0-119">Recupera il pacchetto SoH costruito.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-119">Retrieves the constructed SoH packet.</span></span><br/>    |
| [<span data-ttu-id="cc0b0-120">**INapSoHConstructor:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="cc0b0-120">**INapSoHConstructor::Initialize**</span></span>](inapsohconstructor-initialize-method.md)           | <span data-ttu-id="cc0b0-121">Inizializza il pacchetto SoH.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-121">Initializes the SoH packet.</span></span><br/>              |
| [<span data-ttu-id="cc0b0-122">**INapSoHConstructor:: Validate**</span><span class="sxs-lookup"><span data-stu-id="cc0b0-122">**INapSoHConstructor::Validate**</span></span>](inapsohconstructor-validate-method.md)               | <span data-ttu-id="cc0b0-123">Verifica la validità del pacchetto SoH.</span><span class="sxs-lookup"><span data-stu-id="cc0b0-123">Checks the validity of the SoH packet.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="cc0b0-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc0b0-124">Requirements</span></span>



| <span data-ttu-id="cc0b0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc0b0-125">Requirement</span></span> | <span data-ttu-id="cc0b0-126">Valore</span><span class="sxs-lookup"><span data-stu-id="cc0b0-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc0b0-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc0b0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cc0b0-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc0b0-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cc0b0-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc0b0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cc0b0-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc0b0-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cc0b0-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc0b0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc0b0-132"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc0b0-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc0b0-133">IDL</span><span class="sxs-lookup"><span data-stu-id="cc0b0-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cc0b0-134"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cc0b0-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="cc0b0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="cc0b0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc0b0-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc0b0-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="cc0b0-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc0b0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc0b0-138">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="cc0b0-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="cc0b0-139">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="cc0b0-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 


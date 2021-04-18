---
title: Interfaccia INapComponentConfig (NapCommon. h)
description: Fornisce i metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV).
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- NAP interfaccia INapComponentConfig
- Interfaccia NAP di INapComponentConfig, descrizione
topic_type:
- apiref
api_name:
- INapComponentConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a13ae74ba1de79803ff4a2d3716eec7fe934a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400490"
---
# <a name="inapcomponentconfig-interface"></a><span data-ttu-id="8a219-105">Interfaccia INapComponentConfig</span><span class="sxs-lookup"><span data-stu-id="8a219-105">INapComponentConfig interface</span></span>

> [!Note]  
> <span data-ttu-id="8a219-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="8a219-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8a219-107">L'interfaccia **INapComponentConfig** fornisce i metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV).</span><span class="sxs-lookup"><span data-stu-id="8a219-107">The **INapComponentConfig** interface provides NAP system configuration methods for system health validators (SHVs).</span></span>

> [!Note]  
> <span data-ttu-id="8a219-108">[**INapComponentConfig2**](inapcomponentconfig2.md) e [**INapComponentConfig3**](inapcomponentconfig3.md) ereditano tutti i metodi di questa interfaccia e devono essere usati in alternativa.</span><span class="sxs-lookup"><span data-stu-id="8a219-108">[**INapComponentConfig2**](inapcomponentconfig2.md) and [**INapComponentConfig3**](inapcomponentconfig3.md) inherit all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="8a219-109">Membri</span><span class="sxs-lookup"><span data-stu-id="8a219-109">Members</span></span>

<span data-ttu-id="8a219-110">L'interfaccia **INapComponentConfig** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8a219-110">The **INapComponentConfig** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8a219-111">**INapComponentConfig** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8a219-111">**INapComponentConfig** also has these types of members:</span></span>

-   [<span data-ttu-id="8a219-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="8a219-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8a219-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="8a219-113">Methods</span></span>

<span data-ttu-id="8a219-114">L'interfaccia **INapComponentConfig** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8a219-114">The **INapComponentConfig** interface has these methods.</span></span>



| <span data-ttu-id="8a219-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="8a219-115">Method</span></span>                                                                          | <span data-ttu-id="8a219-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a219-116">Description</span></span>                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a219-117">**INapComponentConfig:: GetConfig**</span><span class="sxs-lookup"><span data-stu-id="8a219-117">**INapComponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)         | <span data-ttu-id="8a219-118">Recupera la configurazione del componente di convalida integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="8a219-118">Retrieves the SHV component configuration.</span></span><br/>                                |
| [<span data-ttu-id="8a219-119">**INapComponentConfig::InvokeUI**</span><span class="sxs-lookup"><span data-stu-id="8a219-119">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)           | <span data-ttu-id="8a219-120">Avvia l'interfaccia utente personalizzata per un componente di convalida integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="8a219-120">Launches the customized user interface for an SHV component.</span></span><br/>              |
| [<span data-ttu-id="8a219-121">**INapComponentConfig::IsUISupported**</span><span class="sxs-lookup"><span data-stu-id="8a219-121">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md) | <span data-ttu-id="8a219-122">Specifica se il componente di convalida integrità di sistema supporta un'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="8a219-122">Specifies whether the SHV component supports a customized user interface.</span></span><br/> |
| [<span data-ttu-id="8a219-123">**INapComponentConfig:: Seconfig**</span><span class="sxs-lookup"><span data-stu-id="8a219-123">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)         | <span data-ttu-id="8a219-124">Imposta la configurazione del componente di convalida integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="8a219-124">Sets the SHV component configuration.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="8a219-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a219-125">Remarks</span></span>

<span data-ttu-id="8a219-126">Questa interfaccia non deve essere implementata dagli agenti di integrità del sistema (SHAs) o dai client di imposizione di quarantena (QeC).</span><span class="sxs-lookup"><span data-stu-id="8a219-126">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a219-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a219-127">Requirements</span></span>



| <span data-ttu-id="8a219-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a219-128">Requirement</span></span> | <span data-ttu-id="8a219-129">Valore</span><span class="sxs-lookup"><span data-stu-id="8a219-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a219-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a219-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8a219-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8a219-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8a219-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a219-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8a219-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a219-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8a219-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a219-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a219-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a219-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a219-136">IDL</span><span class="sxs-lookup"><span data-stu-id="8a219-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8a219-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8a219-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a219-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a219-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a219-139">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="8a219-139">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8a219-140">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="8a219-140">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 


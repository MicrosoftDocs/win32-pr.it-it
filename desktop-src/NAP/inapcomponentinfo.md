---
title: Interfaccia INapComponentInfo (NapCommon. h)
description: Fornisce metodi che i componenti plug-in, ad esempio SHAs e SHV, devono implementare affinché il sistema NAP comunichi con loro.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- NAP interfaccia INapComponentInfo
- Interfaccia NAP di INapComponentInfo, descrizione
topic_type:
- apiref
api_name:
- INapComponentInfo
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba38c71cb79eb7222f619e6702008b31c41e7e2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964012"
---
# <a name="inapcomponentinfo-interface"></a><span data-ttu-id="4ed23-105">Interfaccia INapComponentInfo</span><span class="sxs-lookup"><span data-stu-id="4ed23-105">INapComponentInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="4ed23-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="4ed23-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4ed23-107">L'interfaccia **INapComponentInfo** fornisce metodi che i componenti plug-in, ad esempio Shas e SHV, devono implementare affinché il sistema NAP comunichi con loro.</span><span class="sxs-lookup"><span data-stu-id="4ed23-107">The **INapComponentInfo** interface provides methods that plug-in components (such as SHAs and SHVs) must implement for the NAP system to communicate with them.</span></span> <span data-ttu-id="4ed23-108">Il sistema NAP chiama l'implementazione di questi metodi per recuperare le informazioni amministrative statiche, ad esempio nome descrittivo o stringhe localizzate.</span><span class="sxs-lookup"><span data-stu-id="4ed23-108">The NAP system calls your implementation of these methods to retrieve static administrative information (for example, friendly name or localized strings).</span></span>

## <a name="members"></a><span data-ttu-id="4ed23-109">Membri</span><span class="sxs-lookup"><span data-stu-id="4ed23-109">Members</span></span>

<span data-ttu-id="4ed23-110">L'interfaccia **INapComponentInfo** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4ed23-110">The **INapComponentInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4ed23-111">**INapComponentInfo** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4ed23-111">**INapComponentInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="4ed23-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="4ed23-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4ed23-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="4ed23-113">Methods</span></span>

<span data-ttu-id="4ed23-114">L'interfaccia **INapComponentInfo** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4ed23-114">The **INapComponentInfo** interface has these methods.</span></span>



| <span data-ttu-id="4ed23-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="4ed23-115">Method</span></span>                                                                                                         | <span data-ttu-id="4ed23-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ed23-116">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ed23-117">**INapComponentInfo::ConvertErrorCodeToMessageId**</span><span class="sxs-lookup"><span data-stu-id="4ed23-117">**INapComponentInfo::ConvertErrorCodeToMessageId**</span></span>](inapcomponentinfo-converterrorcodetomessageid-method.md) | <span data-ttu-id="4ed23-118">Utilizzato dal sistema NAP per richiedere che il client di integrità converta un codice di errore HRESULT in un ID messaggio.</span><span class="sxs-lookup"><span data-stu-id="4ed23-118">Used by the NAP System to request the health client convert an HRESULT error code to a message ID.</span></span><br/> |
| [<span data-ttu-id="4ed23-119">**INapComponentInfo:: GetDescription**</span><span class="sxs-lookup"><span data-stu-id="4ed23-119">**INapComponentInfo::GetDescription**</span></span>](inapcomponentinfo-getdescription-method.md)                           | <span data-ttu-id="4ed23-120">Utilizzato dal sistema NAP per ottenere la descrizione di un client di integrità.</span><span class="sxs-lookup"><span data-stu-id="4ed23-120">Used by the NAP System to get the description of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="4ed23-121">**INapComponentInfo:: GetFriendlyName**</span><span class="sxs-lookup"><span data-stu-id="4ed23-121">**INapComponentInfo::GetFriendlyName**</span></span>](inapcomponentinfo-getfriendlyname-method.md)                         | <span data-ttu-id="4ed23-122">Utilizzato dal sistema NAP per ottenere il nome descrittivo di un client di integrità.</span><span class="sxs-lookup"><span data-stu-id="4ed23-122">Used by the NAP System to get the friendly name of a health client.</span></span><br/>                                |
| [<span data-ttu-id="4ed23-123">**INapComponentInfo:: GetIcon**</span><span class="sxs-lookup"><span data-stu-id="4ed23-123">**INapComponentInfo::GetIcon**</span></span>](inapcomponentinfo-geticon-method.md)                                         | <span data-ttu-id="4ed23-124">Utilizzato dal sistema NAP per ottenere l'icona di un client di integrità.</span><span class="sxs-lookup"><span data-stu-id="4ed23-124">Used by the NAP System to get the icon of a health client.</span></span><br/>                                         |
| [<span data-ttu-id="4ed23-125">**INapComponentInfo:: GetLocalizedString**</span><span class="sxs-lookup"><span data-stu-id="4ed23-125">**INapComponentInfo::GetLocalizedString**</span></span>](inapcomponentinfo-getlocalizedstring-method.md)                   | <span data-ttu-id="4ed23-126">Utilizzato dal sistema NAP per ottenere le stringhe localizzate.</span><span class="sxs-lookup"><span data-stu-id="4ed23-126">Used by the NAP System to get localized strings.</span></span><br/>                                                   |
| [<span data-ttu-id="4ed23-127">**INapComponentInfo:: getvendorname**</span><span class="sxs-lookup"><span data-stu-id="4ed23-127">**INapComponentInfo::GetVendorName**</span></span>](inapcomponentinfo-getvendorname-method.md)                             | <span data-ttu-id="4ed23-128">Utilizzato dal sistema NAP per ottenere il nome del fornitore di un client di integrità.</span><span class="sxs-lookup"><span data-stu-id="4ed23-128">Used by the NAP System to get the vendor name of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="4ed23-129">**INapComponentInfo:: GetVersion**</span><span class="sxs-lookup"><span data-stu-id="4ed23-129">**INapComponentInfo::GetVersion**</span></span>](inapcomponentinfo-getversion-method.md)                                   | <span data-ttu-id="4ed23-130">Utilizzato dal sistema NAP per ottenere la versione di un client di integrità.</span><span class="sxs-lookup"><span data-stu-id="4ed23-130">Used by the NAP System to get the version of a health client.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="4ed23-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ed23-131">Requirements</span></span>



| <span data-ttu-id="4ed23-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ed23-132">Requirement</span></span> | <span data-ttu-id="4ed23-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4ed23-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed23-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ed23-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4ed23-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ed23-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4ed23-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ed23-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4ed23-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4ed23-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4ed23-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ed23-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ed23-139"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ed23-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ed23-140">IDL</span><span class="sxs-lookup"><span data-stu-id="4ed23-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ed23-141"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ed23-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ed23-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ed23-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ed23-143">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="4ed23-143">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4ed23-144">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="4ed23-144">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 


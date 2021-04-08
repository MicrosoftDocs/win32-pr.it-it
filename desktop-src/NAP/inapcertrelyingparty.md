---
title: Interfaccia INapCertRelyingParty (NapCertRelyingParty. h)
description: 'Certificato: le relying party devono usare per comunicare con NapAgent.'
ms.assetid: e5ae0f4d-24fa-4049-82d9-1c9baeb34e32
keywords:
- NAP interfaccia INapCertRelyingParty
- Interfaccia NAP di INapCertRelyingParty, descrizione
topic_type:
- apiref
api_name:
- INapCertRelyingParty
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b4439389c6ee65076f710bb6ea752c73a51ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048535"
---
# <a name="inapcertrelyingparty-interface"></a><span data-ttu-id="19a67-105">Interfaccia INapCertRelyingParty</span><span class="sxs-lookup"><span data-stu-id="19a67-105">INapCertRelyingParty interface</span></span>

> [!Note]  
> <span data-ttu-id="19a67-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="19a67-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="19a67-107">L'interfaccia **INapCertRelyingParty** fornisce i metodi che devono essere usati dai relying party per comunicare con napagent.</span><span class="sxs-lookup"><span data-stu-id="19a67-107">The **INapCertRelyingParty** interface provides methods that certificate-relying parties must use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="19a67-108">Membri</span><span class="sxs-lookup"><span data-stu-id="19a67-108">Members</span></span>

<span data-ttu-id="19a67-109">L'interfaccia **INapCertRelyingParty** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="19a67-109">The **INapCertRelyingParty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="19a67-110">**INapCertRelyingParty** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="19a67-110">**INapCertRelyingParty** also has these types of members:</span></span>

-   [<span data-ttu-id="19a67-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="19a67-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="19a67-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="19a67-112">Methods</span></span>

<span data-ttu-id="19a67-113">L'interfaccia **INapCertRelyingParty** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="19a67-113">The **INapCertRelyingParty** interface has these methods.</span></span>



| <span data-ttu-id="19a67-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="19a67-114">Method</span></span>                                                                                                        | <span data-ttu-id="19a67-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19a67-115">Description</span></span>                                                                     |
|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="19a67-116">**INapCertRelyingParty::GetSubscribedRelyingParties**</span><span class="sxs-lookup"><span data-stu-id="19a67-116">**INapCertRelyingParty::GetSubscribedRelyingParties**</span></span>](inapcertrelyingparty-getsubscribedrelyingparties.md) | <span data-ttu-id="19a67-117">Ottiene un elenco di relying party che hanno sottoscritto.</span><span class="sxs-lookup"><span data-stu-id="19a67-117">Gets a list of relying parties that have subscribed.</span></span><br/>                 |
| [<span data-ttu-id="19a67-118">**INapCertRelyingParty::SubscribeCertByGroup**</span><span class="sxs-lookup"><span data-stu-id="19a67-118">**INapCertRelyingParty::SubscribeCertByGroup**</span></span>](inapcertrelyingparty-subscribecertbygroup.md)               | <span data-ttu-id="19a67-119">Sottoscrive un server di certificati di integrità già registrato (HCS).</span><span class="sxs-lookup"><span data-stu-id="19a67-119">Subscribes to an already-registered health certificate server (HCS).</span></span><br/> |
| [<span data-ttu-id="19a67-120">**INapCertRelyingParty::UnSubscribeCertByGroup**</span><span class="sxs-lookup"><span data-stu-id="19a67-120">**INapCertRelyingParty::UnSubscribeCertByGroup**</span></span>](inapcertrelyingparty-unsubscribecertbygroup.md)           | <span data-ttu-id="19a67-121">Annulla la sottoscrizione da un server HCS.</span><span class="sxs-lookup"><span data-stu-id="19a67-121">Unsubscribes from an HCS server.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="19a67-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19a67-122">Requirements</span></span>



| <span data-ttu-id="19a67-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="19a67-123">Requirement</span></span> | <span data-ttu-id="19a67-124">Valore</span><span class="sxs-lookup"><span data-stu-id="19a67-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a67-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19a67-125">Minimum supported client</span></span><br/> | <span data-ttu-id="19a67-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19a67-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="19a67-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19a67-127">Minimum supported server</span></span><br/> | <span data-ttu-id="19a67-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="19a67-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="19a67-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19a67-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="19a67-130"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="19a67-130"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="19a67-131">IDL</span><span class="sxs-lookup"><span data-stu-id="19a67-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19a67-132"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="19a67-132"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19a67-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19a67-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19a67-134">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="19a67-134">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="19a67-135">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="19a67-135">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 


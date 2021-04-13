---
title: Interfaccia INapServerCallback (NapSystemHealthValidator. h)
description: SHV utilizzare per segnalare il completamento asincrono della richiesta.
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- NAP interfaccia INapServerCallback
- Interfaccia NAP di INapServerCallback, descrizione
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18aaf900a603a577ec12835441c67c20453a5dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475268"
---
# <a name="inapservercallback-interface"></a><span data-ttu-id="aa7cd-105">Interfaccia INapServerCallback</span><span class="sxs-lookup"><span data-stu-id="aa7cd-105">INapServerCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="aa7cd-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="aa7cd-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="aa7cd-107">**INapServerCallback** fornisce un metodo che SHV USA per segnalare il completamento della richiesta asincrona.</span><span class="sxs-lookup"><span data-stu-id="aa7cd-107">The **INapServerCallback** provides a method that SHVs use to signal asynchronous request completion.</span></span>

## <a name="members"></a><span data-ttu-id="aa7cd-108">Membri</span><span class="sxs-lookup"><span data-stu-id="aa7cd-108">Members</span></span>

<span data-ttu-id="aa7cd-109">L'interfaccia **INapServerCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="aa7cd-109">The **INapServerCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aa7cd-110">**INapServerCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="aa7cd-110">**INapServerCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="aa7cd-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="aa7cd-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aa7cd-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="aa7cd-112">Methods</span></span>

<span data-ttu-id="aa7cd-113">L'interfaccia **INapServerCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="aa7cd-113">The **INapServerCallback** interface has these methods.</span></span>



| <span data-ttu-id="aa7cd-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="aa7cd-114">Method</span></span>                                                                         | <span data-ttu-id="aa7cd-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa7cd-115">Description</span></span>                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="aa7cd-116">**INapServerCallback:: OnComplete**</span><span class="sxs-lookup"><span data-stu-id="aa7cd-116">**INapServerCallback::OnComplete**</span></span>](inapservercallback-oncomplete-method.md) | <span data-ttu-id="aa7cd-117">Usato da SHV per segnalare il completamento della richiesta asincrona.</span><span class="sxs-lookup"><span data-stu-id="aa7cd-117">Used by SHVs to signal asynchronous request completion.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aa7cd-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa7cd-118">Requirements</span></span>



| <span data-ttu-id="aa7cd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa7cd-119">Requirement</span></span> | <span data-ttu-id="aa7cd-120">Valore</span><span class="sxs-lookup"><span data-stu-id="aa7cd-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa7cd-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa7cd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aa7cd-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="aa7cd-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="aa7cd-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa7cd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aa7cd-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa7cd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aa7cd-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa7cd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa7cd-126"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa7cd-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa7cd-127">IDL</span><span class="sxs-lookup"><span data-stu-id="aa7cd-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aa7cd-128"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aa7cd-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="aa7cd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="aa7cd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa7cd-130"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa7cd-130"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="aa7cd-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa7cd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa7cd-132">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="aa7cd-132">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="aa7cd-133">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="aa7cd-133">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 


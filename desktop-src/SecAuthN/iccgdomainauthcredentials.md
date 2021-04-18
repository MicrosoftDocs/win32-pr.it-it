---
description: Interfaccia implementata dal client che consente agli sviluppatori di fornire le proprie credenziali in modo dinamico in fase di esecuzione per autenticare i contenitori non aggiunti a un dominio con Active Directory.
title: Interfaccia ICcgDomainAuthCredentials (ccgplugins. h)
ms.topic: reference
ms.date: 10/20/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials
api_type:
- COM
api_location:
- ccgplugins.dll
ms.openlocfilehash: 8217f806ff0a1a6b38d045c7f665758ccaf8b1f5
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "106320822"
---
# <a name="iccgdomainauthcredentials-interface"></a><span data-ttu-id="e1ffe-103">Interfaccia ICcgDomainAuthCredentials</span><span class="sxs-lookup"><span data-stu-id="e1ffe-103">ICcgDomainAuthCredentials interface</span></span>

<span data-ttu-id="e1ffe-104">Interfaccia implementata dal client che consente agli sviluppatori di fornire le proprie credenziali in modo dinamico in fase di esecuzione per autenticare i contenitori non aggiunti a un dominio con Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e1ffe-104">A client-implemented interface that allows developers to supply their own credentials dynamically at run time to authenticate non-domain joined containers with Active Directory.</span></span> 

## <a name="members"></a><span data-ttu-id="e1ffe-105">Membri</span><span class="sxs-lookup"><span data-stu-id="e1ffe-105">Members</span></span>

<span data-ttu-id="e1ffe-106">L'interfaccia **ICcgDomainAuthCredentials** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e1ffe-106">The **ICcgDomainAuthCredentials** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e1ffe-107">**ICcgDomainAuthCredentials** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e1ffe-107">**ICcgDomainAuthCredentials** also has these types of members:</span></span>

-   [<span data-ttu-id="e1ffe-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="e1ffe-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e1ffe-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="e1ffe-109">Methods</span></span>

<span data-ttu-id="e1ffe-110">L'interfaccia **ICcgDomainAuthCredentials** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e1ffe-110">The **ICcgDomainAuthCredentials** interface has these methods.</span></span>



| <span data-ttu-id="e1ffe-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="e1ffe-111">Method</span></span>                                           | <span data-ttu-id="e1ffe-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1ffe-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1ffe-113">**GetPasswordCredentials**</span><span class="sxs-lookup"><span data-stu-id="e1ffe-113">**GetPasswordCredentials**</span></span>](iccgdomainauthcredentials-getpasswordcredentials.md)               | <span data-ttu-id="e1ffe-114">Restituisce le credenziali per autenticare un contenitore non appartenente a un dominio con Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e1ffe-114">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="e1ffe-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1ffe-115">Requirements</span></span>



| <span data-ttu-id="e1ffe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1ffe-116">Requirement</span></span> | <span data-ttu-id="e1ffe-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e1ffe-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ffe-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1ffe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e1ffe-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e1ffe-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e1ffe-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1ffe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e1ffe-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1ffe-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e1ffe-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1ffe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1ffe-123"><dt>ccgplugins. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1ffe-123"><dt>ccgplugins.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1ffe-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e1ffe-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="e1ffe-125"><dt>ccgplugins. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e1ffe-125"><dt>ccgplugins.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e1ffe-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e1ffe-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1ffe-127"><dt>ccgplugins.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1ffe-127"><dt>ccgplugins.dll</dt></span></span> </dl> |
| <span data-ttu-id="e1ffe-128">IID</span><span class="sxs-lookup"><span data-stu-id="e1ffe-128">IID</span></span><br/>                      | <span data-ttu-id="e1ffe-129">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="e1ffe-129">6ecda518-2010-4437-8bc3-46e752b7b172</span></span><br/>          |



 


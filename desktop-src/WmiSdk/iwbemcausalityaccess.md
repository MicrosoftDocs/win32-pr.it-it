---
description: Tiene traccia delle richieste figlio generate da una richiesta padre.
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: Interfaccia IWbemCausalityAccess (Wbemint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: db4c7a76b04b659cd467f7a4a7a9a8c1ba42721f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315721"
---
# <a name="iwbemcausalityaccess-interface"></a><span data-ttu-id="3e821-103">Interfaccia IWbemCausalityAccess</span><span class="sxs-lookup"><span data-stu-id="3e821-103">IWbemCausalityAccess interface</span></span>

<span data-ttu-id="3e821-104">L'interfaccia **IWbemCausalityAccess** tiene traccia delle richieste figlio generate da una richiesta padre.</span><span class="sxs-lookup"><span data-stu-id="3e821-104">The **IWbemCausalityAccess** interface keeps track of child requests that are generated from a parent request.</span></span> <span data-ttu-id="3e821-105">È possibile ottenere un oggetto **IWbemCausalityAccess** usando un'interfaccia di query (QI) per [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext).</span><span class="sxs-lookup"><span data-stu-id="3e821-105">You can obtain an **IWbemCausalityAccess** object by using a query interface (QI) for [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext).</span></span> <span data-ttu-id="3e821-106">Ogni richiesta viene identificata da un identificatore univoco globale (GUID) e può disporre di una richiesta padre oppure può essere una richiesta top.</span><span class="sxs-lookup"><span data-stu-id="3e821-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="3e821-107">Un GUID è un numero univoco a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="3e821-107">A GUID is a unique 128-bit number.</span></span> <span data-ttu-id="3e821-108">Ad esempio, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="3e821-108">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

## <a name="members"></a><span data-ttu-id="3e821-109">Membri</span><span class="sxs-lookup"><span data-stu-id="3e821-109">Members</span></span>

<span data-ttu-id="3e821-110">L'interfaccia **IWbemCausalityAccess** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3e821-110">The **IWbemCausalityAccess** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3e821-111">**IWbemCausalityAccess** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3e821-111">**IWbemCausalityAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="3e821-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="3e821-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3e821-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="3e821-113">Methods</span></span>

<span data-ttu-id="3e821-114">L'interfaccia **IWbemCausalityAccess** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3e821-114">The **IWbemCausalityAccess** interface has these methods.</span></span>



| <span data-ttu-id="3e821-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="3e821-115">Method</span></span>                                                    | <span data-ttu-id="3e821-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e821-116">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e821-117">**GetRequestId**</span><span class="sxs-lookup"><span data-stu-id="3e821-117">**GetRequestId**</span></span>](iwbemcausalityaccess-getrequestid.md) | <span data-ttu-id="3e821-118">Restituisce un identificatore GUID univoco per una richiesta.</span><span class="sxs-lookup"><span data-stu-id="3e821-118">Returns a unique GUID identifier for a request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="3e821-119">**IsChildOf**</span><span class="sxs-lookup"><span data-stu-id="3e821-119">**IsChildOf**</span></span>](iwbemcausalityaccess-ischildof.md)       | <span data-ttu-id="3e821-120">Determina se una richiesta è un elemento figlio di una richiesta padre specificata.</span><span class="sxs-lookup"><span data-stu-id="3e821-120">Determines if a request is a child of a specified parent request.</span></span> <span data-ttu-id="3e821-121">Una richiesta padre può avere più richieste figlio, ognuna identificata da un valore GUID univoco.</span><span class="sxs-lookup"><span data-stu-id="3e821-121">A parent request can have multiple child requests, each identified by a unique GUID value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3e821-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e821-122">Requirements</span></span>



| <span data-ttu-id="3e821-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e821-123">Requirement</span></span> | <span data-ttu-id="3e821-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3e821-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e821-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e821-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3e821-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e821-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e821-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e821-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3e821-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e821-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e821-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e821-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e821-130"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e821-130"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="3e821-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3e821-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e821-132"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e821-132"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e821-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e821-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e821-134">API COM per WMI</span><span class="sxs-lookup"><span data-stu-id="3e821-134">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> </dl>

 


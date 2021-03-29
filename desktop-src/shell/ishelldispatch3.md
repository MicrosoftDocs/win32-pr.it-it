---
description: Estende l'oggetto IShellDispatch2.
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: Oggetto IShellDispatch3 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 501b1396bd08ad8fd06f25da9b7030d4ce28d1e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978007"
---
# <a name="ishelldispatch3-object"></a><span data-ttu-id="92898-103">Oggetto IShellDispatch3</span><span class="sxs-lookup"><span data-stu-id="92898-103">IShellDispatch3 object</span></span>

<span data-ttu-id="92898-104">Estende l'oggetto [**IShellDispatch2**](ishelldispatch2-object.md) .</span><span class="sxs-lookup"><span data-stu-id="92898-104">Extends the [**IShellDispatch2**](ishelldispatch2-object.md) object.</span></span> <span data-ttu-id="92898-105">**IShellDispatch3** supporta un nuovo metodo, oltre alle proprietà e ai metodi supportati da **IShellDispatch2**.</span><span class="sxs-lookup"><span data-stu-id="92898-105">**IShellDispatch3** supports one new method in addition to the properties and methods supported by **IShellDispatch2**.</span></span>

> [!Note]  
> <span data-ttu-id="92898-106">**IShellDispatch3** viene implementato e accessibile tramite l'oggetto [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="92898-106">**IShellDispatch3** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="92898-107">Membri</span><span class="sxs-lookup"><span data-stu-id="92898-107">Members</span></span>

<span data-ttu-id="92898-108">L'oggetto **IShellDispatch3** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="92898-108">The **IShellDispatch3** object has these types of members:</span></span>

-   [<span data-ttu-id="92898-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="92898-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="92898-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="92898-110">Methods</span></span>

<span data-ttu-id="92898-111">L'oggetto **IShellDispatch3** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="92898-111">The **IShellDispatch3** object has these methods.</span></span>



| <span data-ttu-id="92898-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="92898-112">Method</span></span>                                             | <span data-ttu-id="92898-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92898-113">Description</span></span>                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="92898-114">**AddToRecent**</span><span class="sxs-lookup"><span data-stu-id="92898-114">**AddToRecent**</span></span>](ishelldispatch3-addtorecent.md) | <span data-ttu-id="92898-115">Aggiunge un file all'elenco degli ultimi elementi usati (MRU).</span><span class="sxs-lookup"><span data-stu-id="92898-115">Adds a file to the most recently used (MRU) list.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="92898-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="92898-116">Remarks</span></span>

<span data-ttu-id="92898-117">Per informazioni sui servizi Windows, vedere la documentazione relativa ai [Servizi](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="92898-117">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="92898-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92898-118">Requirements</span></span>



| <span data-ttu-id="92898-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="92898-119">Requirement</span></span> | <span data-ttu-id="92898-120">Valore</span><span class="sxs-lookup"><span data-stu-id="92898-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92898-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92898-121">Minimum supported client</span></span><br/> | <span data-ttu-id="92898-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="92898-122">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="92898-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92898-123">Minimum supported server</span></span><br/> | <span data-ttu-id="92898-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="92898-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="92898-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92898-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="92898-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="92898-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="92898-127">IDL</span><span class="sxs-lookup"><span data-stu-id="92898-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="92898-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="92898-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="92898-129">DLL</span><span class="sxs-lookup"><span data-stu-id="92898-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92898-130"><dt>Shell32.dll (versione 6,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="92898-130"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92898-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92898-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92898-132">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="92898-132">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="92898-133">**Oggetto Shell**</span><span class="sxs-lookup"><span data-stu-id="92898-133">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="92898-134">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="92898-134">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="92898-135">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="92898-135">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> </dl>

 

 

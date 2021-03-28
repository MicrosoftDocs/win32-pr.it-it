---
description: Estende l'oggetto IShellDispatch4.
title: Oggetto IShellDispatch5 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch5
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9170340a-0f11-4ec9-877d-fb7fef9888b2
ms.openlocfilehash: cbf3e960d7bfb9cd15411142cc036a21a9995ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977967"
---
# <a name="ishelldispatch5-object"></a><span data-ttu-id="ef929-103">Oggetto IShellDispatch5</span><span class="sxs-lookup"><span data-stu-id="ef929-103">IShellDispatch5 object</span></span>

<span data-ttu-id="ef929-104">Estende l'oggetto [**IShellDispatch4**](ishelldispatch4.md) .</span><span class="sxs-lookup"><span data-stu-id="ef929-104">Extends the [**IShellDispatch4**](ishelldispatch4.md) object.</span></span> <span data-ttu-id="ef929-105">Oltre alle proprietà e ai metodi supportati da **IShellDispatch4**, **IShellDispatch5** aggiunge un metodo che visualizza le finestre aperte in uno stack 3D.</span><span class="sxs-lookup"><span data-stu-id="ef929-105">In addition to the properties and methods supported by **IShellDispatch4**, **IShellDispatch5** adds a method that displays open windows in a 3D stack.</span></span>

> [!Note]  
> <span data-ttu-id="ef929-106">**IShellDispatch5** viene implementato e accessibile tramite l'oggetto [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="ef929-106">**IShellDispatch5** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="ef929-107">Membri</span><span class="sxs-lookup"><span data-stu-id="ef929-107">Members</span></span>

<span data-ttu-id="ef929-108">L'oggetto **IShellDispatch5** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ef929-108">The **IShellDispatch5** object has these types of members:</span></span>

-   [<span data-ttu-id="ef929-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ef929-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ef929-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="ef929-110">Methods</span></span>

<span data-ttu-id="ef929-111">L'oggetto **IShellDispatch5** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ef929-111">The **IShellDispatch5** object has these methods.</span></span>



| <span data-ttu-id="ef929-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="ef929-112">Method</span></span>                                                   | <span data-ttu-id="ef929-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef929-113">Description</span></span>                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="ef929-114">**Aperto WindowSwitcher**</span><span class="sxs-lookup"><span data-stu-id="ef929-114">**WindowSwitcher**</span></span>](ishelldispatch5-windowswitcher.md) | <span data-ttu-id="ef929-115">Consente di visualizzare le finestre aperte in uno stack 3D che è possibile scorrere.</span><span class="sxs-lookup"><span data-stu-id="ef929-115">Displays your open windows in a 3D stack that you can flip through.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ef929-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef929-116">Requirements</span></span>



| <span data-ttu-id="ef929-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef929-117">Requirement</span></span> | <span data-ttu-id="ef929-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ef929-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef929-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef929-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ef929-120">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ef929-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ef929-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef929-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ef929-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef929-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ef929-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef929-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef929-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef929-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ef929-125">IDL</span><span class="sxs-lookup"><span data-stu-id="ef929-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef929-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef929-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ef929-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ef929-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef929-128"><dt>Shell32.dll (versione 6,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="ef929-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef929-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef929-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef929-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ef929-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="ef929-131">**Oggetto Shell**</span><span class="sxs-lookup"><span data-stu-id="ef929-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="ef929-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="ef929-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="ef929-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="ef929-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="ef929-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="ef929-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="ef929-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="ef929-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> </dl>

 

 

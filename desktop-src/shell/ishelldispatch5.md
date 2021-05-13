---
description: Estende l'oggetto IShellDispatch4.
title: Oggetto IShellDispatch5 (Shldisp.h)
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
ms.openlocfilehash: 26c3112faa748aa443526fbe9cb493af67502cd7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843002"
---
# <a name="ishelldispatch5-object"></a><span data-ttu-id="28d31-103">Oggetto IShellDispatch5</span><span class="sxs-lookup"><span data-stu-id="28d31-103">IShellDispatch5 object</span></span>

<span data-ttu-id="28d31-104">Estende [**l'oggetto IShellDispatch4.**](ishelldispatch4.md)</span><span class="sxs-lookup"><span data-stu-id="28d31-104">Extends the [**IShellDispatch4**](ishelldispatch4.md) object.</span></span> <span data-ttu-id="28d31-105">Oltre alle proprietà e ai metodi supportati da **IShellDispatch4,** **IShellDispatch5** aggiunge un metodo che visualizza le finestre aperte in uno stack 3D.</span><span class="sxs-lookup"><span data-stu-id="28d31-105">In addition to the properties and methods supported by **IShellDispatch4**, **IShellDispatch5** adds a method that displays open windows in a 3D stack.</span></span>

> [!Note]  
> <span data-ttu-id="28d31-106">**IShellDispatch5 viene** implementato e accessibile tramite [**l'oggetto Shell.**](shell.md)</span><span class="sxs-lookup"><span data-stu-id="28d31-106">**IShellDispatch5** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="28d31-107">Membri</span><span class="sxs-lookup"><span data-stu-id="28d31-107">Members</span></span>

<span data-ttu-id="28d31-108">**L'oggetto IShellDispatch5** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="28d31-108">The **IShellDispatch5** object has these types of members:</span></span>

-   [<span data-ttu-id="28d31-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="28d31-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="28d31-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="28d31-110">Methods</span></span>

<span data-ttu-id="28d31-111">**L'oggetto IShellDispatch5** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="28d31-111">The **IShellDispatch5** object has these methods.</span></span>



| <span data-ttu-id="28d31-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="28d31-112">Method</span></span>                                                   | <span data-ttu-id="28d31-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28d31-113">Description</span></span>                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="28d31-114">**WindowSwitcher**</span><span class="sxs-lookup"><span data-stu-id="28d31-114">**WindowSwitcher**</span></span>](ishelldispatch5-windowswitcher.md) | <span data-ttu-id="28d31-115">Visualizza le finestre aperte in uno stack 3D che è possibile scorrere.</span><span class="sxs-lookup"><span data-stu-id="28d31-115">Displays your open windows in a 3D stack that you can flip through.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="28d31-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28d31-116">Requirements</span></span>



| <span data-ttu-id="28d31-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="28d31-117">Requirement</span></span> | <span data-ttu-id="28d31-118">Valore</span><span class="sxs-lookup"><span data-stu-id="28d31-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28d31-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28d31-119">Minimum supported client</span></span><br/> | <span data-ttu-id="28d31-120">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="28d31-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="28d31-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28d31-121">Minimum supported server</span></span><br/> | <span data-ttu-id="28d31-122">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="28d31-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="28d31-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28d31-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="28d31-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="28d31-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="28d31-125">Idl</span><span class="sxs-lookup"><span data-stu-id="28d31-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="28d31-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="28d31-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="28d31-127">DLL</span><span class="sxs-lookup"><span data-stu-id="28d31-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28d31-128"><dt>Shell32.dll (versione 6.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="28d31-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28d31-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28d31-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d31-130">**Idispatch**</span><span class="sxs-lookup"><span data-stu-id="28d31-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="28d31-131">**Oggetto shell**</span><span class="sxs-lookup"><span data-stu-id="28d31-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="28d31-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="28d31-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="28d31-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="28d31-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="28d31-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="28d31-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="28d31-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="28d31-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> </dl>

 

 

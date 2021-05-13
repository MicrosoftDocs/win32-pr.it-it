---
description: Estende l'oggetto IShellDispatch5.
title: Oggetto IShellDispatch6 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch6
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 540A5CFD-1520-4B61-B461-E893EFA27115
ms.openlocfilehash: de27322324dc8a25bdc679374e625f94a1d1a2ae
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843032"
---
# <a name="ishelldispatch6-object"></a><span data-ttu-id="ddc70-103">Oggetto IShellDispatch6</span><span class="sxs-lookup"><span data-stu-id="ddc70-103">IShellDispatch6 object</span></span>

<span data-ttu-id="ddc70-104">Estende [**l'oggetto IShellDispatch5.**](ishelldispatch5.md)</span><span class="sxs-lookup"><span data-stu-id="ddc70-104">Extends the [**IShellDispatch5**](ishelldispatch5.md) object.</span></span> <span data-ttu-id="ddc70-105">Oltre alle proprietà e ai metodi supportati da **IShellDispatch5,** **IShellDispatch6** aggiunge un metodo che visualizza il riquadro Ricerca app.</span><span class="sxs-lookup"><span data-stu-id="ddc70-105">In addition to the properties and methods supported by **IShellDispatch5**, **IShellDispatch6** adds a method that displays the Apps Search pane.</span></span>

> [!Note]  
> <span data-ttu-id="ddc70-106">**IShellDispatch6 viene** implementato e accessibile tramite [**l'oggetto Shell.**](shell.md)</span><span class="sxs-lookup"><span data-stu-id="ddc70-106">**IShellDispatch6** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="ddc70-107">Membri</span><span class="sxs-lookup"><span data-stu-id="ddc70-107">Members</span></span>

<span data-ttu-id="ddc70-108">**L'oggetto IShellDispatch6** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ddc70-108">The **IShellDispatch6** object has these types of members:</span></span>

-   [<span data-ttu-id="ddc70-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ddc70-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ddc70-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="ddc70-110">Methods</span></span>

<span data-ttu-id="ddc70-111">**L'oggetto IShellDispatch6** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ddc70-111">The **IShellDispatch6** object has these methods.</span></span>



| <span data-ttu-id="ddc70-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="ddc70-112">Method</span></span>                                                 | <span data-ttu-id="ddc70-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddc70-113">Description</span></span>                                                                                                                  |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddc70-114">**SearchCommand**</span><span class="sxs-lookup"><span data-stu-id="ddc70-114">**SearchCommand**</span></span>](ishelldispatch6-searchcommand.md) | <span data-ttu-id="ddc70-115">Visualizza il riquadro Ricerca app, che in genere viene visualizzato quando si inizia a digitare un termine di ricerca dal schermata Start.</span><span class="sxs-lookup"><span data-stu-id="ddc70-115">Displays the Apps Search pane, which normally appears when you begin to type a search term from the Start screen.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ddc70-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ddc70-116">Requirements</span></span>



| <span data-ttu-id="ddc70-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddc70-117">Requirement</span></span> | <span data-ttu-id="ddc70-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ddc70-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc70-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddc70-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ddc70-120">Windows 8 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ddc70-120">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ddc70-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddc70-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ddc70-122">Solo app desktop di Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ddc70-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ddc70-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ddc70-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddc70-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="ddc70-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ddc70-125">Idl</span><span class="sxs-lookup"><span data-stu-id="ddc70-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ddc70-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="ddc70-126"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="ddc70-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ddc70-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddc70-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddc70-128"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddc70-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddc70-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc70-130">**Idispatch**</span><span class="sxs-lookup"><span data-stu-id="ddc70-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="ddc70-131">**Oggetto Shell**</span><span class="sxs-lookup"><span data-stu-id="ddc70-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="ddc70-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="ddc70-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="ddc70-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="ddc70-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="ddc70-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="ddc70-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="ddc70-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="ddc70-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> <dt>

[<span data-ttu-id="ddc70-136">**IShellDispatch5**</span><span class="sxs-lookup"><span data-stu-id="ddc70-136">**IShellDispatch5**</span></span>](ishelldispatch5.md)
</dt> </dl>

 

 

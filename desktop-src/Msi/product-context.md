---
description: La proprietà di contesto restituisce il contesto di questo prodotto.
ms.assetid: aa772a95-eb4e-45af-9788-9833d62139e8
title: Proprietà Product. Context
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8334ca57d552681afeb77d0b213eca8b92bc1234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330275"
---
# <a name="productcontext-property"></a><span data-ttu-id="9a39d-103">Proprietà Product. Context</span><span class="sxs-lookup"><span data-stu-id="9a39d-103">Product.Context property</span></span>

<span data-ttu-id="9a39d-104">La proprietà di **contesto** restituisce il contesto di questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="9a39d-104">The **Context** property returns the context of this product.</span></span>

<span data-ttu-id="9a39d-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9a39d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a39d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a39d-106">Syntax</span></span>


```JScript
propVal = Product.Context
```



## <a name="property-value"></a><span data-ttu-id="9a39d-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9a39d-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="9a39d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a39d-108">Remarks</span></span>

<span data-ttu-id="9a39d-109">Questa proprietà può restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9a39d-109">This property can return one of the following values.</span></span>



| <span data-ttu-id="9a39d-110">Context</span><span class="sxs-lookup"><span data-stu-id="9a39d-110">Context</span></span>                        | <span data-ttu-id="9a39d-111">Valore</span><span class="sxs-lookup"><span data-stu-id="9a39d-111">Value</span></span> | <span data-ttu-id="9a39d-112">Significato</span><span class="sxs-lookup"><span data-stu-id="9a39d-112">Meaning</span></span>                           |
|--------------------------------|-------|-----------------------------------|
| <span data-ttu-id="9a39d-113">\_USERMANAGED MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="9a39d-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="9a39d-114">1</span><span class="sxs-lookup"><span data-stu-id="9a39d-114">1</span></span>     | <span data-ttu-id="9a39d-115">Prodotti in contesto gestito.</span><span class="sxs-lookup"><span data-stu-id="9a39d-115">Products under managed context.</span></span>   |
| <span data-ttu-id="9a39d-116">\_utente MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="9a39d-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="9a39d-117">2</span><span class="sxs-lookup"><span data-stu-id="9a39d-117">2</span></span>     | <span data-ttu-id="9a39d-118">Prodotti in contesto non gestito.</span><span class="sxs-lookup"><span data-stu-id="9a39d-118">Products under unmanaged context.</span></span> |
| <span data-ttu-id="9a39d-119">\_computer MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="9a39d-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="9a39d-120">4</span><span class="sxs-lookup"><span data-stu-id="9a39d-120">4</span></span>     | <span data-ttu-id="9a39d-121">Prodotti in contesto computer.</span><span class="sxs-lookup"><span data-stu-id="9a39d-121">Products under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="9a39d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a39d-122">Requirements</span></span>



| <span data-ttu-id="9a39d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a39d-123">Requirement</span></span> | <span data-ttu-id="9a39d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9a39d-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a39d-125">Versione</span><span class="sxs-lookup"><span data-stu-id="9a39d-125">Version</span></span><br/> | <span data-ttu-id="9a39d-126">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9a39d-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9a39d-127">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9a39d-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9a39d-128">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="9a39d-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="9a39d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9a39d-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="9a39d-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a39d-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="9a39d-131">IID</span><span class="sxs-lookup"><span data-stu-id="9a39d-131">IID</span></span><br/>     | <span data-ttu-id="9a39d-132">IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9a39d-132">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="9a39d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a39d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a39d-134">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="9a39d-134">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="9a39d-135">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="9a39d-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





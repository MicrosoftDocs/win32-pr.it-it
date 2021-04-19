---
description: La proprietà di contesto restituisce il contesto di questa patch.
ms.assetid: 09c92b0b-44f3-4355-8171-03da8ba32757
title: Proprietà patch. Context
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a6495b199046a361910741545a7178050621ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324776"
---
# <a name="patchcontext-property"></a><span data-ttu-id="2c849-103">Proprietà patch. Context</span><span class="sxs-lookup"><span data-stu-id="2c849-103">Patch.Context property</span></span>

<span data-ttu-id="2c849-104">La proprietà di **contesto** restituisce il contesto di questa patch.</span><span class="sxs-lookup"><span data-stu-id="2c849-104">The **Context** property returns the context of this patch.</span></span>

<span data-ttu-id="2c849-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2c849-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c849-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c849-106">Syntax</span></span>


```JScript
propVal = Patch.Context
```



## <a name="property-value"></a><span data-ttu-id="2c849-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2c849-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="2c849-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c849-108">Remarks</span></span>

<span data-ttu-id="2c849-109">Questa proprietà restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2c849-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="2c849-110">Context</span><span class="sxs-lookup"><span data-stu-id="2c849-110">Context</span></span>                        | <span data-ttu-id="2c849-111">Valore</span><span class="sxs-lookup"><span data-stu-id="2c849-111">Value</span></span> | <span data-ttu-id="2c849-112">Significato</span><span class="sxs-lookup"><span data-stu-id="2c849-112">Meaning</span></span>                        |
|--------------------------------|-------|--------------------------------|
| <span data-ttu-id="2c849-113">\_USERMANAGED MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="2c849-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="2c849-114">1</span><span class="sxs-lookup"><span data-stu-id="2c849-114">1</span></span>     | <span data-ttu-id="2c849-115">Patch sotto il contesto gestito.</span><span class="sxs-lookup"><span data-stu-id="2c849-115">Patch under managed context.</span></span>   |
| <span data-ttu-id="2c849-116">\_utente MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="2c849-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="2c849-117">2</span><span class="sxs-lookup"><span data-stu-id="2c849-117">2</span></span>     | <span data-ttu-id="2c849-118">Patch in un contesto non gestito.</span><span class="sxs-lookup"><span data-stu-id="2c849-118">Patch under unmanaged context.</span></span> |
| <span data-ttu-id="2c849-119">\_computer MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="2c849-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="2c849-120">4</span><span class="sxs-lookup"><span data-stu-id="2c849-120">4</span></span>     | <span data-ttu-id="2c849-121">Patch sotto il contesto del computer.</span><span class="sxs-lookup"><span data-stu-id="2c849-121">Patch under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="2c849-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c849-122">Requirements</span></span>



| <span data-ttu-id="2c849-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c849-123">Requirement</span></span> | <span data-ttu-id="2c849-124">Valore</span><span class="sxs-lookup"><span data-stu-id="2c849-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c849-125">Versione</span><span class="sxs-lookup"><span data-stu-id="2c849-125">Version</span></span><br/> | <span data-ttu-id="2c849-126">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2c849-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2c849-127">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2c849-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2c849-128">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2c849-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="2c849-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2c849-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="2c849-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c849-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="2c849-131">IID</span><span class="sxs-lookup"><span data-stu-id="2c849-131">IID</span></span><br/>     | <span data-ttu-id="2c849-132">IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2c849-132">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="2c849-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c849-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c849-134">**Patch (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="2c849-134">**Patch Object**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="2c849-135">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="2c849-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





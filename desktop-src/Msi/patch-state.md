---
description: La proprietà state restituisce lo stato di installazione di questa istanza della patch.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Proprietà patch. state
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f903ec66c2d55567fee9ccbc123e018e1dc7bacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332017"
---
# <a name="patchstate-property"></a><span data-ttu-id="bc050-103">Proprietà patch. state</span><span class="sxs-lookup"><span data-stu-id="bc050-103">Patch.State property</span></span>

<span data-ttu-id="bc050-104">La proprietà **state** restituisce lo stato di installazione di questa istanza della patch.</span><span class="sxs-lookup"><span data-stu-id="bc050-104">The **State** property returns the installation state of this instance of the patch.</span></span>

<span data-ttu-id="bc050-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bc050-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc050-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc050-106">Syntax</span></span>


```JScript
propVal = Patch.State
```



## <a name="property-value"></a><span data-ttu-id="bc050-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bc050-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="bc050-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc050-108">Remarks</span></span>

<span data-ttu-id="bc050-109">Questa proprietà restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bc050-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="bc050-110">Stato di installazione</span><span class="sxs-lookup"><span data-stu-id="bc050-110">Installation State</span></span>        | <span data-ttu-id="bc050-111">Significato</span><span class="sxs-lookup"><span data-stu-id="bc050-111">Meaning</span></span>                                                      |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bc050-112">MSIPATCHSTATE \_ applicato</span><span class="sxs-lookup"><span data-stu-id="bc050-112">MSIPATCHSTATE\_APPLIED</span></span>    | <span data-ttu-id="bc050-113">La patch viene applicata a questa istanza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="bc050-113">Patch is applied to this product instance.</span></span>                   |
| <span data-ttu-id="bc050-114">MSIPATCHSTATE \_ sostituito</span><span class="sxs-lookup"><span data-stu-id="bc050-114">MSIPATCHSTATE\_SUPERSEDED</span></span> | <span data-ttu-id="bc050-115">La patch viene applicata a questa istanza del prodotto, ma viene sostituita.</span><span class="sxs-lookup"><span data-stu-id="bc050-115">Patch is applied to this product instance but is superseded.</span></span> |
| <span data-ttu-id="bc050-116">MSIPATCHSTATE \_ obsoleto</span><span class="sxs-lookup"><span data-stu-id="bc050-116">MSIPATCHSTATE\_OBSOLETED</span></span>  | <span data-ttu-id="bc050-117">La patch viene applicata in questa istanza del prodotto ma è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="bc050-117">Patch is applied in this product instance but obsolete.</span></span>      |



 

<span data-ttu-id="bc050-118">Questo metodo può restituire \_ l'errore Unknown \_ patch, se l'oggetto [**patch**](patch-object.md) viene inizializzato con una stringa vuota per *ProductCode*.</span><span class="sxs-lookup"><span data-stu-id="bc050-118">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc050-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc050-119">Requirements</span></span>



| <span data-ttu-id="bc050-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc050-120">Requirement</span></span> | <span data-ttu-id="bc050-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bc050-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc050-122">Versione</span><span class="sxs-lookup"><span data-stu-id="bc050-122">Version</span></span><br/> | <span data-ttu-id="bc050-123">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bc050-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bc050-124">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bc050-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bc050-125">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="bc050-125">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="bc050-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bc050-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="bc050-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc050-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="bc050-128">IID</span><span class="sxs-lookup"><span data-stu-id="bc050-128">IID</span></span><br/>     | <span data-ttu-id="bc050-129">IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bc050-129">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="bc050-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc050-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc050-131">**Patch**</span><span class="sxs-lookup"><span data-stu-id="bc050-131">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="bc050-132">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="bc050-132">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="bc050-133">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="bc050-133">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





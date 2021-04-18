---
description: La proprietà state restituisce lo stato di installazione dell'istanza del prodotto.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Proprietà Product. state
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 64d2f5d39a516fc4a0c00b8e18c159e1f2496e22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330622"
---
# <a name="productstate-property"></a><span data-ttu-id="dc741-103">Proprietà Product. state</span><span class="sxs-lookup"><span data-stu-id="dc741-103">Product.State property</span></span>

<span data-ttu-id="dc741-104">La proprietà **state** restituisce lo stato di installazione dell'istanza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="dc741-104">The **State** property returns the installation state of this instance of the product.</span></span>

<span data-ttu-id="dc741-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="dc741-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc741-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc741-106">Syntax</span></span>


```JScript
propVal = Product.State
```



## <a name="property-value"></a><span data-ttu-id="dc741-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="dc741-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="dc741-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc741-108">Remarks</span></span>

<span data-ttu-id="dc741-109">Questa proprietà restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="dc741-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="dc741-110">Stato di installazione</span><span class="sxs-lookup"><span data-stu-id="dc741-110">Installation State</span></span>       | <span data-ttu-id="dc741-111">Significato</span><span class="sxs-lookup"><span data-stu-id="dc741-111">Meaning</span></span>                                |
|--------------------------|----------------------------------------|
| <span data-ttu-id="dc741-112">\_impostazione predefinita InstallState</span><span class="sxs-lookup"><span data-stu-id="dc741-112">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="dc741-113">Istanza del prodotto installata localmente.</span><span class="sxs-lookup"><span data-stu-id="dc741-113">Instance of product installed locally.</span></span> |
| <span data-ttu-id="dc741-114">INSTALLSTATE \_ annunciata</span><span class="sxs-lookup"><span data-stu-id="dc741-114">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="dc741-115">Istanza del prodotto annunciata.</span><span class="sxs-lookup"><span data-stu-id="dc741-115">Instance of product advertised.</span></span>        |
| <span data-ttu-id="dc741-116">INSTALLSTATE \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="dc741-116">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="dc741-117">Istanza del prodotto sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="dc741-117">Instance of product unknown.</span></span>           |



 

## <a name="requirements"></a><span data-ttu-id="dc741-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc741-118">Requirements</span></span>



| <span data-ttu-id="dc741-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc741-119">Requirement</span></span> | <span data-ttu-id="dc741-120">Valore</span><span class="sxs-lookup"><span data-stu-id="dc741-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc741-121">Versione</span><span class="sxs-lookup"><span data-stu-id="dc741-121">Version</span></span><br/> | <span data-ttu-id="dc741-122">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dc741-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dc741-123">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dc741-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dc741-124">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="dc741-124">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="dc741-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dc741-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="dc741-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc741-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="dc741-127">IID</span><span class="sxs-lookup"><span data-stu-id="dc741-127">IID</span></span><br/>     | <span data-ttu-id="dc741-128">IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dc741-128">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="dc741-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc741-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc741-130">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="dc741-130">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="dc741-131">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="dc741-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





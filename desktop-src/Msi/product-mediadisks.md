---
description: La proprietà MediaDisks enumera tutti i dischi multimediali per questa istanza del prodotto. Questa proprietà chiama MsiSourceListEnumMediaDisks. Restituisce le informazioni sul disco come una matrice di oggetti record.
ms.assetid: 9ea7c9a8-4ff1-4b26-a8d5-c23510650566
title: Proprietà Product. MediaDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e07af832837aaeb77759816c08cf68d04e14c255
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325887"
---
# <a name="productmediadisks-property"></a><span data-ttu-id="92916-105">Proprietà Product. MediaDisks</span><span class="sxs-lookup"><span data-stu-id="92916-105">Product.MediaDisks property</span></span>

<span data-ttu-id="92916-106">La proprietà **MediaDisks** enumera tutti i dischi multimediali per questa istanza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="92916-106">The **MediaDisks** property enumerates all the media disks for this product instance.</span></span> <span data-ttu-id="92916-107">Questa proprietà chiama [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span><span class="sxs-lookup"><span data-stu-id="92916-107">This property calls the [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span></span> <span data-ttu-id="92916-108">Restituisce le informazioni sul disco come una matrice di oggetti [**record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="92916-108">Returns the disk information as an array of [**Record**](record-object.md) objects.</span></span>

<span data-ttu-id="92916-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="92916-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="92916-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92916-110">Syntax</span></span>


```JScript
propVal = Product.MediaDisks
```



## <a name="property-value"></a><span data-ttu-id="92916-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="92916-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="92916-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="92916-112">Remarks</span></span>

<span data-ttu-id="92916-113">In ogni record, il primo campo contiene l'ID disco, il secondo campo contiene l'etichetta del volume e il terzo campo contiene il prompt del disco registrato per il disco.</span><span class="sxs-lookup"><span data-stu-id="92916-113">In each record, the first field contains the disk Id, the second field contains the volume label and the third field contains the disk prompt registered for the disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="92916-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92916-114">Requirements</span></span>



| <span data-ttu-id="92916-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="92916-115">Requirement</span></span> | <span data-ttu-id="92916-116">Valore</span><span class="sxs-lookup"><span data-stu-id="92916-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92916-117">Versione</span><span class="sxs-lookup"><span data-stu-id="92916-117">Version</span></span><br/> | <span data-ttu-id="92916-118">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="92916-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="92916-119">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="92916-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="92916-120">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="92916-120">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="92916-121">DLL</span><span class="sxs-lookup"><span data-stu-id="92916-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="92916-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92916-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="92916-123">IID</span><span class="sxs-lookup"><span data-stu-id="92916-123">IID</span></span><br/>     | <span data-ttu-id="92916-124">IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="92916-124">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="92916-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92916-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92916-126">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="92916-126">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="92916-127">**MsiSourceListEnumMediaDisks**</span><span class="sxs-lookup"><span data-stu-id="92916-127">**MsiSourceListEnumMediaDisks**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[<span data-ttu-id="92916-128">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="92916-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





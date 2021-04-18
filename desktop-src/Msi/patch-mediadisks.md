---
description: La proprietà MediaDisks enumera tutti i dischi multimediali per questa istanza del prodotto. Questa proprietà chiama MsiSourceListEnumMediaDisks. Restituisce le informazioni sul disco come matrice di oggetti record.
ms.assetid: 02faf211-16c8-4d2f-b192-c2ce8f3f2c66
title: Proprietà patch. MediaDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 40353ecce95cb0c4eb69228b004623bbb87c904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324773"
---
# <a name="patchmediadisks-property"></a><span data-ttu-id="d87b5-105">Proprietà patch. MediaDisks</span><span class="sxs-lookup"><span data-stu-id="d87b5-105">Patch.MediaDisks property</span></span>

<span data-ttu-id="d87b5-106">La proprietà **MediaDisks** enumera tutti i dischi multimediali per questa istanza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="d87b5-106">The **MediaDisks** property enumerates all the media disks for this product instance.</span></span> <span data-ttu-id="d87b5-107">Questa proprietà chiama [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span><span class="sxs-lookup"><span data-stu-id="d87b5-107">This property calls the [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span></span> <span data-ttu-id="d87b5-108">Restituisce le informazioni sul disco come matrice di oggetti [**record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d87b5-108">Returns the disk information as array of [**Record**](record-object.md) objects.</span></span>

<span data-ttu-id="d87b5-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d87b5-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d87b5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d87b5-110">Syntax</span></span>


```JScript
propVal = Patch.MediaDisks
```



## <a name="property-value"></a><span data-ttu-id="d87b5-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d87b5-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="d87b5-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d87b5-112">Remarks</span></span>

<span data-ttu-id="d87b5-113">In ogni record il primo campo contiene l'ID disco, il secondo campo contiene l'etichetta del volume e il terzo campo contiene il prompt del disco registrato per il disco.</span><span class="sxs-lookup"><span data-stu-id="d87b5-113">In each record the first field contains the disk Id, the second field contains the volume label and the third field contains the disk prompt registered for the disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="d87b5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d87b5-114">Requirements</span></span>



| <span data-ttu-id="d87b5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d87b5-115">Requirement</span></span> | <span data-ttu-id="d87b5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d87b5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d87b5-117">Versione</span><span class="sxs-lookup"><span data-stu-id="d87b5-117">Version</span></span><br/> | <span data-ttu-id="d87b5-118">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d87b5-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d87b5-119">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d87b5-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d87b5-120">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d87b5-120">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="d87b5-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d87b5-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="d87b5-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d87b5-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="d87b5-123">IID</span><span class="sxs-lookup"><span data-stu-id="d87b5-123">IID</span></span><br/>     | <span data-ttu-id="d87b5-124">IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d87b5-124">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="d87b5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d87b5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d87b5-126">**Patch**</span><span class="sxs-lookup"><span data-stu-id="d87b5-126">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="d87b5-127">**MsiSourceListEnumMediaDisks**</span><span class="sxs-lookup"><span data-stu-id="d87b5-127">**MsiSourceListEnumMediaDisks**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[<span data-ttu-id="d87b5-128">**Registra**</span><span class="sxs-lookup"><span data-stu-id="d87b5-128">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="d87b5-129">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="d87b5-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





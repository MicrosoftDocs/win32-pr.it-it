---
description: Il metodo SourceListClearMediaDisk dell'oggetto patch rimuove un disco specificato dal set di dischi registrati per una patch. Accetta DiskID come parametro. Questo metodo chiama MsiSourceListClearMediaDisk.
ms.assetid: fc52ecb9-2c79-497b-b551-0d3c4f584e86
title: Patch. SourceListClearMediaDisk, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 722b4573d89214312e77e4fde78e1905aefa885f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325901"
---
# <a name="patchsourcelistclearmediadisk-method"></a><span data-ttu-id="5e2b7-105">Patch. SourceListClearMediaDisk, metodo</span><span class="sxs-lookup"><span data-stu-id="5e2b7-105">Patch.SourceListClearMediaDisk method</span></span>

<span data-ttu-id="5e2b7-106">Il metodo **SourceListClearMediaDisk** dell'oggetto [**patch**](patch-object.md) rimuove un disco specificato dal set di dischi registrati per una patch.</span><span class="sxs-lookup"><span data-stu-id="5e2b7-106">The **SourceListClearMediaDisk** method of the [**Patch**](patch-object.md) object removes a specified disk from the set of registered disks for a patch.</span></span> <span data-ttu-id="5e2b7-107">Accetta *DiskID* come parametro.</span><span class="sxs-lookup"><span data-stu-id="5e2b7-107">Accepts *Diskid* as a parameter.</span></span> <span data-ttu-id="5e2b7-108">Questo metodo chiama [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span><span class="sxs-lookup"><span data-stu-id="5e2b7-108">This method calls [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e2b7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e2b7-109">Syntax</span></span>


```JScript
Patch.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a><span data-ttu-id="5e2b7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e2b7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e2b7-111">*DiskID*</span><span class="sxs-lookup"><span data-stu-id="5e2b7-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="5e2b7-112">Questo parametro fornisce l'ID del disco da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="5e2b7-112">This parameter provides the ID of the disk to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e2b7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e2b7-113">Return value</span></span>

<span data-ttu-id="5e2b7-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5e2b7-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e2b7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e2b7-115">Requirements</span></span>



| <span data-ttu-id="5e2b7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e2b7-116">Requirement</span></span> | <span data-ttu-id="5e2b7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5e2b7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e2b7-118">Versione</span><span class="sxs-lookup"><span data-stu-id="5e2b7-118">Version</span></span><br/> | <span data-ttu-id="5e2b7-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5e2b7-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5e2b7-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5e2b7-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5e2b7-121">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5e2b7-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="5e2b7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5e2b7-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="5e2b7-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e2b7-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="5e2b7-124">IID</span><span class="sxs-lookup"><span data-stu-id="5e2b7-124">IID</span></span><br/>     | <span data-ttu-id="5e2b7-125">IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5e2b7-125">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="5e2b7-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e2b7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e2b7-127">**Patch**</span><span class="sxs-lookup"><span data-stu-id="5e2b7-127">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="5e2b7-128">**MsiSourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="5e2b7-128">**MsiSourceListClearMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[<span data-ttu-id="5e2b7-129">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="5e2b7-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





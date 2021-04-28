---
description: 'Metodo Patch.SourceListAddMediaDisk: il metodo SourceListAddMediaDisk aggiunge un disco al set di dischi registrati. Accetta Diskid, VolumeLabel e DiskPrompt come parametri. Questo metodo chiama su MsiSourceListAddMediaDisk.'
ms.assetid: 6feaf2d3-7e39-4e22-9e74-9a2f98369eac
title: Metodo Patch.SourceListAddMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 052831befb95976358b53d989db36d5b2fa43efe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084374"
---
# <a name="patchsourcelistaddmediadisk-method"></a><span data-ttu-id="e2fd1-105">Metodo Patch.SourceListAddMediaDisk</span><span class="sxs-lookup"><span data-stu-id="e2fd1-105">Patch.SourceListAddMediaDisk method</span></span>

<span data-ttu-id="e2fd1-106">Il **metodo SourceListAddMediaDisk** aggiunge un disco al set di dischi registrati.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-106">The **SourceListAddMediaDisk** method adds a disk to the set of registered disks.</span></span> <span data-ttu-id="e2fd1-107">Accetta *Diskid,* *VolumeLabel e* *DiskPrompt* come parametri.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-107">Accepts *Diskid*, *VolumeLabel* and *DiskPrompt* as parameters.</span></span> <span data-ttu-id="e2fd1-108">Questo metodo chiama su [**MsiSourceListAddMediaDisk.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)</span><span class="sxs-lookup"><span data-stu-id="e2fd1-108">This method calls on [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2fd1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2fd1-109">Syntax</span></span>


```JScript
Patch.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a><span data-ttu-id="e2fd1-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2fd1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2fd1-111">*Diskid*</span><span class="sxs-lookup"><span data-stu-id="e2fd1-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="e2fd1-112">Questo parametro fornisce l'ID del disco da aggiungere o aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-112">This parameter provides the ID of the disk being added or updated.</span></span>

</dd> <dt>

<span data-ttu-id="e2fd1-113">*VolumeLabel*</span><span class="sxs-lookup"><span data-stu-id="e2fd1-113">*VolumeLabel*</span></span> 
</dt> <dd>

<span data-ttu-id="e2fd1-114">Questo parametro fornisce l'etichetta del disco da aggiungere o aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-114">This parameter provides the label of the disk being added or updated.</span></span> <span data-ttu-id="e2fd1-115">Un aggiornamento sovrascrive l'etichetta di volume esistente nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-115">An update, overwrites the existing volume label in the registry.</span></span> <span data-ttu-id="e2fd1-116">Per modificare solo il prompt del disco, ottenere l'etichetta del volume registrato esistente e specificarla insieme al prompt del nuovo disco.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-116">To change the disk prompt only, get the existing registered volume label and provide it along with the new disk prompt.</span></span> <span data-ttu-id="e2fd1-117">Una stringa NULL o vuota registra una stringa vuota (lunghezza di 0 byte) come etichetta di volume.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-117">A NULL or empty string registers an empty string (0 bytes in length) as the volume label.</span></span>

</dd> <dt>

<span data-ttu-id="e2fd1-118">*DiskPrompt*</span><span class="sxs-lookup"><span data-stu-id="e2fd1-118">*DiskPrompt*</span></span> 
</dt> <dd>

<span data-ttu-id="e2fd1-119">Questo parametro fornisce la richiesta del disco per l'aggiunta o l'aggiornamento del disco.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-119">This parameter provides the disk prompt of the disk being added or updated.</span></span> <span data-ttu-id="e2fd1-120">Un aggiornamento sovrascrive il prompt del disco esistente nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-120">An update overwrites the existing disk prompt in the registry.</span></span> <span data-ttu-id="e2fd1-121">Per modificare solo l'etichetta di volume, ottenere il prompt del disco esistente dal Registro di sistema e fornire la nuova etichetta di volume.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-121">To change the volume label only, get the existing disk prompt from the registry and provide it with the new volume label.</span></span> <span data-ttu-id="e2fd1-122">Una stringa NULL o vuota registra una stringa vuota (lunghezza di 0 byte) come richiesta del disco.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-122">A NULL or empty string registers an empty string (0 bytes in length) as the disk prompt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2fd1-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2fd1-123">Return value</span></span>

<span data-ttu-id="e2fd1-124">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-124">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2fd1-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2fd1-125">Requirements</span></span>



| <span data-ttu-id="e2fd1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2fd1-126">Requirement</span></span> | <span data-ttu-id="e2fd1-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e2fd1-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2fd1-128">Versione</span><span class="sxs-lookup"><span data-stu-id="e2fd1-128">Version</span></span><br/> | <span data-ttu-id="e2fd1-129">Windows Installer 5.0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e2fd1-130">Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e2fd1-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e2fd1-131">Windows Installer 3.0 o versione successiva in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e2fd1-131">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="e2fd1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e2fd1-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="e2fd1-133"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2fd1-133"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="e2fd1-134">IID</span><span class="sxs-lookup"><span data-stu-id="e2fd1-134">IID</span></span><br/>     | <span data-ttu-id="e2fd1-135">IPatch IID è definito come \_ 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e2fd1-135">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="e2fd1-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2fd1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2fd1-137">**Patch**</span><span class="sxs-lookup"><span data-stu-id="e2fd1-137">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="e2fd1-138">**MsiSourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="e2fd1-138">**MsiSourceListAddMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[<span data-ttu-id="e2fd1-139">Non supportato in Windows Installer 2.0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="e2fd1-139">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





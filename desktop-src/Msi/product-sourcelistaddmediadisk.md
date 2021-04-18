---
description: Il metodo SourceListAddMediaDisk aggiunge un disco al set di dischi registrati. Accetta i parametri DiskID, VolumeLabel e DiskPrompt. Questo metodo chiama su MsiSourceListAddMediaDisk.
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Metodo Product. SourceListAddMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d2f81b21570d708f361e45be7f6f42a93fd0d335
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325885"
---
# <a name="productsourcelistaddmediadisk-method"></a><span data-ttu-id="1ccab-105">Metodo Product. SourceListAddMediaDisk</span><span class="sxs-lookup"><span data-stu-id="1ccab-105">Product.SourceListAddMediaDisk method</span></span>

<span data-ttu-id="1ccab-106">Il metodo **SourceListAddMediaDisk** aggiunge un disco al set di dischi registrati.</span><span class="sxs-lookup"><span data-stu-id="1ccab-106">The **SourceListAddMediaDisk** method adds a disk to the set of registered disks.</span></span> <span data-ttu-id="1ccab-107">Accetta i parametri *DiskID*, *VolumeLabel* e *DiskPrompt* .</span><span class="sxs-lookup"><span data-stu-id="1ccab-107">Accepts *Diskid*, *VolumeLabel* and *DiskPrompt* as parameters.</span></span> <span data-ttu-id="1ccab-108">Questo metodo chiama su [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span><span class="sxs-lookup"><span data-stu-id="1ccab-108">This method calls on [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ccab-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ccab-109">Syntax</span></span>


```JScript
Product.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a><span data-ttu-id="1ccab-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ccab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ccab-111">*DiskID*</span><span class="sxs-lookup"><span data-stu-id="1ccab-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="1ccab-112">Questo parametro fornisce l'ID del disco da aggiungere o aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1ccab-112">This parameter provides the ID of the disk being added or updated.</span></span>

</dd> <dt>

<span data-ttu-id="1ccab-113">*VolumeLabel*</span><span class="sxs-lookup"><span data-stu-id="1ccab-113">*VolumeLabel*</span></span> 
</dt> <dd>

<span data-ttu-id="1ccab-114">Questo parametro fornisce l'etichetta del disco da aggiungere o aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1ccab-114">This parameter provides the label of the disk being added or updated.</span></span> <span data-ttu-id="1ccab-115">Un aggiornamento sovrascrive l'etichetta di volume esistente nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1ccab-115">An update overwrites the existing volume label in the registry.</span></span> <span data-ttu-id="1ccab-116">Per modificare solo il prompt del disco, ottenere l'etichetta del volume registrato esistente e fornirla insieme al nuovo prompt del disco.</span><span class="sxs-lookup"><span data-stu-id="1ccab-116">To change the disk prompt only, get the existing registered volume label and provide it along with the new disk prompt.</span></span> <span data-ttu-id="1ccab-117">Una stringa vuota per questo parametro registra una stringa vuota (di lunghezza 0 byte) come etichetta del volume.</span><span class="sxs-lookup"><span data-stu-id="1ccab-117">An empty string for this parameter registers an empty string (0 bytes in length) as the volume label.</span></span>

</dd> <dt>

<span data-ttu-id="1ccab-118">*DiskPrompt*</span><span class="sxs-lookup"><span data-stu-id="1ccab-118">*DiskPrompt*</span></span> 
</dt> <dd>

<span data-ttu-id="1ccab-119">Questo parametro fornisce la richiesta di disco del disco da aggiungere o aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1ccab-119">This parameter provides the disk prompt of the disk being added or updated.</span></span> <span data-ttu-id="1ccab-120">Un aggiornamento sovrascrive il prompt del disco esistente nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1ccab-120">An update overwrites the existing disk prompt in the registry.</span></span> <span data-ttu-id="1ccab-121">Per modificare solo l'etichetta del volume, ottenere la richiesta del disco esistente dal registro di sistema e fornirla con la nuova etichetta del volume.</span><span class="sxs-lookup"><span data-stu-id="1ccab-121">To change the volume label only, get the existing disk prompt from the registry and provide it with the new volume label.</span></span> <span data-ttu-id="1ccab-122">Una stringa vuota per questo parametro registra una stringa vuota (di lunghezza 0 byte) come richiesta del disco.</span><span class="sxs-lookup"><span data-stu-id="1ccab-122">An empty string for this parameter registers an empty string (0 bytes in length) as the disk prompt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ccab-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ccab-123">Return value</span></span>

<span data-ttu-id="1ccab-124">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1ccab-124">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ccab-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ccab-125">Requirements</span></span>



| <span data-ttu-id="1ccab-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ccab-126">Requirement</span></span> | <span data-ttu-id="1ccab-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1ccab-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccab-128">Versione</span><span class="sxs-lookup"><span data-stu-id="1ccab-128">Version</span></span><br/> | <span data-ttu-id="1ccab-129">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1ccab-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1ccab-130">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1ccab-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1ccab-131">Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="1ccab-131">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="1ccab-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1ccab-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="1ccab-133"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ccab-133"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="1ccab-134">IID</span><span class="sxs-lookup"><span data-stu-id="1ccab-134">IID</span></span><br/>     | <span data-ttu-id="1ccab-135">IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1ccab-135">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="1ccab-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ccab-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ccab-137">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="1ccab-137">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="1ccab-138">**MsiSourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="1ccab-138">**MsiSourceListAddMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[<span data-ttu-id="1ccab-139">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="1ccab-139">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





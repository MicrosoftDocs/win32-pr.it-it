---
description: Il metodo filehash dell'oggetto Installer accetta il percorso di un file e restituisce un hash a 128 bit del file. Le informazioni sull'hash del file vengono restituite come oggetto record. L'intero hash del file a 128 bit viene restituito come campi di Proprietà IntegerData a 4 32 bit.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Installer. filehash (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a38ef741c5c3a33c526cc78fbdc4551716ed3ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324626"
---
# <a name="installerfilehash-method"></a><span data-ttu-id="e959d-105">Installer. filehash (metodo)</span><span class="sxs-lookup"><span data-stu-id="e959d-105">Installer.FileHash method</span></span>

<span data-ttu-id="e959d-106">Il metodo **filehash** dell' [**oggetto Installer**](installer-object.md) accetta il percorso di un file e restituisce un hash a 128 bit del file.</span><span class="sxs-lookup"><span data-stu-id="e959d-106">The **FileHash** method of the [**Installer Object**](installer-object.md) takes the path to a file and returns a 128-bit hash of that file.</span></span> <span data-ttu-id="e959d-107">Le informazioni sull'hash del file vengono restituite come [**oggetto record**](record-object.md).</span><span class="sxs-lookup"><span data-stu-id="e959d-107">The file hash information is returned as a [**Record Object**](record-object.md).</span></span> <span data-ttu-id="e959d-108">L'intero hash del file a 128 bit viene restituito come campi di proprietà [**IntegerData**](record-integerdata.md) a 4 32 bit.</span><span class="sxs-lookup"><span data-stu-id="e959d-108">The entire 128-bit file hash is returned as four 32-bit [**IntegerData**](record-integerdata.md) property fields.</span></span>

<span data-ttu-id="e959d-109">I valori restituiti nell' [**oggetto record**](record-object.md) corrispondono ai quattro campi della struttura [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) restituita da [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span><span class="sxs-lookup"><span data-stu-id="e959d-109">The values returned in the [**Record Object**](record-object.md) correspond to the four fields of the [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) structure returned by [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="e959d-110">La numerazione di quattro campi è basata su 1 nella [tabella MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="e959d-110">The numbering of four fields is 1-based in the [MsiFileHash Table](msifilehash-table.md).</span></span>

-   <span data-ttu-id="e959d-111">Il campo 1 corrisponde alla colonna HashPart1.</span><span class="sxs-lookup"><span data-stu-id="e959d-111">Field 1 corresponds to the HashPart1 column.</span></span>
-   <span data-ttu-id="e959d-112">Il campo 2 corrisponde alla colonna HashPart2.</span><span class="sxs-lookup"><span data-stu-id="e959d-112">Field 2 corresponds to the HashPart2 column.</span></span>
-   <span data-ttu-id="e959d-113">Il campo 3 corrisponde alla colonna HashPart3.</span><span class="sxs-lookup"><span data-stu-id="e959d-113">Field 3 corresponds to the HashPart3 column.</span></span>
-   <span data-ttu-id="e959d-114">Il campo 4 corrisponde alla colonna HashPart4.</span><span class="sxs-lookup"><span data-stu-id="e959d-114">Field 4 corresponds to the HashPart4 column.</span></span>

## <a name="syntax"></a><span data-ttu-id="e959d-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e959d-115">Syntax</span></span>


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a><span data-ttu-id="e959d-116">Parametri</span><span class="sxs-lookup"><span data-stu-id="e959d-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e959d-117">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="e959d-117">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="e959d-118">Percorso del file di cui eseguire l'hashing.</span><span class="sxs-lookup"><span data-stu-id="e959d-118">Path to the file that is to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="e959d-119">*Opzioni*</span><span class="sxs-lookup"><span data-stu-id="e959d-119">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="e959d-120">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="e959d-120">Reserved for future use.</span></span>

<span data-ttu-id="e959d-121">Il valore di questo parametro deve essere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e959d-121">The value of this parameter must be 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e959d-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e959d-122">Return value</span></span>

<span data-ttu-id="e959d-123">Se ha esito positivo, questo metodo restituisce un [**oggetto record**](record-object.md) contenente l'hash del file.</span><span class="sxs-lookup"><span data-stu-id="e959d-123">If successful, this method returns a [**Record Object**](record-object.md) that contains the hash of the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="e959d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e959d-124">Requirements</span></span>



| <span data-ttu-id="e959d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e959d-125">Requirement</span></span> | <span data-ttu-id="e959d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e959d-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e959d-127">Versione</span><span class="sxs-lookup"><span data-stu-id="e959d-127">Version</span></span><br/> | <span data-ttu-id="e959d-128">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e959d-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e959d-129">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e959d-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e959d-130">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="e959d-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e959d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e959d-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="e959d-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e959d-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e959d-133">IID</span><span class="sxs-lookup"><span data-stu-id="e959d-133">IID</span></span><br/>     | <span data-ttu-id="e959d-134">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e959d-134">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="e959d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e959d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e959d-136">Controllo delle versioni dei file predefinito</span><span class="sxs-lookup"><span data-stu-id="e959d-136">Default File Versioning</span></span>](default-file-versioning.md)
</dt> <dt>

[<span data-ttu-id="e959d-137">Gestire le dimensioni e le versioni dei file</span><span class="sxs-lookup"><span data-stu-id="e959d-137">Manage File Sizes and Versions</span></span>](manage-file-sizes-and-versions.md)
</dt> <dt>

[<span data-ttu-id="e959d-138">Tabella MsiFileHash</span><span class="sxs-lookup"><span data-stu-id="e959d-138">MsiFileHash Table</span></span>](msifilehash-table.md)
</dt> <dt>

[<span data-ttu-id="e959d-139">**MsiGetFileHash**</span><span class="sxs-lookup"><span data-stu-id="e959d-139">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 





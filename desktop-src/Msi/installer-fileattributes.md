---
description: La proprietà FileAttributes dell'oggetto Installer restituisce un numero che rappresenta gli attributi di file combinati per il percorso designato di un file o di una cartella.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Proprietà Installer. FileAttributes (Windows. storage. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9a4d2b956c7d325fabcda7d6950274249120a0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324627"
---
# <a name="installerfileattributes-property"></a><span data-ttu-id="2d70a-103">Proprietà Installer. FileAttributes</span><span class="sxs-lookup"><span data-stu-id="2d70a-103">Installer.FileAttributes property</span></span>

<span data-ttu-id="2d70a-104">La proprietà **FileAttributes** dell'oggetto [**Installer**](installer-object.md) restituisce un numero che rappresenta gli attributi di file combinati per il percorso designato di un file o di una cartella.</span><span class="sxs-lookup"><span data-stu-id="2d70a-104">The **FileAttributes** property of the [**Installer**](installer-object.md) object returns a number representing the combined file attributes for the designated path to a file or folder.</span></span>

<span data-ttu-id="2d70a-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2d70a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d70a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d70a-106">Syntax</span></span>


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a><span data-ttu-id="2d70a-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2d70a-107">Property value</span></span>

<span data-ttu-id="2d70a-108">Percorso necessario del file o della cartella.</span><span class="sxs-lookup"><span data-stu-id="2d70a-108">The required path to the file or folder.</span></span> <span data-ttu-id="2d70a-109">Un percorso parziale presuppone la directory corrente.</span><span class="sxs-lookup"><span data-stu-id="2d70a-109">A partial path assumes the current directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d70a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d70a-110">Remarks</span></span>

<span data-ttu-id="2d70a-111">La proprietà **FileAttributes** restituisce i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2d70a-111">The **FileAttributes** property returns the following values.</span></span>



| <span data-ttu-id="2d70a-112">Attributo file</span><span class="sxs-lookup"><span data-stu-id="2d70a-112">File attribute</span></span>              | <span data-ttu-id="2d70a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="2d70a-113">Value</span></span>      | <span data-ttu-id="2d70a-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2d70a-114">Value</span></span> |
|-----------------------------|------------|-------|
| <span data-ttu-id="2d70a-115">FILE\_ATTRIBUTE\_READONLY</span><span class="sxs-lookup"><span data-stu-id="2d70a-115">FILE\_ATTRIBUTE\_READONLY</span></span>   | <span data-ttu-id="2d70a-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d70a-116">0x00000001</span></span> | <span data-ttu-id="2d70a-117">1</span><span class="sxs-lookup"><span data-stu-id="2d70a-117">1</span></span>     |
| <span data-ttu-id="2d70a-118">FILE\_ATTRIBUTE\_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="2d70a-118">FILE\_ATTRIBUTE\_HIDDEN</span></span>     | <span data-ttu-id="2d70a-119">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2d70a-119">0x00000002</span></span> | <span data-ttu-id="2d70a-120">2</span><span class="sxs-lookup"><span data-stu-id="2d70a-120">2</span></span>     |
| <span data-ttu-id="2d70a-121">FILE\_ATTRIBUTE\_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="2d70a-121">FILE\_ATTRIBUTE\_SYSTEM</span></span>     | <span data-ttu-id="2d70a-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2d70a-122">0x00000004</span></span> | <span data-ttu-id="2d70a-123">4</span><span class="sxs-lookup"><span data-stu-id="2d70a-123">4</span></span>     |
| <span data-ttu-id="2d70a-124">FILE\_ATTRIBUTE\_DIRECTORY</span><span class="sxs-lookup"><span data-stu-id="2d70a-124">FILE\_ATTRIBUTE\_DIRECTORY</span></span>  | <span data-ttu-id="2d70a-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d70a-125">0x00000010</span></span> | <span data-ttu-id="2d70a-126">16</span><span class="sxs-lookup"><span data-stu-id="2d70a-126">16</span></span>    |
| <span data-ttu-id="2d70a-127">\_attributo file \_ temporaneo</span><span class="sxs-lookup"><span data-stu-id="2d70a-127">FILE\_ATTRIBUTE\_TEMPORARY</span></span>  | <span data-ttu-id="2d70a-128">0x00000100</span><span class="sxs-lookup"><span data-stu-id="2d70a-128">0x00000100</span></span> | <span data-ttu-id="2d70a-129">256</span><span class="sxs-lookup"><span data-stu-id="2d70a-129">256</span></span>   |
| <span data-ttu-id="2d70a-130">FILE\_ATTRIBUTE\_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="2d70a-130">FILE\_ATTRIBUTE\_COMPRESSED</span></span> | <span data-ttu-id="2d70a-131">0x00000800</span><span class="sxs-lookup"><span data-stu-id="2d70a-131">0x00000800</span></span> | <span data-ttu-id="2d70a-132">2048</span><span class="sxs-lookup"><span data-stu-id="2d70a-132">2048</span></span>  |
| <span data-ttu-id="2d70a-133">FILE\_ATTRIBUTE\_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="2d70a-133">FILE\_ATTRIBUTE\_OFFLINE</span></span>    | <span data-ttu-id="2d70a-134">0x00001000</span><span class="sxs-lookup"><span data-stu-id="2d70a-134">0x00001000</span></span> | <span data-ttu-id="2d70a-135">4096</span><span class="sxs-lookup"><span data-stu-id="2d70a-135">4096</span></span>  |



 

<span data-ttu-id="2d70a-136">Restituisce-1 se il file o la cartella non esiste o non è accessibile.</span><span class="sxs-lookup"><span data-stu-id="2d70a-136">Returns –1 if the file or folder does not exist or is not accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d70a-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d70a-137">Requirements</span></span>



| <span data-ttu-id="2d70a-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d70a-138">Requirement</span></span> | <span data-ttu-id="2d70a-139">Valore</span><span class="sxs-lookup"><span data-stu-id="2d70a-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d70a-140">Versione</span><span class="sxs-lookup"><span data-stu-id="2d70a-140">Version</span></span><br/> | <span data-ttu-id="2d70a-141">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2d70a-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2d70a-142">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2d70a-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2d70a-143">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="2d70a-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2d70a-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d70a-144">Header</span></span><br/>  | <dl> <span data-ttu-id="2d70a-145"><dt>Windows. storage. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d70a-145"><dt>Windows.storage.h</dt></span></span> </dl>                                                                                                                                                            |
| <span data-ttu-id="2d70a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="2d70a-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="2d70a-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d70a-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2d70a-148">IID</span><span class="sxs-lookup"><span data-stu-id="2d70a-148">IID</span></span><br/>     | <span data-ttu-id="2d70a-149">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2d70a-149">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 





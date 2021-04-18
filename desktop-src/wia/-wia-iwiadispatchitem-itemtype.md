---
description: Tipo di questo elemento. Di sola lettura.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Proprietà Item. ItemType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ItemType
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9b70f7a1698ecdb4de023786f21a6ef9d55f681d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312408"
---
# <a name="itemitemtype-property"></a><span data-ttu-id="8c414-104">Proprietà Item. ItemType</span><span class="sxs-lookup"><span data-stu-id="8c414-104">Item.ItemType property</span></span>

<span data-ttu-id="8c414-105">Tipo di questo elemento.</span><span class="sxs-lookup"><span data-stu-id="8c414-105">The type of this item.</span></span> <span data-ttu-id="8c414-106">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="8c414-106">Read-only.</span></span>

<span data-ttu-id="8c414-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="8c414-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c414-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c414-108">Syntax</span></span>


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a><span data-ttu-id="8c414-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8c414-109">Property value</span></span>

<span data-ttu-id="8c414-110">Sono possibili i seguenti valori:</span><span class="sxs-lookup"><span data-stu-id="8c414-110">The following values are possible:</span></span>



| <span data-ttu-id="8c414-111">Valore</span><span class="sxs-lookup"><span data-stu-id="8c414-111">Value</span></span>  | <span data-ttu-id="8c414-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c414-112">Description</span></span>                                     |
|--------|-------------------------------------------------|
| <span data-ttu-id="8c414-113">device</span><span class="sxs-lookup"><span data-stu-id="8c414-113">device</span></span> | <span data-ttu-id="8c414-114">L'elemento è un dispositivo hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="8c414-114">The item is a WIA hardware device.</span></span>              |
| <span data-ttu-id="8c414-115">folder</span><span class="sxs-lookup"><span data-stu-id="8c414-115">folder</span></span> | <span data-ttu-id="8c414-116">L'elemento è una cartella che contiene altri elementi.</span><span class="sxs-lookup"><span data-stu-id="8c414-116">The item is a folder that contains other items.</span></span> |
| <span data-ttu-id="8c414-117">file</span><span class="sxs-lookup"><span data-stu-id="8c414-117">file</span></span>   | <span data-ttu-id="8c414-118">L'elemento è un'immagine o un file audio.</span><span class="sxs-lookup"><span data-stu-id="8c414-118">The item is an image or audio file.</span></span>             |
| <span data-ttu-id="8c414-119">Audio</span><span class="sxs-lookup"><span data-stu-id="8c414-119">audio</span></span>  | <span data-ttu-id="8c414-120">L'elemento è un clip audio.</span><span class="sxs-lookup"><span data-stu-id="8c414-120">The item is an audio clip.</span></span>                      |
| <span data-ttu-id="8c414-121">image</span><span class="sxs-lookup"><span data-stu-id="8c414-121">image</span></span>  | <span data-ttu-id="8c414-122">L'elemento è un'immagine.</span><span class="sxs-lookup"><span data-stu-id="8c414-122">The item is an image.</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="8c414-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c414-123">Remarks</span></span>

<span data-ttu-id="8c414-124">Un elemento può avere più di un tipo.</span><span class="sxs-lookup"><span data-stu-id="8c414-124">An item can have more than one type.</span></span> <span data-ttu-id="8c414-125">Ogni immagine, ad esempio, è di tipo "image" e "file".</span><span class="sxs-lookup"><span data-stu-id="8c414-125">For example, every image is of both "image" and "file" types.</span></span> <span data-ttu-id="8c414-126">**ItemType** restituisce una stringa che include tutti i tipi validi per l'elemento, separati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="8c414-126">**ItemType** returns a string that includes all valid types for the item, separated by semicolons.</span></span> <span data-ttu-id="8c414-127">Ad esempio, "image; file".</span><span class="sxs-lookup"><span data-stu-id="8c414-127">For example, "image;file".</span></span> <span data-ttu-id="8c414-128">Non sono presenti spazi in questa stringa e non è presente un punto e virgola alla fine.</span><span class="sxs-lookup"><span data-stu-id="8c414-128">There are no spaces in this string, and there is not a semicolon at the end.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c414-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c414-129">Requirements</span></span>



| <span data-ttu-id="8c414-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c414-130">Requirement</span></span> | <span data-ttu-id="8c414-131">Valore</span><span class="sxs-lookup"><span data-stu-id="8c414-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c414-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c414-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8c414-133">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8c414-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c414-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c414-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8c414-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8c414-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8c414-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8c414-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c414-137"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="8c414-137"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 





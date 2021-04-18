---
title: Struttura WMDMMetadataView
description: La struttura WMDMMetadataView definisce la visualizzazione dei metadati. Il contenuto è organizzato in base a questa definizione.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- Struttura WMDMMetadataView Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aa38a8fe7f19137c5caff18417d48ea23168b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324402"
---
# <a name="wmdmmetadataview-structure"></a><span data-ttu-id="ca4b8-105">Struttura WMDMMetadataView</span><span class="sxs-lookup"><span data-stu-id="ca4b8-105">WMDMMetadataView structure</span></span>

<span data-ttu-id="ca4b8-106">La struttura **WMDMMetadataView** definisce la visualizzazione dei metadati.</span><span class="sxs-lookup"><span data-stu-id="ca4b8-106">The **WMDMMetadataView** structure defines the metadata view.</span></span> <span data-ttu-id="ca4b8-107">Il contenuto è organizzato in base a questa definizione.</span><span class="sxs-lookup"><span data-stu-id="ca4b8-107">Content is organized based on this definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca4b8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca4b8-108">Syntax</span></span>


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a><span data-ttu-id="ca4b8-109">Members</span><span class="sxs-lookup"><span data-stu-id="ca4b8-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca4b8-110">**pwszViewName**</span><span class="sxs-lookup"><span data-stu-id="ca4b8-110">**pwszViewName**</span></span>
</dt> <dd>

<span data-ttu-id="ca4b8-111">Puntatore a una stringa a caratteri wide con terminazione null che contiene il nome della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ca4b8-111">Pointer to a wide-character null-terminated string containing the name of the view.</span></span> <span data-ttu-id="ca4b8-112">Viene utilizzato come nome del nodo radice in cui viene presentata la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ca4b8-112">This is used as the name of the root node under which this view is presented.</span></span>

</dd> <dt>

<span data-ttu-id="ca4b8-113">**nDepth**</span><span class="sxs-lookup"><span data-stu-id="ca4b8-113">**nDepth**</span></span>
</dt> <dd>

<span data-ttu-id="ca4b8-114">Integer contenente la profondità della visualizzazione, che indica il numero di tag di metadati annidati utilizzati per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ca4b8-114">Integer containing the depth of the view, which indicates how many nested metadata tags are used for the view.</span></span>

</dd> <dt>

<span data-ttu-id="ca4b8-115">**ppwszTags**</span><span class="sxs-lookup"><span data-stu-id="ca4b8-115">**ppwszTags**</span></span>
</dt> <dd>

<span data-ttu-id="ca4b8-116">Matrice di stringhe di tag dei metadati per i tag annidati.</span><span class="sxs-lookup"><span data-stu-id="ca4b8-116">Array of metadata tag strings for the nested tags.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ca4b8-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="ca4b8-117">Examples</span></span>

<span data-ttu-id="ca4b8-118">Il codice seguente crea una visualizzazione dei metadati:</span><span class="sxs-lookup"><span data-stu-id="ca4b8-118">The following code creates a metadata view:</span></span>


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



<span data-ttu-id="ca4b8-119">Il codice precedente organizza il contenuto come segue:</span><span class="sxs-lookup"><span data-stu-id="ca4b8-119">The preceding code organizes content as follows:</span></span>

<dl> <span data-ttu-id="ca4b8-120">Visualizzazione personale</span><span class="sxs-lookup"><span data-stu-id="ca4b8-120">My View</span></span><dl> <span data-ttu-id="ca4b8-121">Genre1</span><span class="sxs-lookup"><span data-stu-id="ca4b8-121">Genre1</span></span><dl> <span data-ttu-id="ca4b8-122">Artist1</span><span class="sxs-lookup"><span data-stu-id="ca4b8-122">Artist1</span></span><dl> <span data-ttu-id="ca4b8-123">Album1</span><span class="sxs-lookup"><span data-stu-id="ca4b8-123">Album1</span></span><dl> <span data-ttu-id="ca4b8-124">Song1</span><span class="sxs-lookup"><span data-stu-id="ca4b8-124">Song1</span></span>  
<span data-ttu-id="ca4b8-125">Song2</span><span class="sxs-lookup"><span data-stu-id="ca4b8-125">Song2</span></span>  
<span data-ttu-id="ca4b8-126">...</span><span class="sxs-lookup"><span data-stu-id="ca4b8-126">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="ca4b8-127">Album1</span><span class="sxs-lookup"><span data-stu-id="ca4b8-127">Album1</span></span><dl> <span data-ttu-id="ca4b8-128">Song1</span><span class="sxs-lookup"><span data-stu-id="ca4b8-128">Song1</span></span>  
<span data-ttu-id="ca4b8-129">Song2</span><span class="sxs-lookup"><span data-stu-id="ca4b8-129">Song2</span></span>  
<span data-ttu-id="ca4b8-130">...</span><span class="sxs-lookup"><span data-stu-id="ca4b8-130">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> <span data-ttu-id="ca4b8-131">Artist1</span><span class="sxs-lookup"><span data-stu-id="ca4b8-131">Artist1</span></span><dl> <span data-ttu-id="ca4b8-132">Album1</span><span class="sxs-lookup"><span data-stu-id="ca4b8-132">Album1</span></span><dl> <span data-ttu-id="ca4b8-133">Song1</span><span class="sxs-lookup"><span data-stu-id="ca4b8-133">Song1</span></span>  
<span data-ttu-id="ca4b8-134">Song2</span><span class="sxs-lookup"><span data-stu-id="ca4b8-134">Song2</span></span>  
<span data-ttu-id="ca4b8-135">...</span><span class="sxs-lookup"><span data-stu-id="ca4b8-135">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="ca4b8-136">Album1</span><span class="sxs-lookup"><span data-stu-id="ca4b8-136">Album1</span></span><dl> <span data-ttu-id="ca4b8-137">Song1</span><span class="sxs-lookup"><span data-stu-id="ca4b8-137">Song1</span></span>  
<span data-ttu-id="ca4b8-138">Song2</span><span class="sxs-lookup"><span data-stu-id="ca4b8-138">Song2</span></span>  
<span data-ttu-id="ca4b8-139">...</span><span class="sxs-lookup"><span data-stu-id="ca4b8-139">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca4b8-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca4b8-140">Requirements</span></span>



| <span data-ttu-id="ca4b8-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca4b8-141">Requirement</span></span> | <span data-ttu-id="ca4b8-142">Valore</span><span class="sxs-lookup"><span data-stu-id="ca4b8-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ca4b8-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca4b8-143">Header</span></span><br/> | <dl> <span data-ttu-id="ca4b8-144"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca4b8-144"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca4b8-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca4b8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca4b8-146">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="ca4b8-146">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 






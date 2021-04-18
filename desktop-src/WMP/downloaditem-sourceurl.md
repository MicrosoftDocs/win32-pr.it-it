---
title: DownloadItem. sourceURL
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà sourceURL recupera l'URL di origine del download.
ms.assetid: 87af20a5-5721-498d-8417-3e7dbbec38a2
keywords:
- Media Player Windows DownloadItem. sourceURL
topic_type:
- apiref
api_name:
- DownloadItem.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1670fb4fec0ff4adb68269cf6fe6bb39be248e01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327304"
---
# <a name="downloaditemsourceurl"></a><span data-ttu-id="cab85-106">DownloadItem. sourceURL</span><span class="sxs-lookup"><span data-stu-id="cab85-106">DownloadItem.sourceURL</span></span>

> [!Note]  
> <span data-ttu-id="cab85-107">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="cab85-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="cab85-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="cab85-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="cab85-109">La proprietà **sourceURL** recupera l'URL di origine del download.</span><span class="sxs-lookup"><span data-stu-id="cab85-109">The **sourceURL** property retrieves the source URL of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="cab85-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cab85-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).sourceURL
      
```

## <a name="possible-values"></a><span data-ttu-id="cab85-111">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="cab85-111">Possible Values</span></span>

<span data-ttu-id="cab85-112">Questa proprietà è una **stringa** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cab85-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cab85-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cab85-113">Remarks</span></span>

<span data-ttu-id="cab85-114">È possibile scaricare solo i formati multimediali digitali seguenti:</span><span class="sxs-lookup"><span data-stu-id="cab85-114">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="cab85-115">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="cab85-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="cab85-116">MP3</span><span class="sxs-lookup"><span data-stu-id="cab85-116">MP3</span></span>
-   <span data-ttu-id="cab85-117">Windows Media Audio (WMA)</span><span class="sxs-lookup"><span data-stu-id="cab85-117">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="cab85-118">Windows Media Video (WMV)</span><span class="sxs-lookup"><span data-stu-id="cab85-118">Windows Media Video (WMV)</span></span>

## <a name="requirements"></a><span data-ttu-id="cab85-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cab85-119">Requirements</span></span>



| <span data-ttu-id="cab85-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cab85-120">Requirement</span></span> | <span data-ttu-id="cab85-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cab85-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cab85-122">Versione</span><span class="sxs-lookup"><span data-stu-id="cab85-122">Version</span></span><br/> | <span data-ttu-id="cab85-123">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="cab85-123">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="cab85-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cab85-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="cab85-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cab85-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cab85-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cab85-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cab85-127">**Oggetto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="cab85-127">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 






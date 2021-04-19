---
title: DownloadItem. Progress
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà Progress recupera lo stato di avanzamento del download in byte.
ms.assetid: 58644eac-8dd0-4e9d-8055-03833c863a6e
keywords:
- Media Player di Windows DownloadItem. Progress
topic_type:
- apiref
api_name:
- DownloadItem.progress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1967c1eb3dc72c00b8b10b70da5d797343e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326337"
---
# <a name="downloaditemprogress"></a><span data-ttu-id="5241f-106">DownloadItem. Progress</span><span class="sxs-lookup"><span data-stu-id="5241f-106">DownloadItem.progress</span></span>

> [!Note]  
> <span data-ttu-id="5241f-107">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="5241f-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5241f-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5241f-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5241f-109">La proprietà **Progress** recupera lo stato di avanzamento del download in byte.</span><span class="sxs-lookup"><span data-stu-id="5241f-109">The **progress** property retrieves the progress of the download in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5241f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5241f-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).progress
      
```

## <a name="possible-values"></a><span data-ttu-id="5241f-111">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="5241f-111">Possible Values</span></span>

<span data-ttu-id="5241f-112">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="5241f-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="5241f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5241f-113">Requirements</span></span>



| <span data-ttu-id="5241f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5241f-114">Requirement</span></span> | <span data-ttu-id="5241f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5241f-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5241f-116">Versione</span><span class="sxs-lookup"><span data-stu-id="5241f-116">Version</span></span><br/> | <span data-ttu-id="5241f-117">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5241f-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="5241f-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5241f-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="5241f-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5241f-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5241f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5241f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5241f-121">**Oggetto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="5241f-121">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="5241f-122">**DownloadItem. size**</span><span class="sxs-lookup"><span data-stu-id="5241f-122">**DownloadItem.size**</span></span>](downloaditem-size.md)
</dt> </dl>

 

 






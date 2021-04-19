---
title: DownloadItem. size
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà Size recupera le dimensioni del download.
ms.assetid: e0fd9cb5-155a-4159-94b8-1bf05b4d1062
keywords:
- DownloadItem. Size Media Player Windows
topic_type:
- apiref
api_name:
- DownloadItem.size
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0ebb1ce15d34ad04095f1ef1ed84ad2df008c7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328721"
---
# <a name="downloaditemsize"></a><span data-ttu-id="110d1-106">DownloadItem. size</span><span class="sxs-lookup"><span data-stu-id="110d1-106">DownloadItem.size</span></span>

> [!Note]  
> <span data-ttu-id="110d1-107">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="110d1-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="110d1-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="110d1-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="110d1-109">La proprietà **size** recupera le dimensioni del download.</span><span class="sxs-lookup"><span data-stu-id="110d1-109">The **size** property retrieves the size of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="110d1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="110d1-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).size
      
```

## <a name="possible-values"></a><span data-ttu-id="110d1-111">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="110d1-111">Possible Values</span></span>

<span data-ttu-id="110d1-112">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="110d1-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="requirements"></a><span data-ttu-id="110d1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="110d1-113">Requirements</span></span>



| <span data-ttu-id="110d1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="110d1-114">Requirement</span></span> | <span data-ttu-id="110d1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="110d1-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="110d1-116">Versione</span><span class="sxs-lookup"><span data-stu-id="110d1-116">Version</span></span><br/> | <span data-ttu-id="110d1-117">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="110d1-117">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="110d1-118">DLL</span><span class="sxs-lookup"><span data-stu-id="110d1-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="110d1-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="110d1-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="110d1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="110d1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="110d1-121">**Oggetto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="110d1-121">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> <dt>

[<span data-ttu-id="110d1-122">**DownloadItem. Progress**</span><span class="sxs-lookup"><span data-stu-id="110d1-122">**DownloadItem.progress**</span></span>](downloaditem-progress.md)
</dt> </dl>

 

 






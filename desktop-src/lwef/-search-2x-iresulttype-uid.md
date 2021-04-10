---
title: Proprietà UID IResultType (WdsSharedIDL. h)
description: Questa proprietà contiene l'identificatore univoco per il tipo.
ms.assetid: 31c2ef7d-f5a7-441e-80ea-fd7e46fded07
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà UID
- Funzionalità dell'ambiente Windows legacy della proprietà UID, interfaccia IResultType
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultType, proprietà UID
topic_type:
- apiref
api_name:
- IResultType.UID
- IResultType.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbdd5a9b17da9cde04ac0b371a885b07415d0e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121519"
---
# <a name="iresulttypeuid-property"></a><span data-ttu-id="f71c7-106">Proprietà IResultType:: UID</span><span class="sxs-lookup"><span data-stu-id="f71c7-106">IResultType::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="f71c7-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f71c7-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="f71c7-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="f71c7-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="f71c7-109">Questa proprietà contiene l'identificatore univoco per il tipo.</span><span class="sxs-lookup"><span data-stu-id="f71c7-109">This property contains the unique identifier for the type.</span></span>

<span data-ttu-id="f71c7-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f71c7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f71c7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f71c7-111">Syntax</span></span>


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="f71c7-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f71c7-112">Property value</span></span>

<span data-ttu-id="f71c7-113">Indirizzo della posizione contenente l'UID.</span><span class="sxs-lookup"><span data-stu-id="f71c7-113">the address of the location containing the uid.</span></span>

## <a name="requirements"></a><span data-ttu-id="f71c7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f71c7-114">Requirements</span></span>



| <span data-ttu-id="f71c7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f71c7-115">Requirement</span></span> | <span data-ttu-id="f71c7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f71c7-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71c7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f71c7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f71c7-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f71c7-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f71c7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f71c7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f71c7-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="f71c7-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f71c7-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f71c7-121">Redistributable</span></span><br/>          | <span data-ttu-id="f71c7-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="f71c7-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="f71c7-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f71c7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f71c7-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f71c7-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 






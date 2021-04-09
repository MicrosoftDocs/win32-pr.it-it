---
title: Proprietà DisplayName IResultProperty (WdsSharedIDL. h)
description: Nome visualizzato localizzato della proprietà.
ms.assetid: 8f9e118a-9e92-4919-afe1-735c61af38f7
keywords:
- Proprietà DisplayName caratteristiche dell'ambiente Windows legacy
- Proprietà DisplayName caratteristiche dell'ambiente Windows legacy, interfaccia IResultProperty
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultProperty, proprietà DisplayName
topic_type:
- apiref
api_name:
- IResultProperty.DisplayName
- IResultProperty.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f36aa934d2ddf31d841478cef1cb9a33b0531224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120354"
---
# <a name="iresultpropertydisplayname-property"></a><span data-ttu-id="cf928-106">IResultProperty::D proprietà di riproduzione</span><span class="sxs-lookup"><span data-stu-id="cf928-106">IResultProperty::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="cf928-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cf928-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="cf928-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="cf928-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="cf928-109">Nome visualizzato localizzato della proprietà.</span><span class="sxs-lookup"><span data-stu-id="cf928-109">Localized display name of the property.</span></span>

<span data-ttu-id="cf928-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cf928-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf928-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf928-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="cf928-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="cf928-112">Property value</span></span>

<span data-ttu-id="cf928-113">Restituisce un puntatore al nome visualizzato localizzato.</span><span class="sxs-lookup"><span data-stu-id="cf928-113">returns a pointer to the localized display name.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf928-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf928-114">Requirements</span></span>



| <span data-ttu-id="cf928-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf928-115">Requirement</span></span> | <span data-ttu-id="cf928-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cf928-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf928-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf928-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cf928-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf928-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cf928-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf928-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cf928-120">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="cf928-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cf928-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="cf928-121">Redistributable</span></span><br/>          | <span data-ttu-id="cf928-122">Windows Desktop Search (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="cf928-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="cf928-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf928-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf928-124"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf928-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 






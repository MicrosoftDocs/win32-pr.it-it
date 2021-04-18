---
title: Mediacollection. getByAttributeAndMediaType, metodo
description: Il metodo getByAttributeAndMediaType recupera un oggetto playlist contenente gli oggetti multimediali con l'attributo e il tipo di supporto specificati.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- Metodo getByAttributeAndMediaType Windows Media Player
- Metodo getByAttributeAndMediaType Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e26abbf2f19d50ec6a10ebbafe12afae8576f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330347"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a><span data-ttu-id="a54d4-106">Mediacollection. getByAttributeAndMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="a54d4-106">MediaCollection.getByAttributeAndMediaType method</span></span>

<span data-ttu-id="a54d4-107">Il metodo **getByAttributeAndMediaType** recupera un oggetto **playlist** contenente gli oggetti **multimediali** con l'attributo e il tipo di supporto specificati.</span><span class="sxs-lookup"><span data-stu-id="a54d4-107">The **getByAttributeAndMediaType** method retrieves a **Playlist** object containing **Media** objects having the specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a54d4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a54d4-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="a54d4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a54d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a54d4-110">*attributo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a54d4-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a54d4-111">**Stringa** contenente l'attributo.</span><span class="sxs-lookup"><span data-stu-id="a54d4-111">**String** containing the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="a54d4-112">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a54d4-112">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a54d4-113">**Stringa** che contiene il valore.</span><span class="sxs-lookup"><span data-stu-id="a54d4-113">**String** containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="a54d4-114">*mediaType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a54d4-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a54d4-115">**Stringa** che contiene il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="a54d4-115">**String** containing the media type.</span></span> <span data-ttu-id="a54d4-116">Deve contenere uno dei valori seguenti: "audio", "video", "Photo", "playlist" o "other".</span><span class="sxs-lookup"><span data-stu-id="a54d4-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a54d4-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a54d4-117">Return value</span></span>

<span data-ttu-id="a54d4-118">Questo metodo restituisce un oggetto **playlist**</span><span class="sxs-lookup"><span data-stu-id="a54d4-118">This method returns a **Playlist** object</span></span>

## <a name="requirements"></a><span data-ttu-id="a54d4-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a54d4-119">Requirements</span></span>



| <span data-ttu-id="a54d4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a54d4-120">Requirement</span></span> | <span data-ttu-id="a54d4-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a54d4-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a54d4-122">Versione</span><span class="sxs-lookup"><span data-stu-id="a54d4-122">Version</span></span><br/> | <span data-ttu-id="a54d4-123">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="a54d4-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="a54d4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a54d4-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="a54d4-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a54d4-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a54d4-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a54d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a54d4-127">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="a54d4-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="a54d4-128">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="a54d4-128">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="a54d4-129">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="a54d4-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 






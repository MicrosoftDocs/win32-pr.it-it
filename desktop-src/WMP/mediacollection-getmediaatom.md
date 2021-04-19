---
title: Mediacollection. getMediaAtom, metodo
description: Il metodo getMediaAtom recupera l'indice in corrispondenza del quale si trova un attributo specificato all'interno del set di attributi disponibili.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- Metodo getMediaAtom Windows Media Player
- Metodo getMediaAtom Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getMediaAtom
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16728b20c26b90c10f144f278f7dec24195b536a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327623"
---
# <a name="mediacollectiongetmediaatom-method"></a><span data-ttu-id="2f708-106">Mediacollection. getMediaAtom, metodo</span><span class="sxs-lookup"><span data-stu-id="2f708-106">MediaCollection.getMediaAtom method</span></span>

<span data-ttu-id="2f708-107">Il metodo **getMediaAtom** recupera l'indice in corrispondenza del quale si trova un attributo specificato all'interno del set di attributi disponibili.</span><span class="sxs-lookup"><span data-stu-id="2f708-107">The **getMediaAtom** method retrieves the index at which a specified attribute resides within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f708-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f708-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="2f708-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f708-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f708-110">*attributo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f708-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f708-111">**Stringa** contenente il nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="2f708-111">**String** containing the attribute name.</span></span> <span data-ttu-id="2f708-112">Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2f708-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f708-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f708-113">Return value</span></span>

<span data-ttu-id="2f708-114">Questo metodo restituisce un **numero** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="2f708-114">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="2f708-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f708-115">Remarks</span></span>

<span data-ttu-id="2f708-116">Il numero di indice recuperato con questo metodo può essere passato al *supporto*. metodo **getItemInfoByAtom** per accedere ai valori di attributo.</span><span class="sxs-lookup"><span data-stu-id="2f708-116">The index number retrieved with this method can be passed to the *Media*.**getItemInfoByAtom** method to access attribute values.</span></span> <span data-ttu-id="2f708-117">Questa tecnica è in genere più efficiente quando si lavora con playlist di grandi dimensioni anziché accedere a un valore di attributo in base al nome tramite *supporti*. **GetItemInfo** o *supporti*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="2f708-117">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span>

<span data-ttu-id="2f708-118">Per usare questo metodo, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="2f708-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="2f708-119">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2f708-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f708-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f708-120">Requirements</span></span>



| <span data-ttu-id="2f708-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f708-121">Requirement</span></span> | <span data-ttu-id="2f708-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2f708-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f708-123">Versione</span><span class="sxs-lookup"><span data-stu-id="2f708-123">Version</span></span><br/> | <span data-ttu-id="2f708-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="2f708-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2f708-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2f708-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="2f708-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f708-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f708-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f708-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f708-128">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="2f708-128">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="2f708-129">**Media. getItemInfoByAtom**</span><span class="sxs-lookup"><span data-stu-id="2f708-129">**Media.getItemInfoByAtom**</span></span>](media-getiteminfobyatom.md)
</dt> <dt>

[<span data-ttu-id="2f708-130">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="2f708-130">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="2f708-131">**Mediacollection (oggetto)**</span><span class="sxs-lookup"><span data-stu-id="2f708-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="2f708-132">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2f708-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2f708-133">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2f708-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






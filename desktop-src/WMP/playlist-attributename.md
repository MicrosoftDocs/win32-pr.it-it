---
title: Playlist. AttributeName
description: La proprietà AttributeName Recupera il nome di un attributo in corrispondenza di un indice specificato.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Playlist. AttributeName Media Player Windows
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4560a7ca2766ee0bbadc582af878bca87e0834e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328113"
---
# <a name="playlistattributename"></a><span data-ttu-id="2ca98-104">Playlist. AttributeName</span><span class="sxs-lookup"><span data-stu-id="2ca98-104">Playlist.attributeName</span></span>

<span data-ttu-id="2ca98-105">La proprietà **attributeName** Recupera il nome di un attributo in corrispondenza di un indice specificato.</span><span class="sxs-lookup"><span data-stu-id="2ca98-105">The **attributeName** property retrieves the name of an attribute at a specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ca98-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ca98-106">Syntax</span></span>

<span data-ttu-id="2ca98-107">*Player*. *currentPlaylist*. **attributeName**( *Indice* )</span><span class="sxs-lookup"><span data-stu-id="2ca98-107">*player*.*currentPlaylist*.**attributeName**( *index* )</span></span>

## <a name="parameters"></a><span data-ttu-id="2ca98-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ca98-108">Parameters</span></span>

<span data-ttu-id="2ca98-109">*index*</span><span class="sxs-lookup"><span data-stu-id="2ca98-109">*index*</span></span>

<span data-ttu-id="2ca98-110">**Numero** (**Long**) che contiene l'indice.</span><span class="sxs-lookup"><span data-stu-id="2ca98-110">**Number** (**long**) containing the index.</span></span>

## <a name="possible-values"></a><span data-ttu-id="2ca98-111">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="2ca98-111">Possible Values</span></span>

<span data-ttu-id="2ca98-112">Questa proprietà è una **stringa** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2ca98-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ca98-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ca98-113">Remarks</span></span>

<span data-ttu-id="2ca98-114">Il numero di attributi viene recuperato dalla proprietà **attributeCount** .</span><span class="sxs-lookup"><span data-stu-id="2ca98-114">The number of attributes is retrieved by the **attributeCount** property.</span></span> <span data-ttu-id="2ca98-115">Dato un indice, **attributeName** restituisce una **stringa** che può essere usata insieme a **setItemInfo** o **GetItemInfo** per specificare o recuperare un valore per l'attributo.</span><span class="sxs-lookup"><span data-stu-id="2ca98-115">Given an index, **attributeName** returns a **String** that can be used in conjunction with **setItemInfo** or **getItemInfo** to specify or retrieve a value for the attribute.</span></span>

<span data-ttu-id="2ca98-116">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="2ca98-116">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="2ca98-117">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2ca98-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="2ca98-118">Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="2ca98-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="2ca98-119">Per il codice di esempio che usa questa proprietà, vedere la proprietà [attributeCount](playlist-attributecount.md) .</span><span class="sxs-lookup"><span data-stu-id="2ca98-119">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ca98-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ca98-120">Requirements</span></span>



| <span data-ttu-id="2ca98-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ca98-121">Requirement</span></span> | <span data-ttu-id="2ca98-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2ca98-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca98-123">Versione</span><span class="sxs-lookup"><span data-stu-id="2ca98-123">Version</span></span><br/> | <span data-ttu-id="2ca98-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="2ca98-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2ca98-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2ca98-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="2ca98-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ca98-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ca98-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ca98-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca98-128">**Oggetto playlist**</span><span class="sxs-lookup"><span data-stu-id="2ca98-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="2ca98-129">**Playlist. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="2ca98-129">**Playlist.attributeCount**</span></span>](playlist-attributecount.md)
</dt> <dt>

[<span data-ttu-id="2ca98-130">**Playlist. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="2ca98-130">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="2ca98-131">**Playlist. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="2ca98-131">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="2ca98-132">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2ca98-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2ca98-133">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2ca98-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






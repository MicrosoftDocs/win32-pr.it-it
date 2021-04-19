---
title: Attributo Description (WMP SDK)
description: L'attributo Description è una descrizione del contenuto.
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Attributo Description Media Player Windows
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326024"
---
# <a name="description-attribute"></a><span data-ttu-id="4981a-104">Description (attributo)</span><span class="sxs-lookup"><span data-stu-id="4981a-104">Description Attribute</span></span>

<span data-ttu-id="4981a-105">L'attributo **Description** è una descrizione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="4981a-105">The **Description** attribute is a description of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4981a-106">Si applica a</span><span class="sxs-lookup"><span data-stu-id="4981a-106">Applies To</span></span>

-   [<span data-ttu-id="4981a-107">File musicali</span><span class="sxs-lookup"><span data-stu-id="4981a-107">Music Files</span></span>](music-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="4981a-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="4981a-108">Remarks</span></span>

<span data-ttu-id="4981a-109">Questo attributo viene archiviato in file musicali, non nella libreria.</span><span class="sxs-lookup"><span data-stu-id="4981a-109">This attribute is stored in music files, not in the library.</span></span>

<span data-ttu-id="4981a-110">Questo attributo può avere più valori.</span><span class="sxs-lookup"><span data-stu-id="4981a-110">This attribute may have multiple values.</span></span> <span data-ttu-id="4981a-111">Per recuperare tutti i valori per un attributo multivalore, è necessario usare il *supporto*. metodo **getItemInfoByType** , non il metodo *media*. GetItemInfo.</span><span class="sxs-lookup"><span data-stu-id="4981a-111">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.getItemInfo method.</span></span>

<span data-ttu-id="4981a-112">La costante Windows Media Format SDK per questo attributo è g \_ wszWMDescription.</span><span class="sxs-lookup"><span data-stu-id="4981a-112">The Windows Media Format SDK constant for this attribute is g\_wszWMDescription.</span></span>

<span data-ttu-id="4981a-113">Per determinare se è possibile modificare il valore di questo attributo, usare il metodo [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="4981a-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4981a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4981a-114">Requirements</span></span>



| <span data-ttu-id="4981a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4981a-115">Requirement</span></span> | <span data-ttu-id="4981a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4981a-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="4981a-117">Versione</span><span class="sxs-lookup"><span data-stu-id="4981a-117">Version</span></span><br/> | <span data-ttu-id="4981a-118">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="4981a-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4981a-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4981a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4981a-120">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="4981a-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 






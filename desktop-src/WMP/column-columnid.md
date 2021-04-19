---
title: COLUMN. columnID
description: L'attributo columnID specifica o recupera un ID di colonna nel controllo PLAYLIST.
ms.assetid: c7b51f0b-e347-46be-a26d-aaa0bce83e0c
keywords:
- Media Player di Windows COLUMN. columnID
topic_type:
- apiref
api_name:
- COLUMN.columnID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4bc9aa6485443ae17486616b030b903a911a8e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330252"
---
# <a name="columncolumnid"></a><span data-ttu-id="b15fe-104">COLUMN. columnID</span><span class="sxs-lookup"><span data-stu-id="b15fe-104">COLUMN.columnID</span></span>

<span data-ttu-id="b15fe-105">L'attributo **ColumnID** specifica o recupera un ID di colonna nel controllo **playlist** .</span><span class="sxs-lookup"><span data-stu-id="b15fe-105">The **columnID** attribute specifies or retrieves a column ID in the **PLAYLIST** control.</span></span>

``` syntax
        elementID.columnID
```

## <a name="possible-values"></a><span data-ttu-id="b15fe-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="b15fe-106">Possible Values</span></span>

<span data-ttu-id="b15fe-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b15fe-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b15fe-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="b15fe-108">Remarks</span></span>

<span data-ttu-id="b15fe-109">I valori **ColumnID** sono gli stessi valori usati con il metodo **GetItemInfo** su un oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="b15fe-109">The **columnID** values are the same values used with the **getItemInfo** method on a **Media** object.</span></span> <span data-ttu-id="b15fe-110">È possibile ottenere un elenco usando i *supporti*. proprietà **attributeCount** per determinare il numero di attributi disponibili per un determinato oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="b15fe-110">A list can be obtained by using the *Media*.**attributeCount** property to determine the number of attributes available for a given **Media** object.</span></span> <span data-ttu-id="b15fe-111">I numeri di indice possono quindi essere usati con il *supporto*. metodo **GetAttribute** per determinare i nomi degli attributi, che a loro volta possono essere passati al *supporto*. **GetItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="b15fe-111">Index numbers can then be used with the *Media*.**getAttributeName** method to determine the names of the attributes, which can in turn be passed to *Media*.**getItemInfo**.</span></span> <span data-ttu-id="b15fe-112">La proprietà **ColumnID** può essere impostata solo su questi valori, ad eccezione di alcuni valori che potrebbero non essere restituiti dal *supporto*. **GetAttributeName**.</span><span class="sxs-lookup"><span data-stu-id="b15fe-112">The **columnID** property can only be set to these values, with the exception of some values that may not be returned by *Media*.**getAttributeName**.</span></span> <span data-ttu-id="b15fe-113">Tali valori sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="b15fe-113">These values are listed below.</span></span>



| <span data-ttu-id="b15fe-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b15fe-114">Value</span></span>     | <span data-ttu-id="b15fe-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b15fe-115">Description</span></span>                                                                        |
|-----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b15fe-116">name</span><span class="sxs-lookup"><span data-stu-id="b15fe-116">name</span></span>      | <span data-ttu-id="b15fe-117">Consente di visualizzare il nome dell'oggetto **supporto** .</span><span class="sxs-lookup"><span data-stu-id="b15fe-117">Displays the name of the **Media** object.</span></span>                                         |
| <span data-ttu-id="b15fe-118">duration</span><span class="sxs-lookup"><span data-stu-id="b15fe-118">duration</span></span>  | <span data-ttu-id="b15fe-119">Consente di visualizzare la durata dell'oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="b15fe-119">Displays the duration of the **Media** object.</span></span>                                     |
| <span data-ttu-id="b15fe-120">sourceURL</span><span class="sxs-lookup"><span data-stu-id="b15fe-120">sourceURL</span></span> | <span data-ttu-id="b15fe-121">Consente di visualizzare l'URL dell'oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="b15fe-121">Displays the URL of the **Media** object.</span></span>                                          |
| <span data-ttu-id="b15fe-122">status</span><span class="sxs-lookup"><span data-stu-id="b15fe-122">status</span></span>    | <span data-ttu-id="b15fe-123">Visualizza lo stato della copia dei file.</span><span class="sxs-lookup"><span data-stu-id="b15fe-123">Displays the status of copying files.</span></span>                                              |
| <span data-ttu-id="b15fe-124">size</span><span class="sxs-lookup"><span data-stu-id="b15fe-124">size</span></span>      | <span data-ttu-id="b15fe-125">Consente di visualizzare le dimensioni del file rappresentato dall'oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="b15fe-125">Displays the size of the file that the **Media** object represents.</span></span>                |
| <span data-ttu-id="b15fe-126">estensione</span><span class="sxs-lookup"><span data-stu-id="b15fe-126">extension</span></span> | <span data-ttu-id="b15fe-127">Consente di visualizzare l'estensione del nome file del file rappresentato dall'oggetto **multimediale** .</span><span class="sxs-lookup"><span data-stu-id="b15fe-127">Displays the file name extension of the file that the **Media** object represents.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b15fe-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b15fe-128">Requirements</span></span>



| <span data-ttu-id="b15fe-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b15fe-129">Requirement</span></span> | <span data-ttu-id="b15fe-130">Valore</span><span class="sxs-lookup"><span data-stu-id="b15fe-130">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b15fe-131">Versione</span><span class="sxs-lookup"><span data-stu-id="b15fe-131">Version</span></span><br/> | <span data-ttu-id="b15fe-132">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b15fe-132">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b15fe-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b15fe-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b15fe-134">**COLUMN-elemento**</span><span class="sxs-lookup"><span data-stu-id="b15fe-134">**COLUMN Element**</span></span>](column-element.md)
</dt> <dt>

[<span data-ttu-id="b15fe-135">**Oggetto multimediale**</span><span class="sxs-lookup"><span data-stu-id="b15fe-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="b15fe-136">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="b15fe-136">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="b15fe-137">**Media. GetAttribute**</span><span class="sxs-lookup"><span data-stu-id="b15fe-137">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="b15fe-138">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b15fe-138">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> </dl>

 

 






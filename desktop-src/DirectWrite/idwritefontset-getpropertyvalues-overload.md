---
title: Metodi GetPropertyValues IDWriteFontSet (DWrite \_ 3. h)
description: Restituisce i valori delle proprietà per il set di caratteri.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- Scrittura diretta metodi GetPropertyValues
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3d135a63be987a4999d898c8e9c7d84251c8ece3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328149"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a><span data-ttu-id="203db-104">Metodi IDWriteFontSet:: GetPropertyValues</span><span class="sxs-lookup"><span data-stu-id="203db-104">IDWriteFontSet::GetPropertyValues methods</span></span>

<span data-ttu-id="203db-105">Restituisce i valori delle proprietà per il set di caratteri.</span><span class="sxs-lookup"><span data-stu-id="203db-105">Returns property values for the font set.</span></span>

### <a name="overload-list"></a><span data-ttu-id="203db-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="203db-106">Overload list</span></span>



| <span data-ttu-id="203db-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="203db-107">Method</span></span>                                                                                                                                   | <span data-ttu-id="203db-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="203db-108">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="203db-109">[**GetPropertyValues ( \_ \_ ID proprietà carattere DWrite \_ , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="203db-109">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span>                       | <span data-ttu-id="203db-110">Restituisce tutti i valori di proprietà univoci nel set, che possono essere utilizzati per scopi quali la visualizzazione di un elenco di famiglie o tag cloud.</span><span class="sxs-lookup"><span data-stu-id="203db-110">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="203db-111">Tutti i valori vengono restituiti indipendentemente dalla lingua, inclusi tutti i nomi localizzati.</span><span class="sxs-lookup"><span data-stu-id="203db-111">All values are returned regardless of language, including all localized names.</span></span> <br/>                                                                                       |
| <span data-ttu-id="203db-112">[**GetPropertyValues ( \_ ID della proprietà del tipo di carattere DWrite \_ \_ , const WCHAR \* , IDWriteStringList \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="203db-112">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, const WCHAR\*, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span></span>        | <span data-ttu-id="203db-113">Restituisce tutti i valori di proprietà univoci nel set, che possono essere utilizzati per scopi quali la visualizzazione di un elenco di famiglie o tag cloud.</span><span class="sxs-lookup"><span data-stu-id="203db-113">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="203db-114">I valori vengono restituiti in ordine di priorità in base all'elenco di lingue, in modo che se un tipo di carattere contiene più di un nome localizzato, verrà restituito quello preferito.</span><span class="sxs-lookup"><span data-stu-id="203db-114">Values are returned in priority order according to the language list, such that if a font contains more than one localized name, the preferred one will be returned.</span></span> <br/> |
| <span data-ttu-id="203db-115">[**GetPropertyValues (UINT32, \_ ID proprietà del tipo di carattere DWrite \_ \_ , bool \* , IDWriteLocalizedStrings \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="203db-115">[**GetPropertyValues(UINT32, DWRITE\_FONT\_PROPERTY\_ID, BOOL\*, IDWriteLocalizedStrings\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span> | <span data-ttu-id="203db-116">Restituisce i valori delle proprietà di un indice di elemento del tipo di carattere specifico.</span><span class="sxs-lookup"><span data-stu-id="203db-116">Returns the property values of a specific font item index.</span></span><br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="203db-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="203db-117">Requirements</span></span>



| <span data-ttu-id="203db-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="203db-118">Requirement</span></span> | <span data-ttu-id="203db-119">Valore</span><span class="sxs-lookup"><span data-stu-id="203db-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="203db-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="203db-120">Header</span></span><br/> | <dl> <span data-ttu-id="203db-121"><dt>DWrite \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="203db-121"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="203db-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="203db-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="203db-123">**IDWriteFontSet**</span><span class="sxs-lookup"><span data-stu-id="203db-123">**IDWriteFontSet**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

<span data-ttu-id="203db-124">�</span><span class="sxs-lookup"><span data-stu-id="203db-124">�</span></span>

<span data-ttu-id="203db-125">�</span><span class="sxs-lookup"><span data-stu-id="203db-125">�</span></span>

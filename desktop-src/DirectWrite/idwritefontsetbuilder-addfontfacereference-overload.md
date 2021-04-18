---
title: Metodi AddFontFaceReference di IDWriteFontSetBuilder (DWrite \_ 3. h)
description: Aggiunge un riferimento a un tipo di carattere al set da compilare.
ms.assetid: 2543720f-1b5a-ca1d-9e24-3fcd61a4de37
keywords:
- Scrittura diretta metodi AddFontFaceReference
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3c20ca2832bfce3696a98c22730580442f621469
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330166"
---
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a><span data-ttu-id="2782b-104">Metodi IDWriteFontSetBuilder:: AddFontFaceReference</span><span class="sxs-lookup"><span data-stu-id="2782b-104">IDWriteFontSetBuilder::AddFontFaceReference methods</span></span>

<span data-ttu-id="2782b-105">Aggiunge un riferimento a un tipo di carattere al set da compilare.</span><span class="sxs-lookup"><span data-stu-id="2782b-105">Adds a reference to a font to the set being built.</span></span>

### <a name="overload-list"></a><span data-ttu-id="2782b-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="2782b-106">Overload list</span></span>



| <span data-ttu-id="2782b-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="2782b-107">Method</span></span>                                                                                                                                           | <span data-ttu-id="2782b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2782b-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2782b-109">[**AddFontFaceReference (IDWriteFontFaceReference \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span><span class="sxs-lookup"><span data-stu-id="2782b-109">[**AddFontFaceReference(IDWriteFontFaceReference\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span></span>                                         | <span data-ttu-id="2782b-110">Aggiunge un riferimento a un tipo di carattere al set da compilare.</span><span class="sxs-lookup"><span data-stu-id="2782b-110">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="2782b-111">I metadati necessari verranno estratti automaticamente dal tipo di carattere quando si chiama CreateFontSet.</span><span class="sxs-lookup"><span data-stu-id="2782b-111">The necessary metadata will automatically be extracted from the font upon calling CreateFontSet.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="2782b-112">[**AddFontFaceReference (IDWriteFontFaceReference \* , proprietà Const DWrite \_ Font \_ \* , UInt32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span><span class="sxs-lookup"><span data-stu-id="2782b-112">[**AddFontFaceReference(IDWriteFontFaceReference\*, const DWRITE\_FONT\_PROPERTY\*, UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span></span> | <span data-ttu-id="2782b-113">Aggiunge un riferimento a un tipo di carattere al set da compilare.</span><span class="sxs-lookup"><span data-stu-id="2782b-113">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="2782b-114">Il chiamante fornisce informazioni sufficienti per eseguire la ricerca, evitando la necessità di aprire il tipo di carattere potenzialmente non locale.</span><span class="sxs-lookup"><span data-stu-id="2782b-114">The caller supplies enough information to search on, avoiding the need to open the potentially non-local font.</span></span> <span data-ttu-id="2782b-115">Eventuali proprietà non fornite dal chiamante saranno mancanti e tali proprietà non saranno disponibili come filtri in GetMatchingFonts.</span><span class="sxs-lookup"><span data-stu-id="2782b-115">Any properties not supplied by the caller will be missing, and those properties will not be available as filters in GetMatchingFonts.</span></span> <span data-ttu-id="2782b-116">GetPropertyValues per le proprietà mancanti restituirà un elenco di stringhe vuote.</span><span class="sxs-lookup"><span data-stu-id="2782b-116">GetPropertyValues for missing properties will return an empty string list.</span></span> <span data-ttu-id="2782b-117">Le proprietà passate devono essere in genere coerenti con il contenuto effettivo del tipo di carattere, ma non devono essere.</span><span class="sxs-lookup"><span data-stu-id="2782b-117">The properties passed should generally be consistent with the actual font contents, but they need not be.</span></span> <span data-ttu-id="2782b-118">È possibile, ad esempio, assegnare un alias a un tipo di carattere usando un nome diverso o un identificatore univoco oppure impostare tag personalizzati non presenti nel tipo di carattere effettivo.</span><span class="sxs-lookup"><span data-stu-id="2782b-118">You could, for example, alias a font using a different name or unique identifier, or you could set custom tags not present in the actual font.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2782b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2782b-119">Requirements</span></span>



| <span data-ttu-id="2782b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2782b-120">Requirement</span></span> | <span data-ttu-id="2782b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2782b-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2782b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2782b-122">Header</span></span><br/> | <dl> <span data-ttu-id="2782b-123"><dt>DWrite \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="2782b-123"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2782b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2782b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2782b-125">**IDWriteFontSetBuilder**</span><span class="sxs-lookup"><span data-stu-id="2782b-125">**IDWriteFontSetBuilder**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

<span data-ttu-id="2782b-126">�</span><span class="sxs-lookup"><span data-stu-id="2782b-126">�</span></span>

<span data-ttu-id="2782b-127">�</span><span class="sxs-lookup"><span data-stu-id="2782b-127">�</span></span>

---
description: Definisce una matrice di 4 byte che contiene i valori ASCII a 4 8 bit, A-Z o a-z per identificare gli script OpenType, il linguaggio e i tag della funzionalità del tipo di carattere.
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: OPENTYPE_TAG (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf973c03f26bdb8f8b3799e1780fed5075d315cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309499"
---
# <a name="opentype_tag"></a><span data-ttu-id="e9e17-103">\_tag OPENTYPE</span><span class="sxs-lookup"><span data-stu-id="e9e17-103">OPENTYPE\_TAG</span></span>

<span data-ttu-id="e9e17-104">Definisce una matrice di 4 byte che contiene i valori ASCII a 4 8 bit, A-Z o a-z per identificare gli script OpenType, il linguaggio e i tag della funzionalità del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="e9e17-104">Defines a 4-byte array that contains four 8-bit ASCII values of space, A-Z, or a-z to identify OpenType script, language, and font feature tags.</span></span>


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a><span data-ttu-id="e9e17-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9e17-105">Remarks</span></span>

<span data-ttu-id="e9e17-106">Negli esempi seguenti vengono definite le rappresentazioni dei tag della funzionalità OpenType.</span><span class="sxs-lookup"><span data-stu-id="e9e17-106">The following examples define representations of OpenType feature tags.</span></span>

-   <span data-ttu-id="e9e17-107">Il tag di funzionalità per la funzionalità di legatura è "Liga".</span><span class="sxs-lookup"><span data-stu-id="e9e17-107">The feature tag for the ligature feature is "liga".</span></span>
-   <span data-ttu-id="e9e17-108">I tag di lingua per Romeno, Urdu e persiano sono rispettivamente "ROM", "URD" e "lontano".</span><span class="sxs-lookup"><span data-stu-id="e9e17-108">The language tags for Romanian, Urdu, and Persian are "ROM ", "URD ", and "FAR ", respectively.</span></span> <span data-ttu-id="e9e17-109">Si noti che ognuno di questi tag termina con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="e9e17-109">Note that each of these tags ends with a space.</span></span>
-   <span data-ttu-id="e9e17-110">I tag di script per gli script latini e arabi sono rispettivamente "Latn" e "Arab".</span><span class="sxs-lookup"><span data-stu-id="e9e17-110">The script tags for Latin and Arabic scripts are "latn" and "arab", respectively.</span></span>

<span data-ttu-id="e9e17-111">Per ulteriori informazioni sui tag delle funzionalità OpenType e sulla specifica OpenType, vedere <https://www.microsoft.com/typography/otspec/featuretags.htm> .</span><span class="sxs-lookup"><span data-stu-id="e9e17-111">For more information on OpenType feature tags and the OpenType specification, see <https://www.microsoft.com/typography/otspec/featuretags.htm>.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9e17-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9e17-112">Requirements</span></span>



| <span data-ttu-id="e9e17-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9e17-113">Requirement</span></span> | <span data-ttu-id="e9e17-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e17-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e9e17-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9e17-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e9e17-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9e17-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e9e17-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9e17-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e9e17-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9e17-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e9e17-119">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e9e17-119">Redistributable</span></span><br/>          | <span data-ttu-id="e9e17-120">Usp10.dll versione 1,600 o successiva in Windows Espandi in un secondo momento</span><span class="sxs-lookup"><span data-stu-id="e9e17-120">Usp10.dll version 1.600 or greater onWindows XPand later</span></span><br/>                |
| <span data-ttu-id="e9e17-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9e17-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9e17-122"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9e17-122"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9e17-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9e17-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9e17-124">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="e9e17-124">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="e9e17-125">Strutture Uniscribe</span><span class="sxs-lookup"><span data-stu-id="e9e17-125">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="e9e17-126">**ScriptGetFontAlternateGlyphs**</span><span class="sxs-lookup"><span data-stu-id="e9e17-126">**ScriptGetFontAlternateGlyphs**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[<span data-ttu-id="e9e17-127">**ScriptGetFontFeatureTags**</span><span class="sxs-lookup"><span data-stu-id="e9e17-127">**ScriptGetFontFeatureTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[<span data-ttu-id="e9e17-128">**ScriptGetFontLanguageTags**</span><span class="sxs-lookup"><span data-stu-id="e9e17-128">**ScriptGetFontLanguageTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[<span data-ttu-id="e9e17-129">**ScriptGetFontScriptTags**</span><span class="sxs-lookup"><span data-stu-id="e9e17-129">**ScriptGetFontScriptTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[<span data-ttu-id="e9e17-130">**ScriptItemizeOpenType**</span><span class="sxs-lookup"><span data-stu-id="e9e17-130">**ScriptItemizeOpenType**</span></span>](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[<span data-ttu-id="e9e17-131">**ScriptPlaceOpenType**</span><span class="sxs-lookup"><span data-stu-id="e9e17-131">**ScriptPlaceOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[<span data-ttu-id="e9e17-132">**ScriptPositionSingleGlyph**</span><span class="sxs-lookup"><span data-stu-id="e9e17-132">**ScriptPositionSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[<span data-ttu-id="e9e17-133">**ScriptShapeOpenType**</span><span class="sxs-lookup"><span data-stu-id="e9e17-133">**ScriptShapeOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[<span data-ttu-id="e9e17-134">**ScriptSubstituteSingleGlyph**</span><span class="sxs-lookup"><span data-stu-id="e9e17-134">**ScriptSubstituteSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 





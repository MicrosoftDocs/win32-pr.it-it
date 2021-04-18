---
description: Definisce alcuni o tutti gli attributi carattere, i glifi, le larghezze di avanzamento, le posizioni x e y, i mapping da carattere a glifo e così via per una stringa.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317141"
---
# <a name="script_string_analysis"></a><span data-ttu-id="69b62-103">\_analisi della stringa di script \_</span><span class="sxs-lookup"><span data-stu-id="69b62-103">SCRIPT\_STRING\_ANALYSIS</span></span>

<span data-ttu-id="69b62-104">Definisce alcuni o tutti gli attributi carattere, i glifi, le larghezze di avanzamento, le posizioni x e y, i mapping da carattere a glifo e così via per una stringa.</span><span class="sxs-lookup"><span data-stu-id="69b62-104">Defines some or all of the character attributes, glyphs, advance widths, x and y positions, character-to-glyph mappings, and so forth, for a string.</span></span>


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a><span data-ttu-id="69b62-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="69b62-105">Remarks</span></span>

<span data-ttu-id="69b62-106">Si tratta di una struttura opaca allocata in modo dinamico e recuperata da [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse).</span><span class="sxs-lookup"><span data-stu-id="69b62-106">This is an opaque structure that is allocated dynamically and retrieved by [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse).</span></span> <span data-ttu-id="69b62-107">È obbligatorio anche per tutte le altre funzioni \**scriptString \** _.</span><span class="sxs-lookup"><span data-stu-id="69b62-107">It is required for all other \**ScriptString\** _ functions, as well.</span></span>

<span data-ttu-id="69b62-108">Poiché l'analisi può essere di grandi dimensioni, è importante che l'applicazione chiami [_ *ScriptStringFree* \*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) non appena termina con la stringa.</span><span class="sxs-lookup"><span data-stu-id="69b62-108">Since the analysis can be large, it is important for your application to call [_ *ScriptStringFree*\*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) as soon as it has finished with the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b62-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69b62-109">Requirements</span></span>



| <span data-ttu-id="69b62-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="69b62-110">Requirement</span></span> | <span data-ttu-id="69b62-111">Valore</span><span class="sxs-lookup"><span data-stu-id="69b62-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69b62-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69b62-112">Minimum supported client</span></span><br/> | <span data-ttu-id="69b62-113">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="69b62-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="69b62-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69b62-114">Minimum supported server</span></span><br/> | <span data-ttu-id="69b62-115">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="69b62-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="69b62-116">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="69b62-116">Redistributable</span></span><br/>          | <span data-ttu-id="69b62-117">Internet Explorer 5 o versioni successive onWindows me/98/95</span><span class="sxs-lookup"><span data-stu-id="69b62-117">Internet Explorer 5 or later onWindows Me/98/95</span></span><br/>                         |
| <span data-ttu-id="69b62-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69b62-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="69b62-119"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="69b62-119"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69b62-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69b62-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b62-121">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="69b62-121">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="69b62-122">Strutture Uniscribe</span><span class="sxs-lookup"><span data-stu-id="69b62-122">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="69b62-123">**ScriptStringAnalyse**</span><span class="sxs-lookup"><span data-stu-id="69b62-123">**ScriptStringAnalyse**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[<span data-ttu-id="69b62-124">**ScriptStringFree**</span><span class="sxs-lookup"><span data-stu-id="69b62-124">**ScriptStringFree**</span></span>](script-string-analysis.md)
</dt> </dl>

 

 





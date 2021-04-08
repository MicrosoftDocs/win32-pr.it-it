---
description: Le librerie di runtime C standard contengono entrambe le versioni Unicode UTF-16 (carattere wide) delle funzioni stringa che è possibile usare con le versioni Unicode e orientata ai byte delle funzioni stringa che possono essere usate con i caratteri dei set di caratteri a byte singolo (SBCSs). Il tipo di dati Unicode WCHAR è compatibile con il tipo di dati wchar \_ t in ANSI C e consente l'accesso alle funzioni stringa Unicode. Le versioni Unicode delle funzioni iniziano con le lettere &\# 0034; wcs&\# 0034; (o a volte &\# 0034; \_ WCS&\# 0034;). Il tipo di dati CHAR utilizzato per le tabelle codici è compatibile con il tipo di dati carattere char in ANSI C, per consentire l'accesso alle funzioni per le stringhe di caratteri. Le versioni dei caratteri delle funzioni iniziano con le lettere &\# 0034; str&\# 0034;. Sono inoltre disponibili versioni speciali per i set di caratteri a doppio byte (DBCS) che iniziano con le lettere &\# 0034; \_ MB&\# 0034;.
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: Funzioni C standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6247b3707f96908ef16d887462ba06573fd8dd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885549"
---
# <a name="standard-c-functions"></a><span data-ttu-id="eb86f-108">Funzioni C standard</span><span class="sxs-lookup"><span data-stu-id="eb86f-108">Standard C Functions</span></span>

<span data-ttu-id="eb86f-109">Le librerie di runtime C standard contengono entrambe le versioni Unicode UTF-16 (carattere wide) delle funzioni stringa che è possibile usare con le versioni [Unicode](unicode.md) e orientata ai byte delle funzioni stringa che possono essere usate con i caratteri dei [set di caratteri a byte singolo](single-byte-character-sets.md) (SBCSs).</span><span class="sxs-lookup"><span data-stu-id="eb86f-109">The standard C runtime libraries contain both Unicode UTF-16 (wide character) versions of string functions that can be used with [Unicode](unicode.md) and byte-oriented versions of string functions that can be used with characters from [single-byte character sets](single-byte-character-sets.md) (SBCSs).</span></span> <span data-ttu-id="eb86f-110">Il tipo di dati Unicode WCHAR è compatibile con il tipo di dati wchar \_ t in ANSI C e consente l'accesso alle funzioni stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="eb86f-110">The Unicode data type WCHAR is compatible with the data type wchar\_t in ANSI C, and allows access to the Unicode string functions.</span></span> <span data-ttu-id="eb86f-111">Le versioni Unicode delle funzioni iniziano con le lettere "WCS" (o a volte " \_ WCS").</span><span class="sxs-lookup"><span data-stu-id="eb86f-111">The Unicode versions of the functions start with the letters "wcs" (or sometimes "\_wcs").</span></span> <span data-ttu-id="eb86f-112">Il tipo di dati CHAR utilizzato per le tabelle codici è compatibile con il tipo di dati carattere char in ANSI C, per consentire l'accesso alle funzioni per le stringhe di caratteri.</span><span class="sxs-lookup"><span data-stu-id="eb86f-112">The data type CHAR used for code pages is compatible with the character data type char in ANSI C, to allow access to the character string functions.</span></span> <span data-ttu-id="eb86f-113">Le versioni dei caratteri delle funzioni iniziano con le lettere "Str".</span><span class="sxs-lookup"><span data-stu-id="eb86f-113">The character versions of the functions start with the letters "str".</span></span> <span data-ttu-id="eb86f-114">Sono inoltre disponibili versioni speciali per i [set di caratteri a doppio byte](double-byte-character-sets.md) (DBCS) che iniziano con le lettere " \_ MBS".</span><span class="sxs-lookup"><span data-stu-id="eb86f-114">There are also special versions for [double-byte character sets](double-byte-character-sets.md) (DBCSs) that start with the letters "\_mbs".</span></span>

<span data-ttu-id="eb86f-115">Le librerie di runtime C standard includono funzioni generiche per tutte le funzioni stringa C standard.</span><span class="sxs-lookup"><span data-stu-id="eb86f-115">The standard C runtime libraries include generic functions for all standard C string functions.</span></span> <span data-ttu-id="eb86f-116">Iniziano con " \_ TCS" e sono elencati nel file di intestazione Tchar. h.</span><span class="sxs-lookup"><span data-stu-id="eb86f-116">They start with "\_tcs" and are listed in the Tchar.h header file.</span></span> <span data-ttu-id="eb86f-117">Queste funzioni usano il tipo di dati TCHAR generico.</span><span class="sxs-lookup"><span data-stu-id="eb86f-117">These functions use the generic TCHAR data type.</span></span>

<span data-ttu-id="eb86f-118">Un'applicazione deve aggiungere le righe seguenti per usare le funzioni generiche e compilare per Unicode.</span><span class="sxs-lookup"><span data-stu-id="eb86f-118">An application must add the following lines to use the generic functions and compile for Unicode.</span></span>


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



<span data-ttu-id="eb86f-119">Si noti che sono necessari entrambi i file Tchar. h e WCHAR. h e che è necessario anche il carattere di sottolineatura principale della \_ variabile Unicode.</span><span class="sxs-lookup"><span data-stu-id="eb86f-119">Note that both the Tchar.h and Wchar.h files are required, and that the leading underscore on the \_UNICODE variable is also required.</span></span> <span data-ttu-id="eb86f-120">Questa nomenclatura è specifica della libreria C standard.</span><span class="sxs-lookup"><span data-stu-id="eb86f-120">This nomenclature is specific to the standard C library.</span></span> <span data-ttu-id="eb86f-121">Il rendering "UNICODE" senza il carattere di sottolineatura è relativo ai runtime di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="eb86f-121">"UNICODE" rendered without the underscore is for the Microsoft Windows runtimes.</span></span>

<span data-ttu-id="eb86f-122">Le funzioni [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) e [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) possono essere convertite dal set di caratteri supportato dalla libreria C standard in Unicode e viceversa, con alcune limitazioni.</span><span class="sxs-lookup"><span data-stu-id="eb86f-122">The [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) and [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) functions can convert from the character set supported by the standard C library to Unicode and back, with some limitations.</span></span> <span data-ttu-id="eb86f-123">Per ulteriori informazioni sulla conversione di stringhe da e verso Unicode, vedere [conversione tra tipi di stringa](translation-between-string-types.md).</span><span class="sxs-lookup"><span data-stu-id="eb86f-123">For more information about translating strings to and from Unicode, see [Translation Between String Types](translation-between-string-types.md).</span></span>

<span data-ttu-id="eb86f-124">La funzione [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) definita in TCHAR. h supporta le stesse specifiche di formato delle funzioni di stampa strsafe. h, ad esempio [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa).</span><span class="sxs-lookup"><span data-stu-id="eb86f-124">The [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) function defined in Tchar.h supports the same format specifications as the Strsafe.h print functions, for example [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa).</span></span> <span data-ttu-id="eb86f-125">Analogamente, TCHAR. h definisce una funzione [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) , in cui la stringa di formato è una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="eb86f-125">Similarly, Tchar.h defines a [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) function, in which the format string itself is a Unicode string.</span></span>

> [!Caution]  
> <span data-ttu-id="eb86f-126">Una gestione dei buffer insufficiente è coinvolta in molti problemi di sicurezza che coinvolgono sovraccarichi del buffer.</span><span class="sxs-lookup"><span data-stu-id="eb86f-126">Poor buffer handling is implicated in many security issues that involve buffer overruns.</span></span> <span data-ttu-id="eb86f-127">Vedere le informazioni di [riferimento su strsafe. h](../menurc/strsafe-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="eb86f-127">See [Strsafe.h Reference](../menurc/strsafe-ovw.md).</span></span> <span data-ttu-id="eb86f-128">Le funzioni definite in strsafe. h forniscono un'elaborazione aggiuntiva per la gestione appropriata del buffer nel codice.</span><span class="sxs-lookup"><span data-stu-id="eb86f-128">The functions defined in Strsafe.h provide additional processing for proper buffer handling in your code.</span></span> <span data-ttu-id="eb86f-129">Hanno lo scopo di sostituire le controparti C/C++ predefinite, nonché le implementazioni specifiche di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="eb86f-129">They are intended to replace their built-in C/C++ counterparts as well as specific Microsoft Windows implementations.</span></span> <span data-ttu-id="eb86f-130">Per ulteriori informazioni, vedere [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="eb86f-130">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="eb86f-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb86f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb86f-132">Unicode nell'API Windows</span><span class="sxs-lookup"><span data-stu-id="eb86f-132">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 

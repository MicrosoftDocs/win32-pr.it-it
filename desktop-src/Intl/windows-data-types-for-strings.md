---
description: La maggior parte delle operazioni di stringa può utilizzare la stessa logica per le tabelle codici Unicode e per Windows.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Tipi di dati di Windows per le stringhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e24be1024736ce324e040e58f6ac45636a11d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058358"
---
# <a name="windows-data-types-for-strings"></a><span data-ttu-id="0653e-103">Tipi di dati di Windows per le stringhe</span><span class="sxs-lookup"><span data-stu-id="0653e-103">Windows Data Types for Strings</span></span>

<span data-ttu-id="0653e-104">La maggior parte delle operazioni di stringa può utilizzare la stessa logica per le [tabelle codici](code-pages.md) [Unicode](unicode.md) e per Windows.</span><span class="sxs-lookup"><span data-stu-id="0653e-104">Most string operations can use the same logic for [Unicode](unicode.md) and for [Windows code pages](code-pages.md).</span></span> <span data-ttu-id="0653e-105">L'unica differenza è che l'unità di base dell'operazione è un carattere a 16 bit (noto anche come carattere wide) per Unicode e un carattere a 8 bit per le tabelle codici di Windows.</span><span class="sxs-lookup"><span data-stu-id="0653e-105">The only difference is that the basic unit of operation is a 16-bit character (also known as a wide character) for Unicode and an 8-bit character for Windows code pages.</span></span> <span data-ttu-id="0653e-106">I file di intestazione di Windows forniscono diverse definizioni di tipi che semplificano la creazione di origini che possono essere compilate per Unicode o per le tabelle codici di Windows.</span><span class="sxs-lookup"><span data-stu-id="0653e-106">The Windows header files provide several type definitions that make it easy to create sources that can be compiled for Unicode or for Windows code pages.</span></span>

<span data-ttu-id="0653e-107">Windows supporta tre set di tipi di dati di tipo carattere e stringa: un set di definizioni di tipo generico che possono essere compilate per le tabelle codici Unicode o Windows e due set di definizioni di tipi specifiche.</span><span class="sxs-lookup"><span data-stu-id="0653e-107">Windows supports three sets of character and string data types: a set of generic type definitions that can compile for either Unicode or Windows code pages, and two sets of specific type definitions.</span></span> <span data-ttu-id="0653e-108">Un set di definizioni di tipi specifiche è da usare con Unicode e l'altro per l'uso con le tabelle codici di Windows.</span><span class="sxs-lookup"><span data-stu-id="0653e-108">One set of specific type definitions is for use with Unicode, and the other is for use with Windows code pages.</span></span>

<span data-ttu-id="0653e-109">Un'applicazione che usa tipi di dati generici può essere compilata per Unicode semplicemente definendo "UNICODE" prima delle istruzioni **\# include** per i file di intestazione o durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="0653e-109">An application using generic data types can be compiled for Unicode simply by defining "UNICODE" before the **\#include** statements for the header files, or during compilation.</span></span> <span data-ttu-id="0653e-110">Le nuove applicazioni Windows devono utilizzare Unicode per evitare le incoerenze di diverse tabelle codici e semplificare la localizzazione.</span><span class="sxs-lookup"><span data-stu-id="0653e-110">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and to simplify localization.</span></span> <span data-ttu-id="0653e-111">Devono essere scritti con tipi di dati generici e devono definire "UNICODE" per compilare questi tipi in tipi Unicode.</span><span class="sxs-lookup"><span data-stu-id="0653e-111">They should be written with generic data types, and should define "UNICODE" in order to compile these types into Unicode types.</span></span> <span data-ttu-id="0653e-112">Nelle poche posizioni in cui un'applicazione deve funzionare con dati di tipo carattere a 8 bit, può utilizzare esplicitamente i tipi per le tabelle codici di Windows.</span><span class="sxs-lookup"><span data-stu-id="0653e-112">In the few places where an application must work with 8-bit character data, it can make explicit use of the types for Windows code pages.</span></span>

<span data-ttu-id="0653e-113">La possibilità di compilare i tipi generici nei tipi per le tabelle codici di Windows esiste principalmente per supportare le applicazioni legacy.</span><span class="sxs-lookup"><span data-stu-id="0653e-113">The ability to compile the generic types into types for Windows code pages exists mainly to support legacy applications.</span></span> <span data-ttu-id="0653e-114">Per eseguire la compilazione per le tabelle codici di Windows, l'applicazione omette semplicemente la definizione UNICODE.</span><span class="sxs-lookup"><span data-stu-id="0653e-114">To compile for Windows code pages, the application just omits the UNICODE definition.</span></span>

<span data-ttu-id="0653e-115">Nell'esempio seguente viene illustrato il metodo utilizzato nei file di intestazione di Windows per definire i tre set di tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="0653e-115">The following example shows the method used in the Windows header files to define the three sets of data types.</span></span> <span data-ttu-id="0653e-116">Per l'implementazione, vedere il file di intestazione Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="0653e-116">For the implementation, see the Winnt.h header file.</span></span>


```C++
// Generic types

#ifdef UNICODE
    typedef wchar_t TCHAR;
#else
    typedef unsigned char TCHAR;
#endif

typedef TCHAR *LPTSTR, *LPTCH;

// 8-bit character specific

typedef unsigned char CHAR;
typedef CHAR *LPSTR, *LPCH;

// Unicode specific (wide characters)

typedef unsigned wchar_t WCHAR;
typedef WCHAR *LPWSTR, *LPWCH;
```



<span data-ttu-id="0653e-117">La lettera "T" in una definizione di tipo, ad esempio TCHAR o LPTSTR, designa un tipo generico che può essere compilato per le tabelle codici di Windows o Unicode.</span><span class="sxs-lookup"><span data-stu-id="0653e-117">The letter "T" in a type definition, for example, TCHAR or LPTSTR, designates a generic type that can be compiled for either Windows code pages or Unicode.</span></span> <span data-ttu-id="0653e-118">La lettera "W" in una definizione di tipo, ad esempio WCHAR o LPWSTR, definisce un tipo Unicode.</span><span class="sxs-lookup"><span data-stu-id="0653e-118">The letter "W" in a type definition, for example, WCHAR or LPWSTR, designates a Unicode type.</span></span> <span data-ttu-id="0653e-119">Poiché le tabelle codici di Windows sono del formato precedente, hanno definizioni di tipo semplice, ad esempio CHAR e LPSTR.</span><span class="sxs-lookup"><span data-stu-id="0653e-119">Because Windows code pages are of the older form, they have simple type definitions, such as CHAR and LPSTR.</span></span> <span data-ttu-id="0653e-120">Per una descrizione completa dei tipi di dati in Windows, vedere [tipi di dati di Windows](../winprog/windows-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="0653e-120">For a complete description of data types in Windows, see [Windows Data Types](../winprog/windows-data-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0653e-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0653e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0653e-122">Unicode nell'API Windows</span><span class="sxs-lookup"><span data-stu-id="0653e-122">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 

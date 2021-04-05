---
description: Il Windows SDK fornisce i prototipi di funzione in Generic, tabella codici di Windows e versioni Unicode.
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: Convenzioni per prototipi di funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951860f72870dcbbcb88572f379e39dc843ecb11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882149"
---
# <a name="conventions-for-function-prototypes"></a><span data-ttu-id="8fd35-103">Convenzioni per prototipi di funzione</span><span class="sxs-lookup"><span data-stu-id="8fd35-103">Conventions for Function Prototypes</span></span>

<span data-ttu-id="8fd35-104">Il Windows SDK fornisce i prototipi di funzione in Generic, [tabella codici di Windows](code-pages.md)e versioni [Unicode](unicode.md) .</span><span class="sxs-lookup"><span data-stu-id="8fd35-104">The Windows SDK provides function prototypes in generic, [Windows code page](code-pages.md), and [Unicode](unicode.md) versions.</span></span> <span data-ttu-id="8fd35-105">I prototipi possono essere compilati per produrre prototipi di tabella codici di Windows o prototipi Unicode.</span><span class="sxs-lookup"><span data-stu-id="8fd35-105">The prototypes can be compiled to produce either Windows code page prototypes or Unicode prototypes.</span></span> <span data-ttu-id="8fd35-106">Tutti e tre i prototipi vengono descritti in questo argomento e sono illustrati dagli esempi di codice per la funzione [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="8fd35-106">All three prototypes are discussed in this topic and are illustrated by code samples for the [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) function.</span></span>

<span data-ttu-id="8fd35-107">Di seguito è riportato un esempio di prototipo generico:</span><span class="sxs-lookup"><span data-stu-id="8fd35-107">The following is an example of a generic prototype.</span></span>


```C++
BOOL SetWindowText(
  HWND hwnd,
  LPCTSTR lpText
);
```



<span data-ttu-id="8fd35-108">Il file di intestazione fornisce il nome della funzione generica implementato come macro.</span><span class="sxs-lookup"><span data-stu-id="8fd35-108">The header file provides the generic function name implemented as a macro.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText SetWindowTextW
#else
#define SetWindowText SetWindowTextA
#endif // !UNICODE
```



<span data-ttu-id="8fd35-109">Il preprocessore espande la macro nella tabella codici di Windows o nel nome della funzione Unicode.</span><span class="sxs-lookup"><span data-stu-id="8fd35-109">The preprocessor expands the macro into either the Windows code page or Unicode function name.</span></span> <span data-ttu-id="8fd35-110">La lettera "A" (ANSI) o "W" (Unicode) viene aggiunta alla fine del nome della funzione generica, a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="8fd35-110">The letter "A" (ANSI) or "W" (Unicode) is added at the end of the generic function name, as appropriate.</span></span> <span data-ttu-id="8fd35-111">Il file di intestazione fornisce quindi due prototipi specifici, uno per le tabelle codici di Windows e uno per Unicode, come illustrato negli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8fd35-111">The header file then provides two specific prototypes, one for Windows code pages and one for Unicode, as shown in the following examples.</span></span>


```C++
BOOL SetWindowTextA(
  HWND hwnd,
  LPCSTR lpText
);
```




```C++
BOOL SetWindowTextW(
  HWND hwnd,
  LPCWSTR lpText
);
```



<span data-ttu-id="8fd35-112">Come illustrato in [tipi di dati di Windows per le stringhe](windows-data-types-for-strings.md), il prototipo di funzione generica usa il tipo di dati LPCTSTR per il parametro di testo.</span><span class="sxs-lookup"><span data-stu-id="8fd35-112">As explained in [Windows Data Types for Strings](windows-data-types-for-strings.md), the generic function prototype uses the data type LPCTSTR for the text parameter.</span></span> <span data-ttu-id="8fd35-113">Tuttavia, il prototipo della tabella codici di Windows utilizza il tipo LPCSTR e il prototipo Unicode utilizza LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="8fd35-113">However, the Windows code page prototype uses the type LPCSTR, and the Unicode prototype uses LPCWSTR.</span></span>

<span data-ttu-id="8fd35-114">Per tutte le funzioni con argomenti di testo, le applicazioni devono in genere utilizzare i prototipi di funzione generici.</span><span class="sxs-lookup"><span data-stu-id="8fd35-114">For all functions with text arguments, applications should normally use the generic function prototypes.</span></span> <span data-ttu-id="8fd35-115">Se un'applicazione definisce "UNICODE" prima delle istruzioni **\# include** per i file di intestazione o durante la compilazione, le istruzioni verranno compilate in funzioni Unicode.</span><span class="sxs-lookup"><span data-stu-id="8fd35-115">If an application defines "UNICODE" either before the **\#include** statements for the header files or during compilation, the statements will be compiled into Unicode functions.</span></span>

> [!Note]  
> <span data-ttu-id="8fd35-116">Le nuove applicazioni Windows devono utilizzare Unicode per evitare le incoerenze di diverse tabelle codici e per semplificare la localizzazione.</span><span class="sxs-lookup"><span data-stu-id="8fd35-116">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="8fd35-117">Devono essere scritti con funzioni generiche ed è necessario definire UNICODE per compilare le funzioni in funzioni Unicode.</span><span class="sxs-lookup"><span data-stu-id="8fd35-117">They should be written with generic functions, and should define UNICODE to compile the functions into Unicode functions.</span></span> <span data-ttu-id="8fd35-118">Nelle poche posizioni in cui un'applicazione deve funzionare con dati di tipo carattere a 8 bit, può utilizzare esplicitamente le funzioni per le tabelle codici di Windows.</span><span class="sxs-lookup"><span data-stu-id="8fd35-118">In the few places where an application must work with 8-bit character data, it can make explicit use of the functions for Windows code pages.</span></span>

 

<span data-ttu-id="8fd35-119">L'applicazione deve sempre utilizzare un prototipo di funzione generico con tipi di carattere e di stringa generici.</span><span class="sxs-lookup"><span data-stu-id="8fd35-119">Your application should always use a generic function prototype with the generic string and character types.</span></span> <span data-ttu-id="8fd35-120">Tutti i nomi di funzione che terminano con una "W" maiuscola accettano Unicode, ovvero parametri con caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="8fd35-120">All function names that end with an uppercase "W" take Unicode, that is, wide character, parameters.</span></span> <span data-ttu-id="8fd35-121">Alcune funzioni sono disponibili solo nelle versioni Unicode e possono essere utilizzate solo con i tipi di dati appropriati.</span><span class="sxs-lookup"><span data-stu-id="8fd35-121">Some functions exist only in Unicode versions and can be used only with the appropriate data types.</span></span> <span data-ttu-id="8fd35-122">Ad esempio, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) e [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) hanno solo versioni Unicode.</span><span class="sxs-lookup"><span data-stu-id="8fd35-122">For example, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) and [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) have only Unicode versions.</span></span>

<span data-ttu-id="8fd35-123">La sezione requisiti nella documentazione di riferimento per ogni funzione di set di caratteri e Unicode fornisce informazioni sulle versioni di funzione implementate dai sistemi operativi supportati.</span><span class="sxs-lookup"><span data-stu-id="8fd35-123">The Requirements section in the reference documentation for each Unicode and character set function provides information on the function versions implemented by supported operating systems.</span></span> <span data-ttu-id="8fd35-124">Se è inclusa una riga che inizia con "Unicode", la funzione dispone di versioni separate della tabella codici Unicode e di Windows.</span><span class="sxs-lookup"><span data-stu-id="8fd35-124">If a line beginning with "Unicode" is included, the function has separate Unicode and Windows code page versions.</span></span>

> [!Note]  
> <span data-ttu-id="8fd35-125">Quando una funzione ha un parametro di lunghezza per una stringa di caratteri, la lunghezza deve essere documentata come conteggio dei valori di TCHAR nella stringa.</span><span class="sxs-lookup"><span data-stu-id="8fd35-125">When a function has a length parameter for a character string, the length should be documented as a count of TCHAR values in the string.</span></span> <span data-ttu-id="8fd35-126">Questo tipo di dati fa riferimento a byte per le versioni della tabella codici di Windows della funzione o parole a 16 bit per le versioni Unicode.</span><span class="sxs-lookup"><span data-stu-id="8fd35-126">This data type refers to bytes for Windows code page versions of the function or 16-bit words for Unicode versions.</span></span> <span data-ttu-id="8fd35-127">Tuttavia, le funzioni che richiedono o restituiscono puntatori a blocchi di memoria non tipizzata, ad esempio la funzione [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) , in genere accettano una dimensione in byte, indipendentemente dal prototipo utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8fd35-127">However, functions that require or return pointers to untyped memory blocks, such as the [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) function, generally take a size in bytes, regardless of the prototype that is used.</span></span> <span data-ttu-id="8fd35-128">Se l'allocazione della memoria non tipizzata è per una stringa, l'applicazione deve moltiplicare il numero di caratteri per sizeof (TCHAR).</span><span class="sxs-lookup"><span data-stu-id="8fd35-128">If the allocation of untyped memory is for a string, the application must multiply the number of characters by sizeof(TCHAR).</span></span> <span data-ttu-id="8fd35-129">Per ulteriori informazioni, vedere [utilizzo di tipi di dati generici](using-generic-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="8fd35-129">For additional information, see [Using Generic Data Types](using-generic-data-types.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8fd35-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8fd35-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fd35-131">Unicode nell'API Windows</span><span class="sxs-lookup"><span data-stu-id="8fd35-131">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 

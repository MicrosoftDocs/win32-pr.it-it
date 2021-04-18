---
description: Se si utilizzano tipi di dati generici nel codice, è possibile compilarli per Unicode semplicemente utilizzando una direttiva per il preprocessore per definire &\# 0034; UNICODE&\# 0034; prima delle \# istruzioni include per i file di intestazione.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Utilizzo di tipi di dati generici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2604f87b12e86076bed47f509c6398fa8482b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319481"
---
# <a name="using-generic-data-types"></a><span data-ttu-id="92aa6-103">Utilizzo di tipi di dati generici</span><span class="sxs-lookup"><span data-stu-id="92aa6-103">Using Generic Data Types</span></span>

<span data-ttu-id="92aa6-104">Se si utilizzano tipi di dati generici nel codice, è possibile compilarli per [Unicode](unicode.md) semplicemente utilizzando una direttiva per il preprocessore per definire "Unicode" prima delle istruzioni **\# include** per i file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="92aa6-104">If you use generic data types in your code, it can be compiled for [Unicode](unicode.md) simply by using a preprocessor directive to define "UNICODE" before the **\#include** statements for the header files.</span></span> <span data-ttu-id="92aa6-105">Per compilare le [tabelle codici ANSI (code for Windows)](code-pages.md), omettere la definizione "Unicode".</span><span class="sxs-lookup"><span data-stu-id="92aa6-105">To compile the code for [Windows (ANSI) code pages](code-pages.md), omit the "UNICODE" definition.</span></span> <span data-ttu-id="92aa6-106">Le nuove applicazioni Windows devono utilizzare Unicode per evitare le incoerenze di diverse tabelle codici e semplificare la localizzazione.</span><span class="sxs-lookup"><span data-stu-id="92aa6-106">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and simplify localization.</span></span>

<span data-ttu-id="92aa6-107">Per creare codice sorgente che può essere compilato per l'utilizzo di caratteri e stringhe Unicode o per l'utilizzo di caratteri e stringhe dalle tabelle codici di Windows:</span><span class="sxs-lookup"><span data-stu-id="92aa6-107">To create source code that can be compiled either to use Unicode characters and strings or to use characters and strings from Windows code pages:</span></span>

1.  <span data-ttu-id="92aa6-108">Utilizzare tipi di dati generici, ad esempio TCHAR, LPTSTR e LPTCH, per tutti i tipi di carattere e stringa utilizzati per il testo.</span><span class="sxs-lookup"><span data-stu-id="92aa6-108">Use generic data types, such as TCHAR, LPTSTR, and LPTCH, for all character and string types used for text.</span></span> <span data-ttu-id="92aa6-109">Per ulteriori informazioni sui tipi generici, vedere [tipi di dati di Windows per le stringhe](windows-data-types-for-strings.md).</span><span class="sxs-lookup"><span data-stu-id="92aa6-109">For more about generic types, see [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span>
2.  <span data-ttu-id="92aa6-110">Assicurarsi che i puntatori a buffer di dati non di testo o matrici di byte binari siano codificati con tipi di dati, ad esempio LPBYTE o LPWORD, anziché il tipo LPTSTR o LPTCH.</span><span class="sxs-lookup"><span data-stu-id="92aa6-110">Be sure that pointers to non-text data buffers or binary byte arrays are coded with data types such as LPBYTE or LPWORD, instead of the LPTSTR or LPTCH type.</span></span>
3.  <span data-ttu-id="92aa6-111">Dichiarare i puntatori del tipo indeterminato in modo esplicito come puntatori void usando LPVOID nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="92aa6-111">Declare pointers of indeterminate type explicitly as void pointers by using LPVOID as appropriate.</span></span>
4.  <span data-ttu-id="92aa6-112">Rendere indipendente dal tipo aritmetico del puntatore.</span><span class="sxs-lookup"><span data-stu-id="92aa6-112">Make pointer arithmetic type-independent.</span></span> <span data-ttu-id="92aa6-113">L'uso di unità di dimensioni TCHAR restituisce variabili che sono 2 byte se è definito UNICODE e 1 byte se UNICODE non è definito.</span><span class="sxs-lookup"><span data-stu-id="92aa6-113">Using units of TCHAR size yields variables that are 2 bytes if UNICODE is defined, and 1 byte if UNICODE is not defined.</span></span> <span data-ttu-id="92aa6-114">L'uso dell'aritmetica dei puntatori restituisce sempre il numero di elementi indicati dal puntatore, se le dimensioni degli elementi sono pari a 1 o 2 byte.</span><span class="sxs-lookup"><span data-stu-id="92aa6-114">Using pointer arithmetic always returns the number of elements indicated by the pointer, whether the elements are 1 or 2 bytes in size.</span></span> <span data-ttu-id="92aa6-115">L'espressione seguente recupera sempre il numero di elementi, indipendentemente dal fatto che sia definito UNICODE.</span><span class="sxs-lookup"><span data-stu-id="92aa6-115">The following expression always retrieves the number of elements, regardless of whether UNICODE is defined.</span></span>

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    <span data-ttu-id="92aa6-116">L'espressione seguente determina il numero di byte utilizzati.</span><span class="sxs-lookup"><span data-stu-id="92aa6-116">The following expression determines the number of bytes used.</span></span>

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    <span data-ttu-id="92aa6-117">Non è necessario modificare un'istruzione come quella riportata di seguito, perché l'incremento del puntatore punta all'elemento del carattere successivo.</span><span class="sxs-lookup"><span data-stu-id="92aa6-117">There is no need to change a statement like the following one, because the pointer increment points to the next character element.</span></span>

    ```C++
    chNext = *++lpText;
    ```

    

5.  <span data-ttu-id="92aa6-118">Sostituire stringhe letterali e costanti carattere manifesto con macro.</span><span class="sxs-lookup"><span data-stu-id="92aa6-118">Replace literal strings and manifest character constants with macros.</span></span> <span data-ttu-id="92aa6-119">Modificare le espressioni come quelle riportate di seguito.</span><span class="sxs-lookup"><span data-stu-id="92aa6-119">Change expressions like the following one.</span></span>

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    <span data-ttu-id="92aa6-120">Usare la macro di [**testo**](/windows/desktop/api/Winnt/nf-winnt-text) come indicato di seguito in questa espressione.</span><span class="sxs-lookup"><span data-stu-id="92aa6-120">Use the [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro as follows in this expression.</span></span>

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    <span data-ttu-id="92aa6-121">La macro di [**testo**](/windows/desktop/api/Winnt/nf-winnt-text) causa la valutazione delle stringhe come L "stringa" quando viene definito Unicode e come "stringa" in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="92aa6-121">The [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro causes strings to be evaluated as L"string" when UNICODE is defined, and as "string" otherwise.</span></span> <span data-ttu-id="92aa6-122">Per una gestione più semplice, spostare le stringhe letterali in risorse, soprattutto se contengono caratteri non compresi nell'intervallo ASCII (da 0x00 a 0x7F) o vengono esposti nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="92aa6-122">For easier management, move literal strings into resources, especially if they contain characters outside the ASCII range (0x00 through 0x7F) or are exposed at the user interface.</span></span> <span data-ttu-id="92aa6-123">Per supportare la localizzazione dell'applicazione per diverse lingue nazionali, è molto importante che tutte le stringhe dell'interfaccia utente siano in risorse localizzabili.</span><span class="sxs-lookup"><span data-stu-id="92aa6-123">To support localization of your application for different national languages, it is very important for all user interface strings to be in localizable resources.</span></span>

6.  <span data-ttu-id="92aa6-124">Usare le versioni generiche delle funzioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="92aa6-124">Use the generic versions of the Windows functions.</span></span> <span data-ttu-id="92aa6-125">Per altre informazioni, vedere [convenzioni per i prototipi di funzione](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="92aa6-125">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>
7.  <span data-ttu-id="92aa6-126">Usare le versioni generiche delle funzioni stringa della libreria C standard e ricordare di definire " \_ Unicode" e "Unicode", come descritto in [funzioni C standard](standard-c-functions.md).</span><span class="sxs-lookup"><span data-stu-id="92aa6-126">Use the generic versions of the standard C library string functions, and remember to define "\_UNICODE" as well as "UNICODE", as discussed in [Standard C Functions](standard-c-functions.md).</span></span>
8.  <span data-ttu-id="92aa6-127">Se si sta adattando un'applicazione originariamente scritta per le tabelle codici di Windows, ricordarsi di modificare il codice che si basa su 255 come valore più grande per un carattere.</span><span class="sxs-lookup"><span data-stu-id="92aa6-127">If you are adapting an application originally written for Windows code pages, remember to change any code that relies on 255 as the largest value for a character.</span></span>

<span data-ttu-id="92aa6-128">Quando si compila il codice scritto come descritto in precedenza, il compilatore può creare sia la versione Unicode che la tabella codici di Windows dell'applicazione dalla stessa origine.</span><span class="sxs-lookup"><span data-stu-id="92aa6-128">When you compile code that you have written as outlined above, the compiler can create both Unicode and Windows code page versions of your application from the same source.</span></span> <span data-ttu-id="92aa6-129">A seconda delle definizioni per UNICODE, le funzioni generiche vengono risolte per produrre gli stessi file binari come se fosse stato scritto codice esclusivamente per Unicode o solo per le tabelle codici di Windows.</span><span class="sxs-lookup"><span data-stu-id="92aa6-129">Depending on the definitions for UNICODE, the generic functions are resolved to produce the same binary files as if you wrote code exclusively for Unicode or exclusively for Windows code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92aa6-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="92aa6-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92aa6-131">Utilizzo di set di caratteri e Unicode</span><span class="sxs-lookup"><span data-stu-id="92aa6-131">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 




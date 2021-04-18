---
title: Convenzioni di codifica Windows
description: Se non si ha familiarità con la programmazione Windows, può essere sconcertante quando viene visualizzato per la prima volta un programma Windows.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c8509d7cb799bafdfa70c326f1074b64d93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299642"
---
# <a name="windows-coding-conventions"></a><span data-ttu-id="a3dad-103">Convenzioni di codifica Windows</span><span class="sxs-lookup"><span data-stu-id="a3dad-103">Windows Coding Conventions</span></span>

<span data-ttu-id="a3dad-104">Se non si ha familiarità con la programmazione Windows, può essere sconcertante quando viene visualizzato per la prima volta un programma Windows.</span><span class="sxs-lookup"><span data-stu-id="a3dad-104">If you are new to Windows programming, it can be disconcerting when you first see a Windows program.</span></span> <span data-ttu-id="a3dad-105">Il codice viene compilato con definizioni di tipo strano, ad esempio **DWORD \_ ptr** e **lpRect**, e le variabili hanno nomi quali *HWND* e *PWSZ* (denominata notazione ungherese).</span><span class="sxs-lookup"><span data-stu-id="a3dad-105">The code is filled with strange type definitions like **DWORD\_PTR** and **LPRECT**, and variables have names like *hWnd* and *pwsz* (called Hungarian notation).</span></span> <span data-ttu-id="a3dad-106">È opportuno apprendere alcune delle convenzioni di codifica di Windows.</span><span class="sxs-lookup"><span data-stu-id="a3dad-106">It's worth taking a moment to learn some of the Windows coding conventions.</span></span>

<span data-ttu-id="a3dad-107">La maggior parte delle API di Windows è costituita da funzioni o interfacce di Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="a3dad-107">The vast majority of Windows APIs consist of either functions or Component Object Model (COM) interfaces.</span></span> <span data-ttu-id="a3dad-108">Poche API Windows sono fornite come classi C++.</span><span class="sxs-lookup"><span data-stu-id="a3dad-108">Very few Windows APIs are provided as C++ classes.</span></span> <span data-ttu-id="a3dad-109">Un'eccezione significativa è GDI+, una delle API grafiche 2D.</span><span class="sxs-lookup"><span data-stu-id="a3dad-109">(A notable exception is GDI+, one of the 2-D graphics APIs.)</span></span>

## <a name="typedefs"></a><span data-ttu-id="a3dad-110">Typedef</span><span class="sxs-lookup"><span data-stu-id="a3dad-110">Typedefs</span></span>

<span data-ttu-id="a3dad-111">Le intestazioni di Windows contengono numerosi typedef.</span><span class="sxs-lookup"><span data-stu-id="a3dad-111">The Windows headers contain a lot of typedefs.</span></span> <span data-ttu-id="a3dad-112">Molti di questi vengono definiti nel file di intestazione WinDef. h.</span><span class="sxs-lookup"><span data-stu-id="a3dad-112">Many of these are defined in the header file WinDef.h.</span></span> <span data-ttu-id="a3dad-113">Di seguito sono riportati alcuni dei problemi che si verificheranno spesso.</span><span class="sxs-lookup"><span data-stu-id="a3dad-113">Here are some that you will encounter often.</span></span>

### <a name="integer-types"></a><span data-ttu-id="a3dad-114">Tipi integer</span><span class="sxs-lookup"><span data-stu-id="a3dad-114">Integer types</span></span>



| <span data-ttu-id="a3dad-115">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a3dad-115">Data type</span></span>     | <span data-ttu-id="a3dad-116">Dimensione</span><span class="sxs-lookup"><span data-stu-id="a3dad-116">Size</span></span>    | <span data-ttu-id="a3dad-117">Con segno?</span><span class="sxs-lookup"><span data-stu-id="a3dad-117">Signed?</span></span>  |
|---------------|---------|----------|
| <span data-ttu-id="a3dad-118">**BYTE**</span><span class="sxs-lookup"><span data-stu-id="a3dad-118">**BYTE**</span></span>      | <span data-ttu-id="a3dad-119">8 bit</span><span class="sxs-lookup"><span data-stu-id="a3dad-119">8 bits</span></span>  | <span data-ttu-id="a3dad-120">Senza segno</span><span class="sxs-lookup"><span data-stu-id="a3dad-120">Unsigned</span></span> |
| <span data-ttu-id="a3dad-121">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="a3dad-121">**DWORD**</span></span>     | <span data-ttu-id="a3dad-122">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3dad-122">32 bits</span></span> | <span data-ttu-id="a3dad-123">Senza segno</span><span class="sxs-lookup"><span data-stu-id="a3dad-123">Unsigned</span></span> |
| <span data-ttu-id="a3dad-124">**INT32**</span><span class="sxs-lookup"><span data-stu-id="a3dad-124">**INT32**</span></span>     | <span data-ttu-id="a3dad-125">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3dad-125">32 bits</span></span> | <span data-ttu-id="a3dad-126">Firmato</span><span class="sxs-lookup"><span data-stu-id="a3dad-126">Signed</span></span>   |
| <span data-ttu-id="a3dad-127">**INT64**</span><span class="sxs-lookup"><span data-stu-id="a3dad-127">**INT64**</span></span>     | <span data-ttu-id="a3dad-128">64 bit</span><span class="sxs-lookup"><span data-stu-id="a3dad-128">64 bits</span></span> | <span data-ttu-id="a3dad-129">Firmato</span><span class="sxs-lookup"><span data-stu-id="a3dad-129">Signed</span></span>   |
| <span data-ttu-id="a3dad-130">**LONG**</span><span class="sxs-lookup"><span data-stu-id="a3dad-130">**LONG**</span></span>      | <span data-ttu-id="a3dad-131">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3dad-131">32 bits</span></span> | <span data-ttu-id="a3dad-132">Firmato</span><span class="sxs-lookup"><span data-stu-id="a3dad-132">Signed</span></span>   |
| <span data-ttu-id="a3dad-133">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="a3dad-133">**LONGLONG**</span></span>  | <span data-ttu-id="a3dad-134">64 bit</span><span class="sxs-lookup"><span data-stu-id="a3dad-134">64 bits</span></span> | <span data-ttu-id="a3dad-135">Firmato</span><span class="sxs-lookup"><span data-stu-id="a3dad-135">Signed</span></span>   |
| <span data-ttu-id="a3dad-136">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a3dad-136">**UINT32**</span></span>    | <span data-ttu-id="a3dad-137">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3dad-137">32 bits</span></span> | <span data-ttu-id="a3dad-138">Senza segno</span><span class="sxs-lookup"><span data-stu-id="a3dad-138">Unsigned</span></span> |
| <span data-ttu-id="a3dad-139">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="a3dad-139">**UINT64**</span></span>    | <span data-ttu-id="a3dad-140">64 bit</span><span class="sxs-lookup"><span data-stu-id="a3dad-140">64 bits</span></span> | <span data-ttu-id="a3dad-141">Senza segno</span><span class="sxs-lookup"><span data-stu-id="a3dad-141">Unsigned</span></span> |
| <span data-ttu-id="a3dad-142">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="a3dad-142">**ULONG**</span></span>     | <span data-ttu-id="a3dad-143">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3dad-143">32 bits</span></span> | <span data-ttu-id="a3dad-144">Senza segno</span><span class="sxs-lookup"><span data-stu-id="a3dad-144">Unsigned</span></span> |
| <span data-ttu-id="a3dad-145">**ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="a3dad-145">**ULONGLONG**</span></span> | <span data-ttu-id="a3dad-146">64 bit</span><span class="sxs-lookup"><span data-stu-id="a3dad-146">64 bits</span></span> | <span data-ttu-id="a3dad-147">Senza segno</span><span class="sxs-lookup"><span data-stu-id="a3dad-147">Unsigned</span></span> |
| <span data-ttu-id="a3dad-148">**WORD**</span><span class="sxs-lookup"><span data-stu-id="a3dad-148">**WORD**</span></span>      | <span data-ttu-id="a3dad-149">16 bit</span><span class="sxs-lookup"><span data-stu-id="a3dad-149">16 bits</span></span> | <span data-ttu-id="a3dad-150">Senza segno</span><span class="sxs-lookup"><span data-stu-id="a3dad-150">Unsigned</span></span> |



 

<span data-ttu-id="a3dad-151">Come si può notare, in questi typedef esiste una certa quantità di ridondanza.</span><span class="sxs-lookup"><span data-stu-id="a3dad-151">As you can see, there is a certain amount of redundancy in these typedefs.</span></span> <span data-ttu-id="a3dad-152">Alcune di queste sovrapposizioni sono semplicemente dovute alla cronologia delle API di Windows.</span><span class="sxs-lookup"><span data-stu-id="a3dad-152">Some of this overlap is simply due to the history of the Windows APIs.</span></span> <span data-ttu-id="a3dad-153">I tipi elencati di seguito hanno dimensioni fisse e le dimensioni sono le stesse nelle applicazioni a 32 bit e 64.</span><span class="sxs-lookup"><span data-stu-id="a3dad-153">The types listed here have fixed size, and the sizes are the same in both 32-bit and 64-applications.</span></span> <span data-ttu-id="a3dad-154">Il tipo **DWORD** , ad esempio, è sempre di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a3dad-154">For example, the **DWORD** type is always 32 bits wide.</span></span>

### <a name="boolean-type"></a><span data-ttu-id="a3dad-155">Tipo Boolean</span><span class="sxs-lookup"><span data-stu-id="a3dad-155">Boolean Type</span></span>

<span data-ttu-id="a3dad-156">**Bool** è un typedef per un valore integer usato in un contesto booleano.</span><span class="sxs-lookup"><span data-stu-id="a3dad-156">**BOOL** is a typedef for an integer value that is used in a Boolean context.</span></span> <span data-ttu-id="a3dad-157">Il file di intestazione WinDef. h definisce anche due valori da usare con **bool**.</span><span class="sxs-lookup"><span data-stu-id="a3dad-157">The header file WinDef.h also defines two values for use with **BOOL**.</span></span>


```C++
#define FALSE    0 
#define TRUE     1
```



<span data-ttu-id="a3dad-158">Nonostante questa definizione di **true**, tuttavia, la maggior parte delle funzioni che restituiscono un tipo **bool** può restituire qualsiasi valore diverso da zero per indicare la verità booleana.</span><span class="sxs-lookup"><span data-stu-id="a3dad-158">Despite this definition of **TRUE**, however, most functions that return a **BOOL** type can return any non-zero value to indicate Boolean truth.</span></span> <span data-ttu-id="a3dad-159">Pertanto, è sempre necessario scrivere questo:</span><span class="sxs-lookup"><span data-stu-id="a3dad-159">Therefore, you should always write this:</span></span>


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



<span data-ttu-id="a3dad-160">e non:</span><span class="sxs-lookup"><span data-stu-id="a3dad-160">and not this:</span></span>


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



<span data-ttu-id="a3dad-161">Tenere presente che **bool** è un tipo integer e non è interscambiabile con il tipo C++ **bool** .</span><span class="sxs-lookup"><span data-stu-id="a3dad-161">Be aware that **BOOL** is an integer type and is not interchangeable with the C++ **bool** type.</span></span>

### <a name="pointer-types"></a><span data-ttu-id="a3dad-162">Tipi di puntatore</span><span class="sxs-lookup"><span data-stu-id="a3dad-162">Pointer Types</span></span>

<span data-ttu-id="a3dad-163">Windows definisce molti tipi di dati del form *puntatore a X*.</span><span class="sxs-lookup"><span data-stu-id="a3dad-163">Windows defines many data types of the form *pointer-to-X*.</span></span> <span data-ttu-id="a3dad-164">In genere il prefisso *P-* o *LP-* nel nome.</span><span class="sxs-lookup"><span data-stu-id="a3dad-164">These usually have the prefix *P-* or *LP-* in the name.</span></span> <span data-ttu-id="a3dad-165">Ad esempio, **lpRect** è un puntatore a un oggetto [**Rect**](/previous-versions//dd162897(v=vs.85)), dove **Rect** è una struttura che descrive un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="a3dad-165">For example, **LPRECT** is a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)), where **RECT** is a structure that describes a rectangle.</span></span> <span data-ttu-id="a3dad-166">Le seguenti dichiarazioni di variabili sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="a3dad-166">The following variable declarations are equivalent.</span></span>


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



<span data-ttu-id="a3dad-167">In passato, *P* sta per "pointer" e *LP* sta per "Long pointer".</span><span class="sxs-lookup"><span data-stu-id="a3dad-167">Historically, *P* stands for "pointer" and *LP* stands for "long pointer".</span></span> <span data-ttu-id="a3dad-168">I puntatori lunghi (detti anche *puntatori lontani*) sono retaggio da Windows a 16 bit, quando sono necessari per indirizzare gli intervalli di memoria all'esterno del segmento corrente.</span><span class="sxs-lookup"><span data-stu-id="a3dad-168">Long pointers (also called *far pointers*) are a holdover from 16-bit Windows, when they were needed to address memory ranges outside the current segment.</span></span> <span data-ttu-id="a3dad-169">Il prefisso *LP* è stato mantenuto per semplificare la porta del codice a 16 bit in Windows a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a3dad-169">The *LP* prefix was preserved to make it easier to port 16-bit code to 32-bit Windows.</span></span> <span data-ttu-id="a3dad-170">Attualmente non esiste alcuna distinzione: un puntatore è un puntatore.</span><span class="sxs-lookup"><span data-stu-id="a3dad-170">Today there is no distinction — a pointer is a pointer.</span></span>

### <a name="pointer-precision-types"></a><span data-ttu-id="a3dad-171">Tipi di precisione del puntatore</span><span class="sxs-lookup"><span data-stu-id="a3dad-171">Pointer Precision Types</span></span>

<span data-ttu-id="a3dad-172">I tipi di dati riportati di seguito sono sempre le dimensioni di un puntatore, ovvero 32 bit a larghezza nelle applicazioni a 32 bit e 64 bit in larghezza nelle applicazioni a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="a3dad-172">The following data types are always the size of a pointer—that is, 32 bits wide in 32-bit applications, and 64 bits wide in 64-bit applications.</span></span> <span data-ttu-id="a3dad-173">La dimensione viene determinata in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="a3dad-173">The size is determined at compile time.</span></span> <span data-ttu-id="a3dad-174">Quando un'applicazione a 32 bit viene eseguita in Windows a 64 bit, questi tipi di dati sono ancora di 4 byte.</span><span class="sxs-lookup"><span data-stu-id="a3dad-174">When a 32-bit application runs on 64-bit Windows, these data types are still 4 bytes wide.</span></span> <span data-ttu-id="a3dad-175">Non è possibile eseguire un'applicazione a 64 bit su Windows a 32 bit, quindi non si verifica la situazione inversa.</span><span class="sxs-lookup"><span data-stu-id="a3dad-175">(A 64-bit application cannot run on 32-bit Windows, so the reverse situation does not occur.)</span></span>

-   <span data-ttu-id="a3dad-176">**\_ptr DWORD**</span><span class="sxs-lookup"><span data-stu-id="a3dad-176">**DWORD\_PTR**</span></span>
-   <span data-ttu-id="a3dad-177">**\_ptr int**</span><span class="sxs-lookup"><span data-stu-id="a3dad-177">**INT\_PTR**</span></span>
-   <span data-ttu-id="a3dad-178">**LONG \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="a3dad-178">**LONG\_PTR**</span></span>
-   <span data-ttu-id="a3dad-179">**\_ptr ULONG**</span><span class="sxs-lookup"><span data-stu-id="a3dad-179">**ULONG\_PTR**</span></span>
-   <span data-ttu-id="a3dad-180">**\_ptr uint**</span><span class="sxs-lookup"><span data-stu-id="a3dad-180">**UINT\_PTR**</span></span>

<span data-ttu-id="a3dad-181">Questi tipi vengono utilizzati nelle situazioni in cui è possibile eseguire il cast di un numero intero a un puntatore.</span><span class="sxs-lookup"><span data-stu-id="a3dad-181">These types are used in situations where an integer might be cast to a pointer.</span></span> <span data-ttu-id="a3dad-182">Vengono inoltre utilizzate per definire le variabili per l'aritmetica dei puntatori e per definire i contatori del ciclo che eseguono l'iterazione sull'intervallo completo di byte nei buffer di memoria.</span><span class="sxs-lookup"><span data-stu-id="a3dad-182">They are also used to define variables for pointer arithmetic and to define loop counters that iterate over the full range of bytes in memory buffers.</span></span> <span data-ttu-id="a3dad-183">Più in generale, vengono visualizzati in posizioni in cui un valore esistente a 32 bit è stato espanso a 64 bit in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="a3dad-183">More generally, they appear in places where an existing 32-bit value was expanded to 64 bits on 64-bit Windows.</span></span>

## <a name="hungarian-notation"></a><span data-ttu-id="a3dad-184">Notazione ungherese</span><span class="sxs-lookup"><span data-stu-id="a3dad-184">Hungarian Notation</span></span>

<span data-ttu-id="a3dad-185">La *notazione ungherese* è la pratica di aggiungere i prefissi ai nomi delle variabili, per fornire informazioni aggiuntive sulla variabile.</span><span class="sxs-lookup"><span data-stu-id="a3dad-185">*Hungarian notation* is the practice of adding prefixes to the names of variables, to give additional information about the variable.</span></span> <span data-ttu-id="a3dad-186">(L'inventore della notazione, Charles Simonyi, era ungherese, quindi il suo nome).</span><span class="sxs-lookup"><span data-stu-id="a3dad-186">(The notation's inventor, Charles Simonyi, was Hungarian, hence its name).</span></span>

<span data-ttu-id="a3dad-187">Nella sua forma originale, la notazione ungherese fornisce informazioni *semantiche* su una variabile, che indicano l'uso previsto.</span><span class="sxs-lookup"><span data-stu-id="a3dad-187">In its original form, Hungarian notation gives *semantic* information about a variable, telling you the intended use.</span></span> <span data-ttu-id="a3dad-188">Ad esempio, un indice, *CB* indica una dimensione in byte ("count of bytes") e *i* numeri di riga e di colonna di *RW* e *col* mean.</span><span class="sxs-lookup"><span data-stu-id="a3dad-188">For example, *i* means an index, *cb* means a size in bytes ("count of bytes"), and *rw* and *col* mean row and column numbers.</span></span> <span data-ttu-id="a3dad-189">Questi prefissi sono progettati per evitare l'uso accidentale di una variabile nel contesto errato.</span><span class="sxs-lookup"><span data-stu-id="a3dad-189">These prefixes are designed to avoid the accidental use of a variable in the wrong context.</span></span> <span data-ttu-id="a3dad-190">Se, ad esempio, l'espressione è stata riguardata `rwPosition +  cbTable` , è possibile che venga aggiunto un numero di riga a una dimensione, che è quasi certamente un bug nel codice</span><span class="sxs-lookup"><span data-stu-id="a3dad-190">For example, if you saw the expression `rwPosition +  cbTable`, you would know that a row number is being added to a size, which is almost certainly a bug in the code</span></span>

<span data-ttu-id="a3dad-191">Una forma più comune di notazione ungherese usa i prefissi per fornire informazioni sul *tipo* , ad esempio *DW* per **DWORD** e *w* per **Word**.</span><span class="sxs-lookup"><span data-stu-id="a3dad-191">A more common form of Hungarian notation uses prefixes to give *type* information—for example, *dw* for **DWORD** and *w* for **WORD**.</span></span>

<span data-ttu-id="a3dad-192">Se si esegue una ricerca nel Web di "notazione ungherese", sono disponibili numerose opinioni sulla presenza di una notazione ungherese valida o negativa.</span><span class="sxs-lookup"><span data-stu-id="a3dad-192">If you search the Web for "Hungarian notation," you will find a lot of opinions about whether Hungarian notation is good or bad.</span></span> <span data-ttu-id="a3dad-193">Alcuni programmatori hanno un'intensa antipatia per la notazione ungherese.</span><span class="sxs-lookup"><span data-stu-id="a3dad-193">Some programmers have an intense dislike for Hungarian notation.</span></span> <span data-ttu-id="a3dad-194">Altri lo trovano utile.</span><span class="sxs-lookup"><span data-stu-id="a3dad-194">Others find it helpful.</span></span> <span data-ttu-id="a3dad-195">Indipendentemente, molti degli esempi di codice su MSDN usano la notazione ungherese, ma non è necessario memorizzare i prefissi per comprendere il codice.</span><span class="sxs-lookup"><span data-stu-id="a3dad-195">Regardless, many of the code examples on MSDN use Hungarian notation, but you don't need to memorize the prefixes to understand the code.</span></span>

## <a name="next"></a><span data-ttu-id="a3dad-196">Prossima</span><span class="sxs-lookup"><span data-stu-id="a3dad-196">Next</span></span>

[<span data-ttu-id="a3dad-197">Uso delle stringhe</span><span class="sxs-lookup"><span data-stu-id="a3dad-197">Working with Strings</span></span>](working-with-strings.md)

 

 
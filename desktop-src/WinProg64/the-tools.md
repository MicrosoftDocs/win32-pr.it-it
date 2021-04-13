---
title: Strumenti
description: In questo argomento vengono descritti gli strumenti disponibili per la preparazione dell'applicazione a 64 bit. Windows 10 è disponibile sia per i processori x64 che per quelli basati su ARM64.
ms.assetid: 457b7cc1-8517-4a36-9a0c-cf191ff3b374
keywords:
- Guida alla programmazione di Windows a 64 bit Guida alla programmazione Windows a 64 bit, strumenti
- strumenti per la programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87fb315200ae32eb1e1441ed330be49aa02d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396563"
---
# <a name="the-tools"></a><span data-ttu-id="b36be-106">Strumenti</span><span class="sxs-lookup"><span data-stu-id="b36be-106">The Tools</span></span>

<span data-ttu-id="b36be-107">In questo argomento vengono descritti gli strumenti disponibili per la preparazione dell'applicazione a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b36be-107">This topic describes the tools available for you to use in making your application 64-bit ready.</span></span> <span data-ttu-id="b36be-108">Windows 10 è disponibile sia per i processori x64 che per quelli basati su ARM64.</span><span class="sxs-lookup"><span data-stu-id="b36be-108">Windows 10 is available for both x64 and ARM64 based processors.</span></span>

## <a name="include-files"></a><span data-ttu-id="b36be-109">File di inclusione</span><span class="sxs-lookup"><span data-stu-id="b36be-109">Include Files</span></span>

<span data-ttu-id="b36be-110">Gli elementi API sono praticamente identici tra le finestre a 32 e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b36be-110">The API elements are virtually identical between 32- and 64-bit Windows.</span></span> <span data-ttu-id="b36be-111">I file di intestazione di Windows sono stati modificati in modo che possano essere usati sia per il codice a 32 che per il codice a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b36be-111">The Windows header files have been modified so that they can be used for both 32- and 64-bit code.</span></span> <span data-ttu-id="b36be-112">I nuovi tipi e macro a 64 bit sono definiti in un nuovo file di intestazione, Basetsd. h, che si trova nel set di file di intestazione incluso in Windows. h.</span><span class="sxs-lookup"><span data-stu-id="b36be-112">The new 64-bit types and macros are defined in a new header file, Basetsd.h, which is in the set of header files included by Windows.h.</span></span> <span data-ttu-id="b36be-113">Basetsd. h include le nuove definizioni dei tipi di dati che facilitano la creazione di codice sorgente indipendente dalla dimensione delle parole.</span><span class="sxs-lookup"><span data-stu-id="b36be-113">Basetsd.h includes the new data-type definitions to assist in making source code word-size independent.</span></span>

## <a name="new-data-types"></a><span data-ttu-id="b36be-114">Nuovi tipi di dati</span><span class="sxs-lookup"><span data-stu-id="b36be-114">New Data Types</span></span>

<span data-ttu-id="b36be-115">I file di intestazione di Windows contengono nuovi tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="b36be-115">The Windows header files contain new data types.</span></span> <span data-ttu-id="b36be-116">Questi tipi sono principalmente per la compatibilità dei tipi con i tipi di dati a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="b36be-116">These types are primarily for type compatibility with the 32-bit data types.</span></span> <span data-ttu-id="b36be-117">I nuovi tipi forniscono esattamente la stessa digitazione dei tipi esistenti, garantendo allo stesso tempo il supporto per le finestre a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b36be-117">The new types provide exactly the same typing as the existing types, while at the same time providing support for the 64-bit Windows.</span></span> <span data-ttu-id="b36be-118">Per ulteriori informazioni, vedere [i nuovi tipi di dati](the-new-data-types.md) o il file di intestazione Basetsd. h.</span><span class="sxs-lookup"><span data-stu-id="b36be-118">For more information, see [The New Data Types](the-new-data-types.md) or the Basetsd.h header file.</span></span>

## <a name="predefined-macros"></a><span data-ttu-id="b36be-119">Macro predefinite</span><span class="sxs-lookup"><span data-stu-id="b36be-119">Predefined Macros</span></span>

<span data-ttu-id="b36be-120">Il compilatore definisce le macro seguenti per identificare la piattaforma.</span><span class="sxs-lookup"><span data-stu-id="b36be-120">The compiler defines the following macros to identify the platform.</span></span>



| <span data-ttu-id="b36be-121">Macro</span><span class="sxs-lookup"><span data-stu-id="b36be-121">Macro</span></span>   | <span data-ttu-id="b36be-122">Significato</span><span class="sxs-lookup"><span data-stu-id="b36be-122">Meaning</span></span>                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b36be-123">\_WIN64</span><span class="sxs-lookup"><span data-stu-id="b36be-123">\_WIN64</span></span> | <span data-ttu-id="b36be-124">Piattaforma A 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b36be-124">A 64-bit platform.</span></span> <span data-ttu-id="b36be-125">Sono inclusi sia x64 che ARM64.</span><span class="sxs-lookup"><span data-stu-id="b36be-125">This includes both x64 and ARM64.</span></span>                                                        |
| <span data-ttu-id="b36be-126">\_WIN32</span><span class="sxs-lookup"><span data-stu-id="b36be-126">\_WIN32</span></span> | <span data-ttu-id="b36be-127">Piattaforma A 32 bit.</span><span class="sxs-lookup"><span data-stu-id="b36be-127">A 32-bit platform.</span></span> <span data-ttu-id="b36be-128">Questo valore è definito anche dal compilatore a 64 bit per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="b36be-128">This value is also defined by the 64-bit compiler for backward compatibility.</span></span><br/> |
| <span data-ttu-id="b36be-129">\_WIN16</span><span class="sxs-lookup"><span data-stu-id="b36be-129">\_WIN16</span></span> | <span data-ttu-id="b36be-130">Piattaforma A 16 bit</span><span class="sxs-lookup"><span data-stu-id="b36be-130">A 16-bit platform</span></span>                                                                                           |



 

<span data-ttu-id="b36be-131">Le macro seguenti sono specifiche dell'architettura.</span><span class="sxs-lookup"><span data-stu-id="b36be-131">The following macros are specific to the architecture.</span></span>



| <span data-ttu-id="b36be-132">Macro</span><span class="sxs-lookup"><span data-stu-id="b36be-132">Macro</span></span>      | <span data-ttu-id="b36be-133">Significato</span><span class="sxs-lookup"><span data-stu-id="b36be-133">Meaning</span></span>                |
|------------|------------------------|
| <span data-ttu-id="b36be-134">\_M \_ ia64</span><span class="sxs-lookup"><span data-stu-id="b36be-134">\_M\_IA64</span></span>  | <span data-ttu-id="b36be-135">Piattaforma Intel Itanium</span><span class="sxs-lookup"><span data-stu-id="b36be-135">Intel Itanium platform</span></span> |
| <span data-ttu-id="b36be-136">\_\_Ix86 M</span><span class="sxs-lookup"><span data-stu-id="b36be-136">\_M\_IX86</span></span>  | <span data-ttu-id="b36be-137">piattaforma x86</span><span class="sxs-lookup"><span data-stu-id="b36be-137">x86 platform</span></span>           |
| <span data-ttu-id="b36be-138">\_M \_ x64</span><span class="sxs-lookup"><span data-stu-id="b36be-138">\_M\_X64</span></span>   | <span data-ttu-id="b36be-139">piattaforma x64</span><span class="sxs-lookup"><span data-stu-id="b36be-139">x64 platform</span></span>           |
| <span data-ttu-id="b36be-140">\_\_Arm64 M</span><span class="sxs-lookup"><span data-stu-id="b36be-140">\_M\_ARM64</span></span> | <span data-ttu-id="b36be-141">Piattaforma ARM64</span><span class="sxs-lookup"><span data-stu-id="b36be-141">ARM64 platform</span></span>         |



 

<span data-ttu-id="b36be-142">Non usare queste macro tranne che con codice specifico dell'architettura, invece, \_ se possibile, usare Win64, \_ Win32 e \_ Win16.</span><span class="sxs-lookup"><span data-stu-id="b36be-142">Do not use these macros except with architecture-specific code, instead, use \_WIN64, \_WIN32, and \_WIN16 whenever possible.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="b36be-143">Funzioni di supporto</span><span class="sxs-lookup"><span data-stu-id="b36be-143">Helper Functions</span></span>

<span data-ttu-id="b36be-144">Le funzioni inline seguenti, definite in Basetsd. h, consentono di convertire in modo sicuro i valori da un tipo a un altro.</span><span class="sxs-lookup"><span data-stu-id="b36be-144">The following inline functions (defined in Basetsd.h) can help you safely convert values from one type to another.</span></span>

``` syntax
void            * Handle64ToHandle( const void * POINTER_64 h ) 
void * POINTER_64 HandleToHandle64( const void *h )
long              HandleToLong(     const void *h )
unsigned long     HandleToUlong(    const void *h )
void            * IntToPtr(         const int i )
void            * LongToHandle(     const long h )
void            * LongToPtr(        const long l )
void            * Ptr64ToPtr(       const void * POINTER_64 p )
int               PtrToInt(         const void *p )
long              PtrToLong(        const void *p )
void * POINTER_64 PtrToPtr64(       const void *p )
short             PtrToShort(       const void *p )
unsigned int      PtrToUint(        const void *p )
unsigned long     PtrToUlong(       const void *p )
unsigned short    PtrToUshort(      const void *p )
void            * UIntToPtr(        const unsigned int ui )
void            * ULongToPtr(       const unsigned long ul )
```

> [!WARNING]
> <span data-ttu-id="b36be-145">**IntToPtr** Sign-estende il valore **int** , **UIntToPtr** zero-estende il valore **int senza segno** , **LongToPtr** Sign-estende il valore **Long** e **ULongToPtr** zero-estende il valore **Long senza segno** .</span><span class="sxs-lookup"><span data-stu-id="b36be-145">**IntToPtr** sign-extends the **int** value, **UIntToPtr** zero-extends the **unsigned int** value, **LongToPtr** sign-extends the **long** value, and **ULongToPtr** zero-extends the **unsigned long** value.</span></span>

 

## <a name="64-bit-compiler"></a><span data-ttu-id="b36be-146">Compilatore a 64 bit</span><span class="sxs-lookup"><span data-stu-id="b36be-146">64-bit Compiler</span></span>

<span data-ttu-id="b36be-147">I compilatori a 64 bit possono essere utilizzati per identificare il troncamento del puntatore, i cast di tipo non corretti e altri problemi specifici di 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b36be-147">The 64-bit compilers can be used to identify pointer truncation, improper type casts, and other 64-bit-specific problems.</span></span>

<span data-ttu-id="b36be-148">Quando il compilatore viene eseguito per la prima volta, probabilmente genererà molti avvisi di troncamento o di mancata corrispondenza del tipo, come i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b36be-148">When the compiler is first run, it will probably generate many pointer truncation or type mismatch warnings, such as the following:</span></span>

`warning C4311: 'type cast' : pointer truncation from 'unsigned char *' to 'unsigned long '`

<span data-ttu-id="b36be-149">Usare questi avvisi come guida per rendere il codice più affidabile.</span><span class="sxs-lookup"><span data-stu-id="b36be-149">Use these warnings as a guide to make the code more robust.</span></span> <span data-ttu-id="b36be-150">È consigliabile eliminare tutti gli avvisi, in particolare gli avvisi di troncamento del puntatore.</span><span class="sxs-lookup"><span data-stu-id="b36be-150">It is good practice to eliminate all warnings, especially pointer-truncation warnings.</span></span>

## <a name="64-bit-compiler-switches-and-warnings"></a><span data-ttu-id="b36be-151">commutatori e avvisi del compilatore a 64 bit</span><span class="sxs-lookup"><span data-stu-id="b36be-151">64-bit Compiler Switches and Warnings</span></span>

<span data-ttu-id="b36be-152">Si noti che questo compilatore Abilita il modello di dati LLP64.</span><span class="sxs-lookup"><span data-stu-id="b36be-152">Note that this compiler enables the LLP64 data model.</span></span>

<span data-ttu-id="b36be-153">È disponibile un'opzione di avviso per facilitare il porting a LLP64.</span><span class="sxs-lookup"><span data-stu-id="b36be-153">There is a warning option to assist porting to LLP64.</span></span> <span data-ttu-id="b36be-154">L'opzione-Wp64 (-W3 Abilita gli avvisi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b36be-154">The -Wp64 -W3 switch enables the following warnings:</span></span>

-   <span data-ttu-id="b36be-155">C4305: avviso di troncamento.</span><span class="sxs-lookup"><span data-stu-id="b36be-155">C4305: Truncation warning.</span></span> <span data-ttu-id="b36be-156">Ad esempio, "Return": troncamento da "unsigned int64" a "Long".</span><span class="sxs-lookup"><span data-stu-id="b36be-156">For example, "return": truncation from "unsigned int64" to "long."</span></span>
-   <span data-ttu-id="b36be-157">C4311: avviso di troncamento.</span><span class="sxs-lookup"><span data-stu-id="b36be-157">C4311: Truncation warning.</span></span> <span data-ttu-id="b36be-158">Ad esempio, "cast di tipo": troncamento puntatore da "int \* \_ ptr64" a "int".</span><span class="sxs-lookup"><span data-stu-id="b36be-158">For example, "type cast": pointer truncation from "int\*\_ptr64" to "int."</span></span>
-   <span data-ttu-id="b36be-159">C4312: conversione a un avviso di dimensioni maggiori.</span><span class="sxs-lookup"><span data-stu-id="b36be-159">C4312: Conversion to bigger-size warning.</span></span> <span data-ttu-id="b36be-160">Ad esempio, "Type cast": conversione da "int" a "int \* \_ ptr64" di dimensioni maggiori.</span><span class="sxs-lookup"><span data-stu-id="b36be-160">For example, "type cast": conversion from "int" to "int\*\_ptr64" of greater size.</span></span>
-   <span data-ttu-id="b36be-161">C4318: passaggio di lunghezza zero.</span><span class="sxs-lookup"><span data-stu-id="b36be-161">C4318: Passing zero length.</span></span> <span data-ttu-id="b36be-162">Ad esempio, passando la costante zero come lunghezza alla funzione **memset** .</span><span class="sxs-lookup"><span data-stu-id="b36be-162">For example, passing constant zero as the length to the **memset** function.</span></span>
-   <span data-ttu-id="b36be-163">Operatore C4319: not.</span><span class="sxs-lookup"><span data-stu-id="b36be-163">C4319: Not operator.</span></span> <span data-ttu-id="b36be-164">Ad esempio, "~": zero che estende "unsigned long" a "unsigned \_ Int64" of Greater size.</span><span class="sxs-lookup"><span data-stu-id="b36be-164">For example, "~": zero extending "unsigned long" to "unsigned \_int64" of greater size.</span></span>
-   <span data-ttu-id="b36be-165">C4313: chiamata della famiglia **printf** di funzioni con identificatori e argomenti di tipo conversione in conflitto.</span><span class="sxs-lookup"><span data-stu-id="b36be-165">C4313: Calling the **printf** family of functions with conflicting conversion type specifiers and arguments.</span></span> <span data-ttu-id="b36be-166">Ad esempio, "printf": "% p" nella stringa di formato è in conflitto con l'argomento 2 di tipo " \_ Int64".</span><span class="sxs-lookup"><span data-stu-id="b36be-166">For example, "printf": "%p" in format string conflicts with argument 2 of type "\_int64."</span></span> <span data-ttu-id="b36be-167">Un altro esempio è la chiamata printf ("% x", il valore del puntatore \_ ); causa un troncamento dei bit 32 superiori.</span><span class="sxs-lookup"><span data-stu-id="b36be-167">Another example is the call printf("%x", pointer\_value); this causes a truncation of the upper 32 bits.</span></span> <span data-ttu-id="b36be-168">La chiamata corretta è printf ("% p", valore del puntatore \_ ).</span><span class="sxs-lookup"><span data-stu-id="b36be-168">The correct call is printf("%p", pointer\_value).</span></span>
-   <span data-ttu-id="b36be-169">C4244: uguale all'avviso C4242 esistente.</span><span class="sxs-lookup"><span data-stu-id="b36be-169">C4244: Same as the existing warning C4242.</span></span> <span data-ttu-id="b36be-170">Ad esempio, "Return": conversione da " \_ Int64" a "unsigned int", possibile perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="b36be-170">For example, "return": conversion from "\_int64" to "unsigned int," possible loss of data.</span></span>

## <a name="64-bit-linker-and-libraries"></a><span data-ttu-id="b36be-171">Linker e librerie a 64 bit</span><span class="sxs-lookup"><span data-stu-id="b36be-171">64-bit Linker and Libraries</span></span>

<span data-ttu-id="b36be-172">Per compilare applicazioni, usare il linker e le librerie fornite dal Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b36be-172">To build applications, use the linker and libraries provided by the Windows SDK.</span></span> <span data-ttu-id="b36be-173">La maggior parte delle librerie a 32 bit ha una versione a 64 bit corrispondente, ma alcune librerie legacy sono disponibili solo nelle versioni a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="b36be-173">Most 32-bit libraries have a corresponding 64-bit version, but certain legacy libraries are available only in 32-bit versions.</span></span> <span data-ttu-id="b36be-174">Il codice che effettua chiamate a queste librerie non verrà collegato quando l'applicazione viene compilata per Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b36be-174">Code that calls into these libraries will not link when the application is built for 64-bit Windows.</span></span>

 

 






---
title: opzione/char
description: L'opzione/char consente di garantire che il compilatore MIDL e il compilatore C funzionino insieme correttamente per tutti i tipi char e Small.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- /char switch MIDL
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2254db9d0f4efcd003362e4126c5c295ca532b2f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718703"
---
# <a name="char-switch"></a><span data-ttu-id="dcef2-104">opzione/char</span><span class="sxs-lookup"><span data-stu-id="dcef2-104">/char switch</span></span>

<span data-ttu-id="dcef2-105">L'opzione **/char** consente di garantire che il compilatore MIDL e il compilatore C funzionino insieme correttamente per tutti i tipi [**char**](char-idl.md) e [**small**](small.md) .</span><span class="sxs-lookup"><span data-stu-id="dcef2-105">The **/char** switch helps to ensure that the MIDL compiler and C compiler operate together correctly for all [**char**](char-idl.md) and [**small**](small.md) types.</span></span>

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a><span data-ttu-id="dcef2-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="dcef2-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span data-ttu-id="dcef2-107"><span id="signed"></span><span id="SIGNED"></span>con segno \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="dcef2-107"><span id="signed"></span><span id="SIGNED"></span>\*\*\*\*signed\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="dcef2-108">Specifica che il tipo di compilatore C predefinito per [**char**](char-idl.md) è firmato.</span><span class="sxs-lookup"><span data-stu-id="dcef2-108">Specifies that the default C-compiler type for [**char**](char-idl.md) is signed.</span></span> <span data-ttu-id="dcef2-109">Tutte le occorrenze di **char** non associate a una specifica del segno vengono generate come carattere senza segno.</span><span class="sxs-lookup"><span data-stu-id="dcef2-109">All occurrences of **char** not accompanied by a sign specification are generated as unsigned char.</span></span>

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span data-ttu-id="dcef2-110"><span id="unsigned"></span><span id="UNSIGNED"></span>senza segno \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="dcef2-110"><span id="unsigned"></span><span id="UNSIGNED"></span>\*\*\*\*unsigned\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="dcef2-111">Specifica che il tipo di compilatore C predefinito per [**char**](char-idl.md) è senza segno.</span><span class="sxs-lookup"><span data-stu-id="dcef2-111">Specifies that the default C-compiler type for [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="dcef2-112">Tutti gli utilizzi di [**small**](small.md) non accompagnati da una specifica del segno vengono generati con segno di dimensioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="dcef2-112">All uses of [**small**](small.md) not accompanied by a sign specification are generated as signed small.</span></span>

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span data-ttu-id="dcef2-113"><span id="ascii7"></span><span id="ASCII7"></span>ascii7 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="dcef2-113"><span id="ascii7"></span><span id="ASCII7"></span>\*\*\*\*ascii7\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="dcef2-114">Specifica che tutti i valori [**char**](char-idl.md) devono essere passati nei file generati senza una parola chiave del segno specifica.</span><span class="sxs-lookup"><span data-stu-id="dcef2-114">Specifies that all [**char**](char-idl.md) values are to be passed into the generated files without a specific sign keyword.</span></span> <span data-ttu-id="dcef2-115">Tutti gli utilizzi di [**small**](small.md) non accompagnati da una specifica del segno vengono generati come **piccoli**.</span><span class="sxs-lookup"><span data-stu-id="dcef2-115">All uses of [**small**](small.md) not accompanied by a sign specification are generated as **small**.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcef2-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="dcef2-116">Remarks</span></span>

<span data-ttu-id="dcef2-117">Per definizione, il [**carattere**](char-idl.md) MIDL è senza segno.</span><span class="sxs-lookup"><span data-stu-id="dcef2-117">By definition, MIDL [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="dcef2-118">"Small" è definito in termini di **char** ( \# define Small Char) e MIDL [**small**](small.md) è firmato.</span><span class="sxs-lookup"><span data-stu-id="dcef2-118">"Small" is defined in terms of **char** (\#define small char), and MIDL [**small**](small.md) is signed.</span></span>

<span data-ttu-id="dcef2-119">L'opzione **/char** indica al compilatore MIDL di specificare dichiarazioni esplicite o non [**firmate**](unsigned.md) nei file generati quando la dichiarazione di firma del compilatore C è in conflitto con l'impostazione predefinita MIDL per quel tipo. [](signed.md)</span><span class="sxs-lookup"><span data-stu-id="dcef2-119">The **/char** switch directs the MIDL compiler to specify explicit [**signed**](signed.md) or [**unsigned**](unsigned.md) declarations in the generated files when the C-compiler sign declaration conflicts with the MIDL default for that type.</span></span>

<span data-ttu-id="dcef2-120">Tenere presente che il compilatore MIDL genera gli stub come codice sorgente C, che è necessario compilare come parte dei programmi client e server.</span><span class="sxs-lookup"><span data-stu-id="dcef2-120">Remember that the MIDL compiler generates the stubs as C source code, which you must compile as part of your client and server programs.</span></span> <span data-ttu-id="dcef2-121">Alcuni compilatori usano i dati [**char**](char-idl.md) con **segno** ovunque nel codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="dcef2-121">Some compilers use a **signed char** everywhere [**char**](char-idl.md) data is specified in the source code.</span></span> <span data-ttu-id="dcef2-122">Il codice sorgente dello stub che il compilatore MIDL genera considera tutti i dati **char** come **unsigned char**.</span><span class="sxs-lookup"><span data-stu-id="dcef2-122">The stub source code that the MIDL compiler generates treats all **char** data as **unsigned char**.</span></span> <span data-ttu-id="dcef2-123">Se il compilatore MIDL genera semplicemente tutti i dati **char** nel file IDL come dati **char** negli Stub, i compilatori che usano un **carattere signed** per i dati **char** potrebbero causare un conflitto nel codice sorgente dello stub.</span><span class="sxs-lookup"><span data-stu-id="dcef2-123">If the MIDL compiler simply generated all **char** data in the IDL file as **char** data in the stubs, compilers that use a **signed char** for **char** data would cause a conflict in the stub source code.</span></span>

<span data-ttu-id="dcef2-124">Lo scopo dell'opzione della riga di comando **/char** è risolvere questi potenziali conflitti.</span><span class="sxs-lookup"><span data-stu-id="dcef2-124">The purpose of the **/char** command line switch is to resolve these potential conflicts.</span></span> <span data-ttu-id="dcef2-125">Conserva tutti i dati specificati come [**caratteri**](char-idl.md) nel file IDL come **carattere senza segno** nel codice sorgente dello stub.</span><span class="sxs-lookup"><span data-stu-id="dcef2-125">It preserves all data specified as [**char**](char-idl.md) in the IDL file as **unsigned char** in the stub source code.</span></span> <span data-ttu-id="dcef2-126">Gestisce anche [**piccoli**](small.md) dati come firmati.</span><span class="sxs-lookup"><span data-stu-id="dcef2-126">It also maintains [**small**](small.md) data as signed.</span></span>

<span data-ttu-id="dcef2-127">Nella tabella seguente vengono riepilogati i tipi generati.</span><span class="sxs-lookup"><span data-stu-id="dcef2-127">The following table summarizes the generated types.</span></span>



| <span data-ttu-id="dcef2-128">MIDL/char-opzione</span><span class="sxs-lookup"><span data-stu-id="dcef2-128">midl /char option</span></span>       | <span data-ttu-id="dcef2-129">Tipo char generato</span><span class="sxs-lookup"><span data-stu-id="dcef2-129">Generated char type</span></span> | <span data-ttu-id="dcef2-130">Tipo piccolo generato</span><span class="sxs-lookup"><span data-stu-id="dcef2-130">Generated small type</span></span> |
|-------------------------|---------------------|----------------------|
| <span data-ttu-id="dcef2-131">**/char MIDL firmato**</span><span class="sxs-lookup"><span data-stu-id="dcef2-131">**midl /char signed**</span></span>   | <span data-ttu-id="dcef2-132">**unsigned char**</span><span class="sxs-lookup"><span data-stu-id="dcef2-132">**unsigned char**</span></span>   | <span data-ttu-id="dcef2-133">**small**</span><span class="sxs-lookup"><span data-stu-id="dcef2-133">**small**</span></span>            |
| <span data-ttu-id="dcef2-134">**MIDL/char senza segno**</span><span class="sxs-lookup"><span data-stu-id="dcef2-134">**midl /char unsigned**</span></span> | <span data-ttu-id="dcef2-135">**char**</span><span class="sxs-lookup"><span data-stu-id="dcef2-135">**char**</span></span>            | <span data-ttu-id="dcef2-136">**con segno piccolo**</span><span class="sxs-lookup"><span data-stu-id="dcef2-136">**signed small**</span></span>     |
| <span data-ttu-id="dcef2-137">**ascii7/char MIDL**</span><span class="sxs-lookup"><span data-stu-id="dcef2-137">**midl /char ascii7**</span></span>   | <span data-ttu-id="dcef2-138">**char**</span><span class="sxs-lookup"><span data-stu-id="dcef2-138">**char**</span></span>            | <span data-ttu-id="dcef2-139">**small**</span><span class="sxs-lookup"><span data-stu-id="dcef2-139">**small**</span></span>            |



 

<span data-ttu-id="dcef2-140">L'opzione **/char** signed indica che i tipi char e Small del compilatore C sono firmati.</span><span class="sxs-lookup"><span data-stu-id="dcef2-140">The **/char** signed option indicates that the C-compiler char and small types are signed.</span></span> <span data-ttu-id="dcef2-141">Per trovare la corrispondenza con il valore predefinito MIDL per **char**, il compilatore MIDL deve convertire tutti gli usi di **char** non accompagnati da una specifica di segno a un **carattere senza segno**.</span><span class="sxs-lookup"><span data-stu-id="dcef2-141">To match the MIDL default for **char**, the MIDL compiler must convert all uses of **char** not accompanied by a sign specification to **unsigned char**.</span></span> <span data-ttu-id="dcef2-142">Il tipo [**piccolo**](small.md) non viene modificato perché questa impostazione predefinita del compilatore C corrisponde al valore predefinito MIDL per **small**.</span><span class="sxs-lookup"><span data-stu-id="dcef2-142">The [**small**](small.md) type is not modified because this C-compiler default matches the MIDL default for **small**.</span></span>

<span data-ttu-id="dcef2-143">L'opzione unsigned **/char** indica che il tipo [**char**](char-idl.md) del compilatore C è senza segno.</span><span class="sxs-lookup"><span data-stu-id="dcef2-143">The **/char** unsigned option indicates that the C-compiler [**char**](char-idl.md) type is unsigned.</span></span> <span data-ttu-id="dcef2-144">Il compilatore MIDL converte tutti gli utilizzi di [**small**](small.md) non accompagnati da una specifica di **segno a** **small** con segno.</span><span class="sxs-lookup"><span data-stu-id="dcef2-144">The MIDL compiler converts all uses of [**small**](small.md) not accompanied by a sign specification to **signed** **small**.</span></span>

<span data-ttu-id="dcef2-145">L'opzione ascii7 indica che non viene aggiunta alcuna specifica di firma esplicita ai tipi [**char**](char-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="dcef2-145">The ascii7 option indicates that no explicit sign specification is added to [**char**](char-idl.md) types.</span></span> <span data-ttu-id="dcef2-146">Il tipo [**small**](small.md) viene generato come **small**.</span><span class="sxs-lookup"><span data-stu-id="dcef2-146">The type [**small**](small.md) is generated as **small**.</span></span>

<span data-ttu-id="dcef2-147">Per evitare confusione, è consigliabile utilizzare le specifiche esplicite del segno per i tipi [**char**](char-idl.md) e Small quando possibile nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="dcef2-147">To avoid confusion, you should use explicit sign specifications for [**char**](char-idl.md) and small types whenever possible in the IDL file.</span></span> <span data-ttu-id="dcef2-148">Si noti che l'uso di tipi **char** con firma esplicita nel file IDL non è supportato da DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="dcef2-148">Note that the use of explicitly signed **char** types in your IDL file is not supported by DCE IDL.</span></span> <span data-ttu-id="dcef2-149">Pertanto, questa funzionalità non è disponibile quando si esegue la compilazione con l'opzione MIDL [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="dcef2-149">Therefore, this feature is not available when you compile with the MIDL [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="dcef2-150">Per ulteriori informazioni relative a **/char**, vedere [**small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="dcef2-150">For more information related to **/char**, see [**small**](small.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dcef2-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="dcef2-151">Examples</span></span>

<span data-ttu-id="dcef2-152">**nome file. idl con firma MIDL/char**</span><span class="sxs-lookup"><span data-stu-id="dcef2-152">**midl /char signed filename.idl**</span></span>

<span data-ttu-id="dcef2-153">**MIDL/char unsigned filename. idl**</span><span class="sxs-lookup"><span data-stu-id="dcef2-153">**midl /char unsigned filename.idl**</span></span>

<span data-ttu-id="dcef2-154">**MIDL/char ascii7 nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="dcef2-154">**midl /char ascii7 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="dcef2-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcef2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcef2-156">**char**</span><span class="sxs-lookup"><span data-stu-id="dcef2-156">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="dcef2-157">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="dcef2-157">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="dcef2-158">**/osf**</span><span class="sxs-lookup"><span data-stu-id="dcef2-158">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="dcef2-159">**piccolo**</span><span class="sxs-lookup"><span data-stu-id="dcef2-159">**small**</span></span>](small.md)
</dt> </dl>

 

 





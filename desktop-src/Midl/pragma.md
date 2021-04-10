---
title: pragma (attributo)
description: La direttiva \ pragma MIDL \_ echo indica a MIDL di emettere la stringa specificata, senza virgolette, nel file di intestazione generato.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- attributo pragma MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f5e1c00c089bc8915adc2d9f3363305c677a96
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955879"
---
# <a name="pragma-attribute"></a><span data-ttu-id="7f71b-104">pragma (attributo)</span><span class="sxs-lookup"><span data-stu-id="7f71b-104">pragma attribute</span></span>

<span data-ttu-id="7f71b-105">La \# direttiva **pragma MIDL \_ echo** indica a MIDL di emettere la stringa specificata, senza virgolette, nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="7f71b-105">The \#**pragma midl\_echo** directive instructs MIDL to emit the specified string, without the quotation characters, into the generated header file.</span></span>

``` syntax
#pragma midl_echo("string")
#pragma token-sequence
#pragma pack (n)
#pragma pack ( [push] [, id] [, n} )
#pragma pack ( [pop] [, id] [, n} )
```

## <a name="parameters"></a><span data-ttu-id="7f71b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f71b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f71b-107">*string*</span><span class="sxs-lookup"><span data-stu-id="7f71b-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="7f71b-108">Specifica una stringa inserita nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="7f71b-108">Specifies a string that is inserted into the generated header file.</span></span> <span data-ttu-id="7f71b-109">Le virgolette vengono rimosse durante il processo di inserimento.</span><span class="sxs-lookup"><span data-stu-id="7f71b-109">The quotation marks are removed during the insertion process.</span></span>

</dd> <dt>

<span data-ttu-id="7f71b-110">*sequenza di token*</span><span class="sxs-lookup"><span data-stu-id="7f71b-110">*token-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="7f71b-111">Specifica una sequenza di token che vengono inseriti nel file di intestazione generato come parte di una direttiva **\# pragma** senza elaborazione da parte del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="7f71b-111">Specifies a sequence of tokens that are inserted into the generated header file as part of a **\#pragma** directive without processing by the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="7f71b-112">*n*</span><span class="sxs-lookup"><span data-stu-id="7f71b-112">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="7f71b-113">Specifica la dimensione corrente del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7f71b-113">Specifies the current pack size.</span></span> <span data-ttu-id="7f71b-114">Tra i valori validi sono compresi 1, 2, 4, 8 e 16.</span><span class="sxs-lookup"><span data-stu-id="7f71b-114">Valid values are 1, 2, 4, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="7f71b-115">*id*</span><span class="sxs-lookup"><span data-stu-id="7f71b-115">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="7f71b-116">Specifica l'identificatore utente.</span><span class="sxs-lookup"><span data-stu-id="7f71b-116">Specifies the user identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f71b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f71b-117">Remarks</span></span>

<span data-ttu-id="7f71b-118">Le direttive di pre-elaborazione del linguaggio c visualizzate nel file IDL vengono elaborate dal preprocessore del compilatore C.</span><span class="sxs-lookup"><span data-stu-id="7f71b-118">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="7f71b-119">Le direttive **\# define** nel file IDL sono disponibili durante la compilazione MIDL, anche se non al compilatore C.</span><span class="sxs-lookup"><span data-stu-id="7f71b-119">The **\#define** directives in the IDL file are available during MIDL compilation, although not to the C compiler.</span></span>

<span data-ttu-id="7f71b-120">Ad esempio, quando il preprocessore rileva la direttiva " \# define Windows 4", il preprocessore sostituisce tutte le occorrenze di "Windows" nel file IDL con "4".</span><span class="sxs-lookup"><span data-stu-id="7f71b-120">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="7f71b-121">Il simbolo "WINDOWS" non è disponibile in fase di compilazione C.</span><span class="sxs-lookup"><span data-stu-id="7f71b-121">The symbol "WINDOWS" is not available at C-compile time.</span></span>

<span data-ttu-id="7f71b-122">Per consentire alle definizioni di macro del preprocessore C di passare attraverso il compilatore MIDL al compilatore C, usare la direttiva **\# pragma MIDL \_ echo** o [**cpp \_ quot**](cpp-quote.md) .</span><span class="sxs-lookup"><span data-stu-id="7f71b-122">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or [**cpp\_quote**](cpp-quote.md) directive.</span></span> <span data-ttu-id="7f71b-123">Queste direttive indicano al compilatore MIDL di generare un file di intestazione contenente la stringa di parametro con le virgolette rimosse.</span><span class="sxs-lookup"><span data-stu-id="7f71b-123">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="7f71b-124">Le direttive di **\_ virgolette** Echo e cpp di **\# pragma MIDL \_** sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="7f71b-124">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="7f71b-125">La direttiva **\# pragma pack** viene usata dal compilatore MIDL per controllare la compressione delle strutture.</span><span class="sxs-lookup"><span data-stu-id="7f71b-125">The **\#pragma pack** directive is used by the MIDL compiler to control the packing of structures.</span></span> <span data-ttu-id="7f71b-126">Esegue l'override dell'opzione della riga di comando [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="7f71b-126">It overrides the [**/Zp**](-zp.md) command-line switch.</span></span> <span data-ttu-id="7f71b-127">L'opzione Pack (*n*) consente di impostare le dimensioni correnti del pacchetto su un valore specifico: 1, 2, 4, 8 o 16.</span><span class="sxs-lookup"><span data-stu-id="7f71b-127">The pack (*n*) option sets the current pack size to a specific value: 1, 2, 4, 8, or 16.</span></span> <span data-ttu-id="7f71b-128">Le opzioni Pack (push) e Pack (pop) presentano le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f71b-128">The pack (push) and pack (pop) options have the following characteristics:</span></span>

-   <span data-ttu-id="7f71b-129">Il compilatore mantiene uno stack di compressione.</span><span class="sxs-lookup"><span data-stu-id="7f71b-129">The compiler maintains a packing stack.</span></span> <span data-ttu-id="7f71b-130">Gli elementi dello stack di compressione includono una dimensione del pacchetto e un *ID* facoltativo. Lo stack è limitato solo dalla memoria disponibile con le dimensioni del pacchetto corrente nella parte superiore dello stack.</span><span class="sxs-lookup"><span data-stu-id="7f71b-130">The elements of the packing stack include a pack size and an optional *id*. The stack is limited only by available memory with the current pack size at the top of the stack.</span></span>
-   <span data-ttu-id="7f71b-131">Pack (push) determina la dimensione corrente del pacchetto inserita nello stack di compressione.</span><span class="sxs-lookup"><span data-stu-id="7f71b-131">Pack (push) results in the current pack size pushed onto the packing stack.</span></span> <span data-ttu-id="7f71b-132">Lo stack è limitato dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="7f71b-132">The stack is limited by available memory.</span></span>
-   <span data-ttu-id="7f71b-133">Pack (push,*n*) corrisponde a Pack (push) seguito da Pack (*n*).</span><span class="sxs-lookup"><span data-stu-id="7f71b-133">Pack (push,*n*) is the same as pack (push) followed by pack (*n*).</span></span>
-   <span data-ttu-id="7f71b-134">Pack (push, *ID*) inserisce anche l' *ID* nello stack di compressione insieme alle dimensioni del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7f71b-134">Pack (push, *id*) also pushes *id* onto the packing stack along with the pack size.</span></span>
-   <span data-ttu-id="7f71b-135">Pack (push, *ID*, *n*) corrisponde a Pack (push, *ID*) seguito da Pack (*n*).</span><span class="sxs-lookup"><span data-stu-id="7f71b-135">Pack (push, *id*, *n*) is the same as pack (push, *id*) followed by pack (*n*).</span></span>
-   <span data-ttu-id="7f71b-136">Pack (pop) genera lo stack di compressione.</span><span class="sxs-lookup"><span data-stu-id="7f71b-136">Pack (pop) results in popping the packing stack.</span></span> <span data-ttu-id="7f71b-137">I pop sbilanciati generano avvisi e impostano le dimensioni correnti del pacchetto sul valore della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="7f71b-137">Unbalanced pops cause warnings and set the current pack size to the command-line value.</span></span>
-   <span data-ttu-id="7f71b-138">Se si specifica Pack (pop, *ID*, *n*), *n* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="7f71b-138">If pack (pop, *id*, *n*) is specified, then *n* is ignored.</span></span>

<span data-ttu-id="7f71b-139">Il compilatore MIDL inserisce le stringhe specificate nell' [**\\ \_ offerta cpp**](cpp-quote.md) e le direttive **pragma** nel file di intestazione nella sequenza in cui sono specificate nel file IDL e in relazione ad altri componenti dell'interfaccia nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="7f71b-139">The MIDL compiler places the strings specified in the [**\\cpp\_quote**](cpp-quote.md) and **pragma** directives in the header file in the sequence in which they are specified in the IDL file and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="7f71b-140">Le stringhe dovrebbero in genere essere visualizzate nella sezione Interface-Body del file IDL dopo tutte le operazioni di [**importazione**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="7f71b-140">The strings should usually appear in the interface-body section of the IDL file after all [**import**](import.md) operations.</span></span>

<span data-ttu-id="7f71b-141">Il compilatore MIDL non tenta di elaborare direttive **\# pragma** che non iniziano con il prefisso "MIDL" \_ .</span><span class="sxs-lookup"><span data-stu-id="7f71b-141">The MIDL compiler does not attempt to process **\#pragma** directives that do not start with the prefix "midl\_."</span></span> <span data-ttu-id="7f71b-142">Altre direttive **\# pragma** nel file IDL vengono passate nel file di intestazione generato senza modifiche.</span><span class="sxs-lookup"><span data-stu-id="7f71b-142">Other **\#pragma** directives in the IDL file are passed into the generated header file without changes.</span></span>

## <a name="examples"></a><span data-ttu-id="7f71b-143">Esempi</span><span class="sxs-lookup"><span data-stu-id="7f71b-143">Examples</span></span>

``` syntax
/* IDL file */ 
#pragma midl_echo("#define UNICODE") 
cpp_quote("#define __DELAYED_PREPROCESSING__ 1") 
#pragma hdrstop 
#pragma check_pointer(on) 
 
/* generated header file */ 
#define UNICODE 
#define __DELAYED_PREPROCESSING__ 1 
#pragma hdrstop 
#pragma check_pointer(on)
```

## <a name="see-also"></a><span data-ttu-id="7f71b-144">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7f71b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f71b-145">**\_virgolette cpp**</span><span class="sxs-lookup"><span data-stu-id="7f71b-145">**cpp\_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="7f71b-146">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="7f71b-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7f71b-147">**importare**</span><span class="sxs-lookup"><span data-stu-id="7f71b-147">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="7f71b-148">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="7f71b-148">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 





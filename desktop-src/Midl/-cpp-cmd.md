---
title: /cpp_cmd opzione
description: L' \_ opzione cmd/cpp specifica il preprocessore usato dal compilatore MIDL per la pre-elaborazione dei file di input.
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /cpp_cmd switch MIDL
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718697"
---
# <a name="cpp_cmd-switch"></a><span data-ttu-id="72930-104">\_opzione cmd/cpp</span><span class="sxs-lookup"><span data-stu-id="72930-104">/cpp\_cmd switch</span></span>

<span data-ttu-id="72930-105">L' **opzione \_ cmd/cpp** specifica il preprocessore usato dal compilatore MIDL per la pre-elaborazione dei file di input.</span><span class="sxs-lookup"><span data-stu-id="72930-105">The **/cpp\_cmd** switch specifies the preprocessor that the MIDL compiler uses to preprocess input files.</span></span>

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a><span data-ttu-id="72930-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="72930-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="72930-107">*Binario per il \_ preprocessore C \_*</span><span class="sxs-lookup"><span data-stu-id="72930-107">*C\_preprocessor\_binary*</span></span> 
</dt> <dd>

<span data-ttu-id="72930-108">Specifica il comando che richiama il preprocessore.</span><span class="sxs-lookup"><span data-stu-id="72930-108">Specifies the command that invokes the preprocessor.</span></span> <span data-ttu-id="72930-109">Questo comando consente agli sviluppatori di eseguire l'override del preprocessore predefinito.</span><span class="sxs-lookup"><span data-stu-id="72930-109">This command allows developers to override the default preprocessor.</span></span> <span data-ttu-id="72930-110">Per impostazione predefinita, MIDL richiama il compilatore Microsoft C/C++ dall'ambiente di compilazione del computer di compilazione.</span><span class="sxs-lookup"><span data-stu-id="72930-110">By default, MIDL invokes the Microsoft C/C++ compiler from the build machine's build environment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72930-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="72930-111">Remarks</span></span>

<span data-ttu-id="72930-112">L' *argomento \_ \_ binario del preprocessore C* per l'opzione può specificare il percorso completo. il suffisso e le virgolette di exe sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="72930-112">The *C\_preprocessor\_binary* argument to the switch may specify the full path; the exe suffix and quotes are optional.</span></span> <span data-ttu-id="72930-113">In genere, gli sviluppatori usano l'opzione per scegliere una particolare versione del preprocessore di Microsoft C/C++ o equivalente nell'ambiente di compilazione.</span><span class="sxs-lookup"><span data-stu-id="72930-113">Typically, developers use the switch to choose a particular version of the Microsoft C/C++ preprocessor or equivalent in the build environment.</span></span> <span data-ttu-id="72930-114">In questo caso, non è necessario usare l'opzione [**/cpp \_ opt**](-cpp-opt.md) con **/cpp \_ cmd**.</span><span class="sxs-lookup"><span data-stu-id="72930-114">In this case, it is not necessary to use the [**/cpp\_opt**](-cpp-opt.md) switch with **/cpp\_cmd**.</span></span>

<span data-ttu-id="72930-115">Quando si usa un preprocessore non Microsoft, in particolare quando il preprocessore specificato non indirizza l'output a stdout, l'opzione del compilatore C che reindirizza l'output in stdout come parte dell'opzione [**\_ opt**](-cpp-opt.md) del compilatore MIDL/cpp deve essere specificata.</span><span class="sxs-lookup"><span data-stu-id="72930-115">When using a non-Microsoft preprocessor, especially when the specified preprocessor does not direct its output to stdout, the C compiler switch that redirects output to stdout as part of the MIDL compiler [**/cpp\_opt**](-cpp-opt.md) switch must be specified.</span></span> <span data-ttu-id="72930-116">Per informazioni dettagliate, vedere i [requisiti del preprocessore C per MIDL](c-preprocessor-requirements-for-midl.md)</span><span class="sxs-lookup"><span data-stu-id="72930-116">See [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for details</span></span>

<span data-ttu-id="72930-117">Il preprocessore viene richiamato da una stringa di comando costituita dalle informazioni fornite al compilatore MIDL dalle opzioni **/cpp \_ cmd**, [**/cpp \_ opt**](-cpp-opt.md), [**/d**](-d.md), [**/i**](-i.md)e [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="72930-117">The preprocessor is invoked by a command string that is formed from the information provided to the MIDL compiler by **/cpp\_cmd**, [**/cpp\_opt**](-cpp-opt.md), [**/D**](-d.md), [**/I**](-i.md), and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="72930-118">La tabella seguente riepiloga il modo in cui viene costruita la stringa di comando per ogni combinazione di opzioni **/cpp \_ cmd** e **/cpp \_ opz** .</span><span class="sxs-lookup"><span data-stu-id="72930-118">The following table summarizes how the command string is constructed for each combination of **/cpp\_cmd** and **/cpp\_opt** switches.</span></span>

<span data-ttu-id="72930-119">Quando non si specifica l'opzione **\_ cmd/cpp** , il compilatore MIDL richiama il compilatore Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="72930-119">When the **/cpp\_cmd** switch is not specified, the MIDL compiler invokes the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="72930-120">MIDL usa un file binario Cl.exe trovato nell'ambiente di compilazione.</span><span class="sxs-lookup"><span data-stu-id="72930-120">MIDL uses a Cl.exe binary found in the build environment.</span></span>

<span data-ttu-id="72930-121">Quando l' [**opzione \_ /cpp opt**](-cpp-opt.md) non è presente, il compilatore MIDL concatena la stringa specificata dall'opzione **\_ cmd/cpp** con le informazioni specificate dalle opzioni MIDL [**/i**](-i.md), [**/d**](-d.md) e [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="72930-121">When the [**/cpp\_opt**](-cpp-opt.md) switch is not present, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the information specified by the MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) options.</span></span> <span data-ttu-id="72930-122">La stringa/E viene inoltre concatenata alla stringa di chiamata del compilatore C per indicare che il compilatore C/C++ deve eseguire solo la pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="72930-122">The string /E is also concatenated to the C-compiler invocation string to indicate that the C/C++ compiler should perform preprocessing only.</span></span> <span data-ttu-id="72930-123">L'opzione [**/nologo**](-nologo.md) viene aggiunta per disattivare il banner del compilatore C/C++.</span><span class="sxs-lookup"><span data-stu-id="72930-123">The [**/nologo**](-nologo.md) switch is added to suppress the C/C++ compiler banner.</span></span> <span data-ttu-id="72930-124">Il compilatore MIDL usa la stringa concatenata per richiamare il preprocessore C per l'IDL di primo livello, nonché i file IDL importati e anche per eventuali file ACF corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="72930-124">The MIDL compiler uses the concatenated string to invoke the C preprocessor for top-level IDL as well as imported IDL files, and also for any present, corresponding ACF files.</span></span>

<span data-ttu-id="72930-125">Quando è presente l'opzione [**/cpp \_ opt**](-cpp-opt.md) , che dovrebbe essere un caso raro per le piattaforme a 32 bit e a 64 bit correnti, il compilatore MIDL concatena la stringa specificata dall'opzione **\_ cmd/cpp** con la stringa specificata dall'opzione **/cpp \_ opt** .</span><span class="sxs-lookup"><span data-stu-id="72930-125">When the [**/cpp\_opt**](-cpp-opt.md) switch is present, which should be a rare case for the current 32-bit and 64-bit platforms, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the string specified by the **/cpp\_opt** switch.</span></span> <span data-ttu-id="72930-126">Il compilatore MIDL usa la stringa concatenata per richiamare il binario del preprocessore indicato al posto del preprocessore predefinito.</span><span class="sxs-lookup"><span data-stu-id="72930-126">The MIDL compiler uses the concatenated string to invoke the indicated preprocessor binary in place of the default preprocessor.</span></span> <span data-ttu-id="72930-127">Quando è presente l'opzione **\_ opt/cpp** , né le opzioni del compilatore MIDL specificate dalle opzioni [**/I**](-i.md), [**/d**](-d.md)e [**/u**](-u.md) né l'opzione del compilatore C/e sono concatenate alla stringa.</span><span class="sxs-lookup"><span data-stu-id="72930-127">When the **/cpp\_opt** switch is present, neither the MIDL compiler options specified by the [**/I**](-i.md), [**/D**](-d.md), and [**/U**](-u.md) switches nor the C compiler switch /E is concatenated with the string.</span></span> <span data-ttu-id="72930-128">È necessario fornire l'opzione/E, o equivalente, come parte della stringa.</span><span class="sxs-lookup"><span data-stu-id="72930-128">You must supply the /E option, or equivalent, as part of the string.</span></span>



| <span data-ttu-id="72930-129">/cpp \_ cmd è presente?</span><span class="sxs-lookup"><span data-stu-id="72930-129">/cpp\_cmd present?</span></span> | <span data-ttu-id="72930-130">/cpp \_ opt presente?</span><span class="sxs-lookup"><span data-stu-id="72930-130">/cpp\_opt present?</span></span> | <span data-ttu-id="72930-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72930-131">Description</span></span>                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72930-132">No (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72930-132">No (default)</span></span>       | <span data-ttu-id="72930-133">No (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72930-133">No (default)</span></span>       | <span data-ttu-id="72930-134">Richiama il compilatore Microsoft C/C++ predefinito con le impostazioni ottenute dalle opzioni MIDL [**/i**](-i.md), [**/d**](-d.md) e [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="72930-134">Invokes the default Microsoft C/C++ compiler with settings obtained from MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="72930-135">Aggiunge le opzioni del preprocessore/E e [**/nologo**](-nologo.md).</span><span class="sxs-lookup"><span data-stu-id="72930-135">Adds the preprocessor switches /E and [**/nologo**](-nologo.md).</span></span> |
| <span data-ttu-id="72930-136">Sì</span><span class="sxs-lookup"><span data-stu-id="72930-136">Yes</span></span>                | <span data-ttu-id="72930-137">No</span><span class="sxs-lookup"><span data-stu-id="72930-137">No</span></span>                 | <span data-ttu-id="72930-138">Richiama il file binario del preprocessore indicato con le stesse opzioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="72930-138">Invokes the indicated preprocessor binary with the same switches as above.</span></span>                                                                                                                                        |
| <span data-ttu-id="72930-139">No</span><span class="sxs-lookup"><span data-stu-id="72930-139">No</span></span>                 | <span data-ttu-id="72930-140">Sì</span><span class="sxs-lookup"><span data-stu-id="72930-140">Yes</span></span>                | <span data-ttu-id="72930-141">Richiama il compilatore Microsoft C con le opzioni specificate.</span><span class="sxs-lookup"><span data-stu-id="72930-141">Invokes the Microsoft C compiler with specified options.</span></span> <span data-ttu-id="72930-142">Non usa le opzioni MIDL [**/i**](-i.md), [**/d**](-d.md), [**/u**](-u.md) .</span><span class="sxs-lookup"><span data-stu-id="72930-142">Does not use MIDL [**/I**](-i.md), [**/D**](-d.md), [**/U**](-u.md) options.</span></span> <span data-ttu-id="72930-143">È necessario specificare/E come parte di [**/cpp \_ opt**](-cpp-opt.md).</span><span class="sxs-lookup"><span data-stu-id="72930-143">You must supply /E as part of [**/cpp\_opt**](-cpp-opt.md).</span></span>             |
| <span data-ttu-id="72930-144">Sì</span><span class="sxs-lookup"><span data-stu-id="72930-144">Yes</span></span>                | <span data-ttu-id="72930-145">Sì</span><span class="sxs-lookup"><span data-stu-id="72930-145">Yes</span></span>                | <span data-ttu-id="72930-146">Richiama il file binario del preprocessore specificato solo con le opzioni specificate.</span><span class="sxs-lookup"><span data-stu-id="72930-146">Invokes the specified preprocessor binary with specified options only.</span></span> <span data-ttu-id="72930-147">È necessario utilizzare le virgolette.</span><span class="sxs-lookup"><span data-stu-id="72930-147">You must use quotes.</span></span>                                                                                                                       |



 

## <a name="examples"></a><span data-ttu-id="72930-148">Esempio</span><span class="sxs-lookup"><span data-stu-id="72930-148">Examples</span></span>

<span data-ttu-id="72930-149">**MIDL/cpp \_ cmd d: \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC: \\ Inc nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="72930-149">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="72930-150">**MIDL/cpp \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="72930-150">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="72930-151">**MIDL/cpp \_ opz "/E/DFLAG = true/IC: \\ Inc" nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="72930-151">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="72930-152">**MIDL/cpp \_ cmd "CL"/cpp \_ opz "/e/DFLAG = true/IC: \\ Inc" nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="72930-152">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="72930-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72930-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72930-154">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="72930-154">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="72930-155">**/cpp \_ opt**</span><span class="sxs-lookup"><span data-stu-id="72930-155">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="72930-156">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="72930-156">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="72930-157">**\_cpp/No**</span><span class="sxs-lookup"><span data-stu-id="72930-157">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="72930-158">C-requisiti per il preprocessore MIDL</span><span class="sxs-lookup"><span data-stu-id="72930-158">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 





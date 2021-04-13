---
title: /cpp_opt opzione
description: L' \_ opzione/cpp opz specifica le opzioni da passare al preprocessore C/C++.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /cpp_opt switch MIDL
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e352a89ddadfc0a92e33e964afb5f0d9e9df6e
ms.sourcegitcommit: 97d62bfd3213d9c4ce46c3cd2b1177caf720681a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104399997"
---
# <a name="cpp_opt-switch"></a><span data-ttu-id="c0197-104">/cpp \_ opz switch</span><span class="sxs-lookup"><span data-stu-id="c0197-104">/cpp\_opt switch</span></span>

<span data-ttu-id="c0197-105">L'opzione **/cpp \_ opz** specifica le opzioni da passare al preprocessore C/C++.</span><span class="sxs-lookup"><span data-stu-id="c0197-105">The **/cpp\_opt** switch specifies options to pass to the C/C++ preprocessor.</span></span>

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a><span data-ttu-id="c0197-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="c0197-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="c0197-107">*C ( \_ opzione del preprocessore) \_*</span><span class="sxs-lookup"><span data-stu-id="c0197-107">*C\_preprocessor\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="c0197-108">Specifica l'opzione della riga di comando associata al preprocessore richiamato.</span><span class="sxs-lookup"><span data-stu-id="c0197-108">Specifies command-line option associated with the invoked preprocessor.</span></span> 

<span data-ttu-id="c0197-109">**Nota**: per i preprocessori di Microsoft C/C++, è necessario specificare l'opzione `/E` come parte della stringa di *\_ \_ opzione del preprocessore c* .</span><span class="sxs-lookup"><span data-stu-id="c0197-109">**Note**: For the Microsoft C/C++ preprocessors you must supply the `/E` switch as part of the *C\_preprocessor\_option* string.</span></span> 

<span data-ttu-id="c0197-110">Le virgolette sono obbligatorie quando viene usata più di un'opzione e per gli spazi.</span><span class="sxs-lookup"><span data-stu-id="c0197-110">Quotes are required when more than one option is used, and for spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0197-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0197-111">Remarks</span></span>

<span data-ttu-id="c0197-112">Non utilizzare questa opzione a meno che non esista un motivo specifico per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="c0197-112">Do not use this switch unless there is a specific reason for doing so.</span></span> <span data-ttu-id="c0197-113">Per informazioni importanti sulla pre-elaborazione, vedere [requisiti per il preprocessore per MIDL](c-preprocessor-requirements-for-midl.md) .</span><span class="sxs-lookup"><span data-stu-id="c0197-113">Consult [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for important information regarding preprocessing.</span></span>

<span data-ttu-id="c0197-114">È possibile usare l'opzione **/cpp \_ opt** con o senza l' [**opzione \_ cmd di/cpp**](-cpp-cmd.md) .</span><span class="sxs-lookup"><span data-stu-id="c0197-114">The **/cpp\_opt** switch can be used with or without the [**/cpp\_cmd**](-cpp-cmd.md) switch.</span></span> <span data-ttu-id="c0197-115">Per informazioni dettagliate sul modo in cui la riga di comando del preprocessore viene costruita in entrambi i casi, vedere **/cpp \_ cmd** .</span><span class="sxs-lookup"><span data-stu-id="c0197-115">Consult **/cpp\_cmd** for details of how the preprocessor command line is constructed in either case.</span></span>

<span data-ttu-id="c0197-116">L'opzione **/cpp \_ opt** , se specificata, deve sempre includere per `/E` funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="c0197-116">The **/cpp\_opt** switch, if specified, must always include `/E` in order to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="c0197-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="c0197-117">Examples</span></span>

<span data-ttu-id="c0197-118">**MIDL/cpp \_ cmd d: \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC: \\ Inc nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="c0197-118">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="c0197-119">**MIDL/cpp \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="c0197-119">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="c0197-120">**MIDL/cpp \_ opz "/E/DFLAG = true/IC: \\ Inc" nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="c0197-120">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="c0197-121">**MIDL/cpp \_ cmd "CL"/cpp \_ opz "/e/DFLAG = true/IC: \\ Inc" nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="c0197-121">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c0197-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0197-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0197-123">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="c0197-123">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="c0197-124">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="c0197-124">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="c0197-125">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="c0197-125">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="c0197-126">**\_cpp/No**</span><span class="sxs-lookup"><span data-stu-id="c0197-126">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="c0197-127">C-requisiti per il preprocessore MIDL</span><span class="sxs-lookup"><span data-stu-id="c0197-127">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 





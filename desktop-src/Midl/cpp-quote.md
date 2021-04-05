---
title: cpp_quote (attributo)
description: La \_ parola chiave delle virgolette cpp indica a MIDL di emettere la stringa specificata, senza virgolette, nel file di intestazione generato.
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- attributo cpp_quote MIDL
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045862"
---
# <a name="cpp_quote-attribute"></a><span data-ttu-id="9255d-104">\_attributo di virgolette cpp</span><span class="sxs-lookup"><span data-stu-id="9255d-104">cpp\_quote attribute</span></span>

<span data-ttu-id="9255d-105">La parola chiave delle **\_ virgolette cpp** indica a MIDL di emettere la stringa specificata, senza virgolette, nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="9255d-105">The **cpp\_quote** keyword instructs MIDL to emit the specified string, without the quote characters, into the generated header file.</span></span>

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a><span data-ttu-id="9255d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9255d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9255d-107">*string*</span><span class="sxs-lookup"><span data-stu-id="9255d-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="9255d-108">Specifica una stringa racchiusa tra virgolette emessa nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="9255d-108">Specifies a quoted string that is emitted in the generated header file.</span></span> <span data-ttu-id="9255d-109">La stringa deve essere racchiusa tra virgolette per impedire l'espansione da parte del preprocessore C.</span><span class="sxs-lookup"><span data-stu-id="9255d-109">The string must be quoted to prevent expansion by the C preprocessor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9255d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9255d-110">Remarks</span></span>

<span data-ttu-id="9255d-111">Le direttive di pre-elaborazione del linguaggio c visualizzate nel file IDL vengono elaborate dal preprocessore del compilatore C.</span><span class="sxs-lookup"><span data-stu-id="9255d-111">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="9255d-112">Le direttive **\# define** nel file IDL sono disponibili durante la compilazione MIDL, ma non sono disponibili per il compilatore C.</span><span class="sxs-lookup"><span data-stu-id="9255d-112">The **\#define** directives in the IDL file are available during MIDL compilation but are not available to the C compiler.</span></span>

<span data-ttu-id="9255d-113">Ad esempio, quando il preprocessore rileva la direttiva " \# define Windows 4", il preprocessore sostituisce tutte le occorrenze di "Windows" nel file IDL con "4".</span><span class="sxs-lookup"><span data-stu-id="9255d-113">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="9255d-114">Il simbolo "WINDOWS" non è disponibile durante la compilazione in linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="9255d-114">The symbol "WINDOWS" is not available during C-language compilation.</span></span>

<span data-ttu-id="9255d-115">Per consentire alle definizioni di macro del preprocessore C di passare attraverso il compilatore MIDL al compilatore C, usare la direttiva **\# pragma MIDL \_ echo** o **cpp \_ quot** .</span><span class="sxs-lookup"><span data-stu-id="9255d-115">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or **cpp\_quote** directive.</span></span> <span data-ttu-id="9255d-116">Queste direttive indicano al compilatore MIDL di generare un file di intestazione contenente la stringa di parametro con le virgolette rimosse.</span><span class="sxs-lookup"><span data-stu-id="9255d-116">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="9255d-117">Le direttive di **\_ virgolette** Echo e cpp di **\# pragma MIDL \_** sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="9255d-117">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="9255d-118">Il compilatore MIDL inserisce le stringhe specificate nell' **\_ offerta cpp** e le direttive [**pragma**](pragma.md) nel file di intestazione nella sequenza in cui sono specificate nel file IDL e in relazione ad altri componenti dell'interfaccia nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="9255d-118">The MIDL compiler places the strings specified in the **cpp\_quote** and [**pragma**](pragma.md) directives into the header file in the sequence in which they are specified in the IDL file, and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="9255d-119">Le stringhe dovrebbero in genere essere visualizzate nella sezione corpo dell'interfaccia del file IDL dopo tutte le operazioni di [**importazione**](import.md) .</span><span class="sxs-lookup"><span data-stu-id="9255d-119">The strings should usually appear in the IDL file interface body section after all [**import**](import.md) operations.</span></span>

## <a name="examples"></a><span data-ttu-id="9255d-120">Esempi</span><span class="sxs-lookup"><span data-stu-id="9255d-120">Examples</span></span>

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a><span data-ttu-id="9255d-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9255d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9255d-122">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="9255d-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="9255d-123">**importare**</span><span class="sxs-lookup"><span data-stu-id="9255d-123">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="9255d-124">**pragma**</span><span class="sxs-lookup"><span data-stu-id="9255d-124">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 





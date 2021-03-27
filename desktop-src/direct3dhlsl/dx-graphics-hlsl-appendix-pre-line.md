---
title: " line (direttiva)"
description: Direttiva per il preprocessore che imposta il numero di riga e il nome file archiviati internamente del compilatore sui valori specificati.
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- HLSL (direttiva riga)
topic_type:
- apiref
api_name:
- line Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0932138ce5aec85ad3d3e7058db0c2a93e131181
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397666"
---
# <a name="line-directive"></a><span data-ttu-id="42ae0-104">\#line (direttiva)</span><span class="sxs-lookup"><span data-stu-id="42ae0-104">\#line Directive</span></span>

<span data-ttu-id="42ae0-105">Direttiva per il preprocessore che imposta il numero di riga e il nome file archiviati internamente del compilatore sui valori specificati.</span><span class="sxs-lookup"><span data-stu-id="42ae0-105">Preprocessor directive that sets the compiler's internally-stored line number and filename to the specified values.</span></span>



| <span data-ttu-id="42ae0-106">\#riga *lineNumber* "*nomefile*"</span><span class="sxs-lookup"><span data-stu-id="42ae0-106">\#line *lineNumber* "*filename*"</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="42ae0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="42ae0-107">Parameters</span></span>



| <span data-ttu-id="42ae0-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="42ae0-108">Item</span></span>                                                                                                                              | <span data-ttu-id="42ae0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42ae0-109">Description</span></span>                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42ae0-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*</span><span class="sxs-lookup"><span data-stu-id="42ae0-110"><span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*</span></span><br/>                    | <span data-ttu-id="42ae0-111">Numero di riga da impostare.</span><span class="sxs-lookup"><span data-stu-id="42ae0-111">Line number to set.</span></span> <span data-ttu-id="42ae0-112">Può trattarsi di qualsiasi costante di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="42ae0-112">This can be any integer constant.</span></span> <span data-ttu-id="42ae0-113">È possibile eseguire la sostituzione delle macro sui token di pre-elaborazione, purché il risultato restituisca la sintassi corretta.</span><span class="sxs-lookup"><span data-stu-id="42ae0-113">Macro replacement can be performed on the preprocessing tokens, as long as the result evaluates to the correct syntax.</span></span> <br/>                     |
| <span data-ttu-id="42ae0-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*nome file* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="42ae0-114"><span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*filename* \[optional\]</span></span> <br/> | <span data-ttu-id="42ae0-115">Nome file da impostare.</span><span class="sxs-lookup"><span data-stu-id="42ae0-115">Filename to set.</span></span> <span data-ttu-id="42ae0-116">Il nome file può essere costituito da qualsiasi combinazione di caratteri e deve essere racchiuso tra virgolette doppie ("").</span><span class="sxs-lookup"><span data-stu-id="42ae0-116">The filename can be any combination of characters, and must be enclosed in double quotation marks (" ").</span></span> <span data-ttu-id="42ae0-117">Se questo parametro viene omesso, il nome del file precedente rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="42ae0-117">If this parameter is omitted, the previous filename remains unchanged.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="42ae0-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="42ae0-118">Remarks</span></span>

<span data-ttu-id="42ae0-119">Il compilatore usa il numero di riga e il nome del file per fare riferimento agli errori rilevati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="42ae0-119">The compiler uses the line number and filename to refer to errors that it finds during compilation.</span></span> <span data-ttu-id="42ae0-120">Il numero di riga in genere si riferisce alla linea di input corrente, mentre il nome del file fa riferimento al file di input corrente.</span><span class="sxs-lookup"><span data-stu-id="42ae0-120">The line number usually refers to the current input line, and the filename refers to the current input file.</span></span> <span data-ttu-id="42ae0-121">Il numero di riga viene incrementato dopo l'elaborazione di ogni riga.</span><span class="sxs-lookup"><span data-stu-id="42ae0-121">The line number is incremented after each line is processed.</span></span> <span data-ttu-id="42ae0-122">Se si modifica il numero di riga e il nome del file, il compilatore ignora i valori precedenti e continua l'elaborazione con i nuovi valori.</span><span class="sxs-lookup"><span data-stu-id="42ae0-122">If you change the line number and filename, the compiler ignores the previous values and continues processing with the new values.</span></span> <span data-ttu-id="42ae0-123">La \# direttiva line viene in genere utilizzata dai generatori di programma per fare in modo che i messaggi di errore facciano riferimento al file di origine originale anziché al programma generato.</span><span class="sxs-lookup"><span data-stu-id="42ae0-123">The \#line directive is typically used by program generators to cause error messages to refer to the original source file instead of to the generated program.</span></span>

<span data-ttu-id="42ae0-124">Il convertitore usa il numero di riga e il nome file per determinare i valori del \_ \_ file \_ \_ e della \_ \_ riga \_ \_ delle macro predefinite.</span><span class="sxs-lookup"><span data-stu-id="42ae0-124">The translator uses the line number and filename to determine the values of the predefined macros \_\_FILE\_\_ and \_\_LINE\_\_.</span></span> <span data-ttu-id="42ae0-125">È possibile utilizzare queste macro per inserire messaggi di errore autodescrittivi nel testo del programma.</span><span class="sxs-lookup"><span data-stu-id="42ae0-125">You can use these macros to insert self-descriptive error messages into the program text.</span></span> <span data-ttu-id="42ae0-126">La \_ \_ macro file si \_ \_ espande in una stringa il cui contenuto è il nome file, racchiuso tra virgolette doppie ("").</span><span class="sxs-lookup"><span data-stu-id="42ae0-126">The \_\_FILE\_\_ macro expands to a string whose contents are the filename, surrounded by double quotation marks (" ").</span></span>

## <a name="examples"></a><span data-ttu-id="42ae0-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="42ae0-127">Examples</span></span>

<span data-ttu-id="42ae0-128">Nell'esempio seguente il numero di riga viene impostato su 151 e il nome del file viene impostato su "copy. c".</span><span class="sxs-lookup"><span data-stu-id="42ae0-128">The following example sets the line number to 151 and the filename to "copy.c".</span></span>


```
#line 151 "copy.c"
```



<span data-ttu-id="42ae0-129">Nell'esempio seguente, la macro ASSERT usa la riga e il file delle macro predefinite \_ \_ \_ \_ \_ \_ \_ \_ per stampare un messaggio di errore relativo al file di origine se l'asserzione specificata non è true.</span><span class="sxs-lookup"><span data-stu-id="42ae0-129">In the following example, the macro ASSERT uses the predefined macros \_\_LINE\_\_ and \_\_FILE\_\_ to print an error message about the source file if the specified assertion is not true.</span></span>


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a><span data-ttu-id="42ae0-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42ae0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ae0-131">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="42ae0-131">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 






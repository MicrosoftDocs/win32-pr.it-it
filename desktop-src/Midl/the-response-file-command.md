---
title: Comando del file di risposta
description: Un file di risposta è un file di testo contenente una o più opzioni della riga di comando del compilatore MIDL.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- riferimento alla riga di comando MIDL , comando del file di risposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cf4d07ce8465239874ff666537646da2c4c564
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387667"
---
# <a name="the-response-file-command"></a><span data-ttu-id="4ca68-104">Comando del file di risposta</span><span class="sxs-lookup"><span data-stu-id="4ca68-104">The Response File Command</span></span>

<span data-ttu-id="4ca68-105">Un file di risposta è un file di testo contenente una o più opzioni della riga di comando del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="4ca68-105">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="4ca68-106">A differenza di una riga di comando, un file di risposta consente più righe di opzioni e nomi di file.</span><span class="sxs-lookup"><span data-stu-id="4ca68-106">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="4ca68-107">Ciò può essere utile a causa di limitazioni dell'ambiente di compilazione o per praticità del processo di compilazione.</span><span class="sxs-lookup"><span data-stu-id="4ca68-107">This may be useful due to limitations of your build environment, or as a convenience for your build process.</span></span>

## <a name="switch-options"></a><span data-ttu-id="4ca68-108">Opzioni di cambio</span><span class="sxs-lookup"><span data-stu-id="4ca68-108">Switch Options</span></span>

``` syntax
midl @response_file
```

<dl> <dt>

<span data-ttu-id="4ca68-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*file \_ di risposta*</span><span class="sxs-lookup"><span data-stu-id="4ca68-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*response\_file*</span></span>
</dt> <dd>

<span data-ttu-id="4ca68-110">Specifica il nome di un file di risposta.</span><span class="sxs-lookup"><span data-stu-id="4ca68-110">Specifies the name of a response file.</span></span> <span data-ttu-id="4ca68-111">Il nome del file di risposta deve seguire immediatamente il carattere @.</span><span class="sxs-lookup"><span data-stu-id="4ca68-111">The response file name must immediately follow the @ character.</span></span> <span data-ttu-id="4ca68-112">Non sono consentiti spazi vuoti tra il carattere @ e il nome del file di risposta.</span><span class="sxs-lookup"><span data-stu-id="4ca68-112">No white space is allowed between the @ character and the response file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ca68-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ca68-113">Remarks</span></span>

<span data-ttu-id="4ca68-114">In alternativa all'inserimento di tutte le opzioni associate a un'opzione nella riga di comando, il compilatore MIDL accetta i file di risposta che contengono opzioni e argomenti.</span><span class="sxs-lookup"><span data-stu-id="4ca68-114">As an alternative to placing all options associated with a switch on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="4ca68-115">Le opzioni in un file di risposta vengono interpretate come se fossero presenti in tale percorso nella riga di comando MIDL.</span><span class="sxs-lookup"><span data-stu-id="4ca68-115">Options in a response file are interpreted as if they are present in that location in the MIDL command line.</span></span>

<span data-ttu-id="4ca68-116">Ogni argomento in un file di risposta deve iniziare e terminare sulla stessa riga.</span><span class="sxs-lookup"><span data-stu-id="4ca68-116">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="4ca68-117">Non è possibile usare il carattere barra rovesciata ( \\ ) per concatenare le righe.</span><span class="sxs-lookup"><span data-stu-id="4ca68-117">The backslash character (\\) cannot be used to concatenate lines.</span></span> <span data-ttu-id="4ca68-118">Quando fa parte di una stringa tra virgolette nel file di risposta, il carattere barra rovesciata può essere usato solo prima di un'altra barra rovesciata o prima di un carattere virgolette doppie (").</span><span class="sxs-lookup"><span data-stu-id="4ca68-118">When it is part of a quoted string in the response file, the backslash character can only be used before another backslash or before a double quotation mark character (").</span></span> <span data-ttu-id="4ca68-119">Quando non fa parte di una stringa tra virgolette, il carattere barra rovesciata può essere usato solo prima di un carattere virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="4ca68-119">When it is not part of a quoted string, the backslash character can only be used before a double quotation mark character.</span></span>

<span data-ttu-id="4ca68-120">MIDL supporta argomenti della riga di comando che includono uno o più file di risposta combinati con altre opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4ca68-120">MIDL supports command-line arguments that include one or more response files combined with other command-line switches.</span></span>

<span data-ttu-id="4ca68-121">Il compilatore MIDL non supporta i file di risposta annidati.</span><span class="sxs-lookup"><span data-stu-id="4ca68-121">The MIDL compiler does not support nested response files.</span></span>

## <a name="examples"></a><span data-ttu-id="4ca68-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="4ca68-122">Examples</span></span>

<span data-ttu-id="4ca68-123">**Midl @midl.rsp**</span><span class="sxs-lookup"><span data-stu-id="4ca68-123">**midl @midl.rsp**</span></span>

<span data-ttu-id="4ca68-124">**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**</span><span class="sxs-lookup"><span data-stu-id="4ca68-124">**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ca68-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ca68-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ca68-126">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="4ca68-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





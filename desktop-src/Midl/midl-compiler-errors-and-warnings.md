---
title: Errori e avvisi del compilatore MIDL
description: Quando si usa il compilatore MIDL, errori e avvisi possono essere causati da un uso non corretto delle opzioni della riga di comando o dal contenuto dei file IDL e ACF.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Microsoft Interface Definition Language MIDL, riferimento
- MIDL compilatore MIDL, errori
- MIDL del compilatore, errori
- errori MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae531528f83f3731b4449c7aba012f3228edd9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855193"
---
# <a name="midl-compiler-errors-and-warnings"></a><span data-ttu-id="da299-107">Errori e avvisi del compilatore MIDL</span><span class="sxs-lookup"><span data-stu-id="da299-107">MIDL Compiler Errors and Warnings</span></span>

<span data-ttu-id="da299-108">Quando si usa il compilatore MIDL, errori e avvisi possono essere causati da un uso non corretto delle opzioni della riga di comando o dal contenuto dei file IDL e ACF.</span><span class="sxs-lookup"><span data-stu-id="da299-108">When using the MIDL compiler, errors and warnings can be caused by improper use of the command-line switches or by the content of the IDL and ACF files.</span></span> <span data-ttu-id="da299-109">Se l'errore è dovuto all'immissione non corretta delle opzioni della riga di comando, un messaggio di errore o di avviso può specificare il nome di una o più opzioni della modalità del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="da299-109">If the error is due to improperly entering the command-line switches, an error or warning message may specify the name of one or more MIDL compiler mode switches.</span></span> <span data-ttu-id="da299-110">Ad esempio, è possibile includere determinati attributi ACF in un file IDL quando si usa l'opzione **di \_ configurazione** di/app, ma il file IDL genererà un errore se si compila senza usare l'opzione di **\_ configurazione dell'app** /.</span><span class="sxs-lookup"><span data-stu-id="da299-110">For example, you can include certain ACF attributes in an IDL file when you use the /**app\_config** switch, but that IDL file will generate an error if you compile without using the /**app\_config** switch.</span></span>

<span data-ttu-id="da299-111">Gli errori nei file IDL e ACF rientrano in due categorie: errori rilevati dal preprocessore ed errori riconosciuti dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="da299-111">Errors in the IDL and ACF files fall into two categories: errors caught by the preprocessor and errors recognized by the compiler.</span></span> <span data-ttu-id="da299-112">Questa sezione elenca i messaggi di errore del compilatore e del preprocessore MIDL.</span><span class="sxs-lookup"><span data-stu-id="da299-112">This section lists the MIDL preprocessor and compiler error messages.</span></span> <span data-ttu-id="da299-113">Vengono inoltre descritti i formati e le cause.</span><span class="sxs-lookup"><span data-stu-id="da299-113">It also describes their formats and causes.</span></span>

-   [<span data-ttu-id="da299-114">Formati di messaggio di errore e di avviso</span><span class="sxs-lookup"><span data-stu-id="da299-114">Error and Warning Message Formats</span></span>](error-and-warning-message-formats.md)
-   [<span data-ttu-id="da299-115">Errori del preprocessore</span><span class="sxs-lookup"><span data-stu-id="da299-115">Preprocessor Errors</span></span>](preprocessor-errors.md)
-   [<span data-ttu-id="da299-116">Errori del compilatore</span><span class="sxs-lookup"><span data-stu-id="da299-116">Compiler Errors</span></span>](compiler-errors.md)

 

 





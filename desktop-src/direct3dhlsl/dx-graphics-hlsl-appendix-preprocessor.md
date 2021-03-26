---
title: Direttive per il preprocessore (HLSL)
description: Le direttive per il preprocessore, ad esempio \ define e \ ifdef, vengono in genere utilizzate per rendere i programmi di origine facili da modificare e facili da compilare in ambienti di esecuzione diversi.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f2d9e51926d2a1b7bf374653becec4fe3de3daa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739231"
---
# <a name="preprocessor-directives-hlsl"></a><span data-ttu-id="b4988-103">Direttive per il preprocessore (HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4988-103">Preprocessor Directives (HLSL)</span></span>

<span data-ttu-id="b4988-104">Le direttive per il preprocessore, ad esempio [ \# define](dx-graphics-hlsl-appendix-pre-define.md) e [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), vengono in genere utilizzate per rendere i programmi di origine facili da modificare e facili da compilare in ambienti di esecuzione diversi.</span><span class="sxs-lookup"><span data-stu-id="b4988-104">Preprocessor directives, such as [\#define](dx-graphics-hlsl-appendix-pre-define.md) and [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), are typically used to make source programs easy to change and easy to compile in different execution environments.</span></span> <span data-ttu-id="b4988-105">Le direttive nel file di origine indicano al preprocessore di eseguire azioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="b4988-105">Directives in the source file tell the preprocessor to perform specific actions.</span></span> <span data-ttu-id="b4988-106">Ad esempio, il preprocessore può sostituire i token nel testo, inserire il contenuto di altri file nel file di origine o eliminare la compilazione di parte del file rimuovendo sezioni di testo.</span><span class="sxs-lookup"><span data-stu-id="b4988-106">For example, the preprocessor can replace tokens in the text, insert the contents of other files into the source file, or suppress compilation of part of the file by removing sections of text.</span></span> <span data-ttu-id="b4988-107">Le righe del preprocessore vengono riconosciute ed eseguite prima dell'espansione di una macro.</span><span class="sxs-lookup"><span data-stu-id="b4988-107">Preprocessor lines are recognized and carried out before macro expansion.</span></span> <span data-ttu-id="b4988-108">Pertanto, se una macro si espande in modo da risultare simile a un comando del preprocessore, tale comando non sarà riconosciuto dal preprocessore.</span><span class="sxs-lookup"><span data-stu-id="b4988-108">Therefore, if a macro expands into something that looks like a preprocessor command, that command is not recognized by the preprocessor.</span></span>

<span data-ttu-id="b4988-109">Le istruzioni del preprocessore utilizzano lo stesso set di caratteri delle istruzioni del file di origine, con l'eccezione che le sequenze di escape non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="b4988-109">Preprocessor statements use the same character set as source file statements, with the exception that escape sequences are not supported.</span></span> <span data-ttu-id="b4988-110">Il set di caratteri utilizzati nelle istruzioni del preprocessore equivale al set di caratteri di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b4988-110">The character set used in preprocessor statements is the same as the execution character set.</span></span> <span data-ttu-id="b4988-111">Il preprocessore riconosce anche i valori di carattere negativi.</span><span class="sxs-lookup"><span data-stu-id="b4988-111">The preprocessor also recognizes negative character values.</span></span>

<span data-ttu-id="b4988-112">Il preprocessore HLSL riconosce le direttive seguenti:</span><span class="sxs-lookup"><span data-stu-id="b4988-112">The HLSL preprocessor recognizes the following directives:</span></span>

-   [<span data-ttu-id="b4988-113">\#definire</span><span class="sxs-lookup"><span data-stu-id="b4988-113">\#define</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
-   [<span data-ttu-id="b4988-114">\#elif</span><span class="sxs-lookup"><span data-stu-id="b4988-114">\#elif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="b4988-115">\#else</span><span class="sxs-lookup"><span data-stu-id="b4988-115">\#else</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="b4988-116">\#endif</span><span class="sxs-lookup"><span data-stu-id="b4988-116">\#endif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="b4988-117">\#errore</span><span class="sxs-lookup"><span data-stu-id="b4988-117">\#error</span></span>](dx-graphics-hlsl-appendix-pre-error.md)
-   [<span data-ttu-id="b4988-118">\#if</span><span class="sxs-lookup"><span data-stu-id="b4988-118">\#if</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="b4988-119">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="b4988-119">\#ifdef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="b4988-120">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="b4988-120">\#ifndef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="b4988-121">\#includere</span><span class="sxs-lookup"><span data-stu-id="b4988-121">\#include</span></span>](dx-graphics-hlsl-appendix-pre-include.md)
-   [<span data-ttu-id="b4988-122">\#linea</span><span class="sxs-lookup"><span data-stu-id="b4988-122">\#line</span></span>](dx-graphics-hlsl-appendix-pre-line.md)
-   [<span data-ttu-id="b4988-123">\#pragma</span><span class="sxs-lookup"><span data-stu-id="b4988-123">\#pragma</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [<span data-ttu-id="b4988-124">\#undef</span><span class="sxs-lookup"><span data-stu-id="b4988-124">\#undef</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)

<span data-ttu-id="b4988-125">Il simbolo di cancelletto ( \# ) deve essere il primo carattere di spazio non vuoto nella riga contenente la direttiva; gli spazi vuoti possono essere visualizzati tra il simbolo di cancelletto e la prima lettera della direttiva.</span><span class="sxs-lookup"><span data-stu-id="b4988-125">The number sign (\#) must be the first nonwhite-space character on the line containing the directive; white-space characters can appear between the number sign and the first letter of the directive.</span></span> <span data-ttu-id="b4988-126">Alcune direttive includono argomenti o valori.</span><span class="sxs-lookup"><span data-stu-id="b4988-126">Some directives include arguments or values.</span></span> <span data-ttu-id="b4988-127">Qualsiasi testo che segue una direttiva (eccetto un argomento o un valore che fa parte della direttiva) deve essere preceduto dal delimitatore di commento a riga singola (//) o racchiuso tra delimitatori di commento (/ \* \* /).</span><span class="sxs-lookup"><span data-stu-id="b4988-127">Any text that follows a directive (except an argument or value that is part of the directive) must be preceded by the single-line comment delimiter (//) or enclosed in comment delimiters (/\* \*/).</span></span> <span data-ttu-id="b4988-128">Le righe che contengono le direttive per il preprocessore possono essere continuate immediatamente prima del marcatore di fine riga con una barra rovesciata ( \) .</span><span class="sxs-lookup"><span data-stu-id="b4988-128">Lines containing preprocessor directives can be continued by immediately preceding the end-of-line marker with a backslash (\).</span></span>

<span data-ttu-id="b4988-129">Le direttive del preprocessore possono essere visualizzate in qualsiasi punto di un file di origine, ma si applicano solo al resto del file di origine.</span><span class="sxs-lookup"><span data-stu-id="b4988-129">Preprocessor directives can appear anywhere in a source file, but they apply only to the remainder of the source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4988-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b4988-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4988-131">Appendice (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b4988-131">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 





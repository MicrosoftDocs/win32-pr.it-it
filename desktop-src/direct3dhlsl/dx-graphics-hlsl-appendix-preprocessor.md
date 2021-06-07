---
title: Direttive per il preprocessore (HLSL)
description: Le direttive per il preprocessore, ad esempio \ define e \ ifdef, vengono in genere usate per semplificare la modifica dei programmi di origine e la compilazione in ambienti di esecuzione diversi.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8efdd996ddeb58c09d1c8250f174c21bb939f082
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386830"
---
# <a name="preprocessor-directives-hlsl"></a><span data-ttu-id="13004-103">Direttive per il preprocessore (HLSL)</span><span class="sxs-lookup"><span data-stu-id="13004-103">Preprocessor Directives (HLSL)</span></span>

<span data-ttu-id="13004-104">Le direttive per il preprocessore, ad esempio [ \# define](dx-graphics-hlsl-appendix-pre-define.md) e [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), vengono in genere usate per semplificare la modifica e la compilazione dei programmi di origine in ambienti di esecuzione diversi.</span><span class="sxs-lookup"><span data-stu-id="13004-104">Preprocessor directives, such as [\#define](dx-graphics-hlsl-appendix-pre-define.md) and [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), are typically used to make source programs easy to change and easy to compile in different execution environments.</span></span> <span data-ttu-id="13004-105">Le direttive nel file di origine indicano al preprocessore di eseguire azioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="13004-105">Directives in the source file tell the preprocessor to perform specific actions.</span></span> <span data-ttu-id="13004-106">Ad esempio, il preprocessore può sostituire i token nel testo, inserire il contenuto di altri file nel file di origine o eliminare la compilazione di parte del file rimuovendo sezioni di testo.</span><span class="sxs-lookup"><span data-stu-id="13004-106">For example, the preprocessor can replace tokens in the text, insert the contents of other files into the source file, or suppress compilation of part of the file by removing sections of text.</span></span> <span data-ttu-id="13004-107">Le righe del preprocessore vengono riconosciute ed eseguite prima dell'espansione di una macro.</span><span class="sxs-lookup"><span data-stu-id="13004-107">Preprocessor lines are recognized and carried out before macro expansion.</span></span> <span data-ttu-id="13004-108">Pertanto, se una macro si espande in modo da risultare simile a un comando del preprocessore, tale comando non sarà riconosciuto dal preprocessore.</span><span class="sxs-lookup"><span data-stu-id="13004-108">Therefore, if a macro expands into something that looks like a preprocessor command, that command is not recognized by the preprocessor.</span></span>

<span data-ttu-id="13004-109">Le istruzioni del preprocessore utilizzano lo stesso set di caratteri delle istruzioni del file di origine, con l'eccezione che le sequenze di escape non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="13004-109">Preprocessor statements use the same character set as source file statements, with the exception that escape sequences are not supported.</span></span> <span data-ttu-id="13004-110">Il set di caratteri utilizzati nelle istruzioni del preprocessore equivale al set di caratteri di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="13004-110">The character set used in preprocessor statements is the same as the execution character set.</span></span> <span data-ttu-id="13004-111">Il preprocessore riconosce anche i valori di carattere negativi.</span><span class="sxs-lookup"><span data-stu-id="13004-111">The preprocessor also recognizes negative character values.</span></span>

<span data-ttu-id="13004-112">Il preprocessore HLSL riconosce le direttive seguenti:</span><span class="sxs-lookup"><span data-stu-id="13004-112">The HLSL preprocessor recognizes the following directives:</span></span>

-   [<span data-ttu-id="13004-113">\#Definire</span><span class="sxs-lookup"><span data-stu-id="13004-113">\#define</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
-   [<span data-ttu-id="13004-114">\#elif</span><span class="sxs-lookup"><span data-stu-id="13004-114">\#elif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="13004-115">\#else</span><span class="sxs-lookup"><span data-stu-id="13004-115">\#else</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="13004-116">\#endif</span><span class="sxs-lookup"><span data-stu-id="13004-116">\#endif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="13004-117">\#Errore</span><span class="sxs-lookup"><span data-stu-id="13004-117">\#error</span></span>](dx-graphics-hlsl-appendix-pre-error.md)
-   [<span data-ttu-id="13004-118">\#if</span><span class="sxs-lookup"><span data-stu-id="13004-118">\#if</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="13004-119">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="13004-119">\#ifdef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="13004-120">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="13004-120">\#ifndef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="13004-121">\#Includono</span><span class="sxs-lookup"><span data-stu-id="13004-121">\#include</span></span>](dx-graphics-hlsl-appendix-pre-include.md)
-   [<span data-ttu-id="13004-122">\#Linea</span><span class="sxs-lookup"><span data-stu-id="13004-122">\#line</span></span>](dx-graphics-hlsl-appendix-pre-line.md)
-   [<span data-ttu-id="13004-123">\#pragma</span><span class="sxs-lookup"><span data-stu-id="13004-123">\#pragma</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [<span data-ttu-id="13004-124">\#undef</span><span class="sxs-lookup"><span data-stu-id="13004-124">\#undef</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)

<span data-ttu-id="13004-125">Il simbolo di numero ( ) deve essere il primo carattere senza spazio nella riga contenente la direttiva . Gli spazi vuoti possono essere presenti tra il simbolo di numero e la prima lettera \# della direttiva.</span><span class="sxs-lookup"><span data-stu-id="13004-125">The number sign (\#) must be the first nonwhite-space character on the line containing the directive; white-space characters can appear between the number sign and the first letter of the directive.</span></span> <span data-ttu-id="13004-126">Alcune direttive includono argomenti o valori.</span><span class="sxs-lookup"><span data-stu-id="13004-126">Some directives include arguments or values.</span></span> <span data-ttu-id="13004-127">Qualsiasi testo che segue una direttiva (ad eccezione di un argomento o di un valore che fa parte della direttiva ) deve essere preceduto dal delimitatore di commento a riga singola (//) o racchiuso tra delimitatori di commento (/ \* \* /).</span><span class="sxs-lookup"><span data-stu-id="13004-127">Any text that follows a directive (except an argument or value that is part of the directive) must be preceded by the single-line comment delimiter (//) or enclosed in comment delimiters (/\* \*/).</span></span> <span data-ttu-id="13004-128">Le righe contenenti direttive del preprocessore possono essere continuate precedendo immediatamente il marcatore di fine riga con una barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="13004-128">Lines containing preprocessor directives can be continued by immediately preceding the end-of-line marker with a backslash (\\).</span></span>

<span data-ttu-id="13004-129">Le direttive del preprocessore possono essere visualizzate in qualsiasi punto di un file di origine, ma si applicano solo al resto del file di origine.</span><span class="sxs-lookup"><span data-stu-id="13004-129">Preprocessor directives can appear anywhere in a source file, but they apply only to the remainder of the source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13004-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13004-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13004-131">Appendice (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13004-131">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 





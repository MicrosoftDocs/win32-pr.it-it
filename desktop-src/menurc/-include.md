---
title: " include"
description: La direttiva \ include fa in modo che il compilatore di risorse elabori il file specificato nel parametro filename.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8d36f1d0ae24f3dc21d67eec57056872aabdbd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400178"
---
# <a name="-include"></a><span data-ttu-id="9328c-103">includere</span><span class="sxs-lookup"><span data-stu-id="9328c-103">' include'</span></span>

<span data-ttu-id="9328c-104">La direttiva **\# include** fa in modo che il compilatore di risorse elabori il file specificato nel parametro *filename* .</span><span class="sxs-lookup"><span data-stu-id="9328c-104">The **\#include** directive causes the resource compiler to process the file specified in the *filename* parameter.</span></span> <span data-ttu-id="9328c-105">Questo file deve essere un file di intestazione che definisce le costanti usate nel file di definizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9328c-105">This file should be a header file that defines the constants used in the resource-definition file.</span></span> <span data-ttu-id="9328c-106">Il file può utilizzare caratteri a byte singolo, a doppio byte o Unicode.</span><span class="sxs-lookup"><span data-stu-id="9328c-106">The file can use single-byte, double-byte, or Unicode characters.</span></span>

``` syntax
#include filename
```

<dl> <dt>

<span data-ttu-id="9328c-107"><span id="filename"></span><span id="FILENAME"></span>*filename*</span><span class="sxs-lookup"><span data-stu-id="9328c-107"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="9328c-108">Nome del file da includere.</span><span class="sxs-lookup"><span data-stu-id="9328c-108">Name of the file to be included.</span></span> <span data-ttu-id="9328c-109">Se il file si trova nella directory corrente, la stringa deve essere racchiusa tra virgolette doppie. Se il file si trova nella directory specificata dalla variabile di ambiente INCLUDE, la stringa deve essere racchiusa tra caratteri minore di e maggiore di (<>).</span><span class="sxs-lookup"><span data-stu-id="9328c-109">If the file is in the current directory, the string must be enclosed in double quotation marks; if the file is in the directory specified by the INCLUDE environment variable, the string must be enclosed in less-than and greater-than characters (<>).</span></span> <span data-ttu-id="9328c-110">È necessario fornire un percorso completo racchiuso tra virgolette doppie (") se il file non si trova nella directory corrente o nella directory specificata dalla variabile di ambiente INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="9328c-110">You must give a full path enclosed in double quotation marks (") if the file is not in the current directory or in the directory specified by the INCLUDE environment variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9328c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9328c-111">Remarks</span></span>

<span data-ttu-id="9328c-112">Usare l'istruzione seguente nel file di intestazione per racchiudere le istruzioni che possono essere compilate da un compilatore C ma non da RC:</span><span class="sxs-lookup"><span data-stu-id="9328c-112">Use the following statement in your header file to surround statements that can be compiled by a C compiler but not RC:</span></span>

``` syntax
#ifndef RC_INVOKED
```

<span data-ttu-id="9328c-113">In questo modo, è possibile usare gli stessi file di inclusione nei file con estensione c e RC.</span><span class="sxs-lookup"><span data-stu-id="9328c-113">This way, you can use the same include files in your .c and .rc files.</span></span>

## <a name="example"></a><span data-ttu-id="9328c-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="9328c-114">Example</span></span>

<span data-ttu-id="9328c-115">Questo esempio elabora i file di intestazione Windows. h e MyDefs. h durante la compilazione del file di definizione delle risorse:</span><span class="sxs-lookup"><span data-stu-id="9328c-115">This example processes the header files Windows.h and MyDefs.h while compiling the resource-definition file:</span></span>

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a><span data-ttu-id="9328c-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9328c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9328c-117">Direttive per il preprocessore</span><span class="sxs-lookup"><span data-stu-id="9328c-117">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 





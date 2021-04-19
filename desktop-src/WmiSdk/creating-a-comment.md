---
description: Il compilatore Managed Object Format (MOF) supporta due stili di commento usando due stili diversi di delimitatori di commento.
ms.assetid: 5ab71b45-7ed1-44c4-8710-6b833b0afb80
ms.tgt_platform: multiple
title: Creazione di un commento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d0e7cf2484fef018c62c8c47d9c55d245191681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310402"
---
# <a name="creating-a-comment"></a><span data-ttu-id="ab880-103">Creazione di un commento</span><span class="sxs-lookup"><span data-stu-id="ab880-103">Creating a Comment</span></span>

<span data-ttu-id="ab880-104">Il compilatore Managed Object Format (MOF) supporta due stili di commento usando due stili diversi di delimitatori di commento.</span><span class="sxs-lookup"><span data-stu-id="ab880-104">The Managed Object Format (MOF) compiler supports two styles of comment using two different styles of comment delimiters.</span></span>

<span data-ttu-id="ab880-105">Nella tabella seguente sono elencati i delimitatori utilizzati per i commenti e l'effetto dei delimitatori nel codice.</span><span class="sxs-lookup"><span data-stu-id="ab880-105">The following table lists the delimiters that are used for comments and the effect that the delimiters have in the code.</span></span>



| <span data-ttu-id="ab880-106">Delimitatore</span><span class="sxs-lookup"><span data-stu-id="ab880-106">Delimiter</span></span>   | <span data-ttu-id="ab880-107">Marks</span><span class="sxs-lookup"><span data-stu-id="ab880-107">Marks</span></span>                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | <span data-ttu-id="ab880-108">Inizio di un commento che termina alla fine della riga.</span><span class="sxs-lookup"><span data-stu-id="ab880-108">Start of a comment that terminates at the end of the line.</span></span>                                    |
| <span data-ttu-id="ab880-109">/\* e \*/</span><span class="sxs-lookup"><span data-stu-id="ab880-109">/\* and \*/</span></span> | <span data-ttu-id="ab880-110">Inizio e fine di un commento che può estendersi su più righe o solo una parte di una riga.</span><span class="sxs-lookup"><span data-stu-id="ab880-110">Beginning and end of a comment that may span multiple lines or only span a portion of a line.</span></span> |



 

<span data-ttu-id="ab880-111">Come nei linguaggi di programmazione C e C++, è necessario utilizzare il delimitatore//con solo commenti a riga singola, ma utilizzare i \* \* delimitatori/e/con i commenti a riga singola o a più righe.</span><span class="sxs-lookup"><span data-stu-id="ab880-111">As in the C and C++ programming languages, you must use the // delimiter with single-line comments only, but use the /\* and \*/ delimiters with either single-line or multiple-line comments.</span></span>

<span data-ttu-id="ab880-112">Nell'esempio di codice seguente vengono descritti i due stili di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="ab880-112">The following code example describes the two delimiter styles.</span></span>

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a><span data-ttu-id="ab880-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ab880-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab880-114">Progettazione di classi Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="ab880-114">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 




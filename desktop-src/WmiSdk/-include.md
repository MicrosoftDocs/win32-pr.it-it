---
description: Include il contenuto di un file MOF in un altro file MOF.
ms.assetid: 06765956-e4ee-467b-9b3b-d5da17b9cd82
ms.tgt_platform: multiple
title: '#include'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5eb3d203cff5bca7e5096082cca7ba531580ae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317580"
---
# <a name="include"></a><span data-ttu-id="c4718-103">' #include '</span><span class="sxs-lookup"><span data-stu-id="c4718-103">'#include'</span></span>
<span data-ttu-id="c4718-104">/\* Titolo: MyMof. mof                           *//*   title: MyMof2. mof \*/</span><span class="sxs-lookup"><span data-stu-id="c4718-104">/\*   Title: MyMof.Mof                           */ /*   Title: MyMof2.Mof                               \*/</span></span>

<span data-ttu-id="c4718-105">Il \# comando Includi preprocessore include il contenuto di un file MOF in un altro file MOF.</span><span class="sxs-lookup"><span data-stu-id="c4718-105">The \#include preprocessor command includes the contents of one MOF file into another MOF file.</span></span> <span data-ttu-id="c4718-106">Nell'esempio di codice riportato di seguito viene illustrata la sintassi per il \# comando Includi.</span><span class="sxs-lookup"><span data-stu-id="c4718-106">The following code example describes the syntax for the \#include command.</span></span>

``` syntax
#include ("Moffile.mof")
```

<span data-ttu-id="c4718-107">Nell'esempio precedente, Moffile. MOF è il nome del file MOF da includere.</span><span class="sxs-lookup"><span data-stu-id="c4718-107">In the previous example, Moffile.mof is the name of the MOF file to include.</span></span>

<span data-ttu-id="c4718-108">Nell'esempio seguente vengono illustrati due file MOF.</span><span class="sxs-lookup"><span data-stu-id="c4718-108">The following example shows two MOF files.</span></span> <span data-ttu-id="c4718-109">Quando si compila il primo file MOF, il compilatore compila automaticamente il secondo file MOF (Mymof2. MOF) nel percorso in cui si inserisce l' \# istruzione include.</span><span class="sxs-lookup"><span data-stu-id="c4718-109">When you compile the first MOF file, the compiler automatically compiles the second MOF file (Mymof2.mof) in the location you place the \#include statement.</span></span>

``` syntax
/*   Title: MyMof.Mof                           */
/*                                              */ 
/*   This MOF file shows how to include  */
/*   an MOF file in another MOF file             */

#pragma namespace("\\\\.\\root")            

#include ("mymof2.mof")

class myclass1 
{
    [key] string Description;
};


instance of myclass1
{
    Description = "Description of myclass1";
};
/*   End of MyMof.Mof                           */
```

<span data-ttu-id="c4718-110">Il file MOF seguente è incluso nell'esempio precedente:</span><span class="sxs-lookup"><span data-stu-id="c4718-110">The following MOF file is included in the previous example:</span></span>

``` syntax
/*   Title: MyMof2.Mof                               */
/*                                                   */
/*   This MOF is included when MyMof.MOF is compiled */

class myclass2 
{
    [key] string Description;
};


instance of myclass2
{
    Description = "Description of myclass2";
    
};
```

## <a name="related-topics"></a><span data-ttu-id="c4718-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4718-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4718-112">Comandi del preprocessore</span><span class="sxs-lookup"><span data-stu-id="c4718-112">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




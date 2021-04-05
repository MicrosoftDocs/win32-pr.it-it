---
title: include (attributo)
description: L'istruzione include di ACF specifica uno o più file di intestazione da includere nel codice stub generato.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- Includi attributo MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2aab7b7262bceb330e3f4645e4f16035b783197
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104116989"
---
# <a name="include-attribute"></a><span data-ttu-id="46f2e-104">include (attributo)</span><span class="sxs-lookup"><span data-stu-id="46f2e-104">include attribute</span></span>

<span data-ttu-id="46f2e-105">L'istruzione **include** di ACF specifica uno o più file di intestazione da includere nel codice stub generato.</span><span class="sxs-lookup"><span data-stu-id="46f2e-105">The ACF **include** statement specifies one or more header files to be included in the generated stub code.</span></span>

``` syntax
include filenames;
```

## <a name="parameters"></a><span data-ttu-id="46f2e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="46f2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46f2e-107">*nomi*</span><span class="sxs-lookup"><span data-stu-id="46f2e-107">*filenames*</span></span> 
</dt> <dd>

<span data-ttu-id="46f2e-108">Specifica il nome di uno o più file di intestazione del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="46f2e-108">Specifies the name of one or more C-language header files.</span></span> <span data-ttu-id="46f2e-109">Usare il nome file completo, incluso il. Estensione H e racchiudere ogni nome di file tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="46f2e-109">Use the full file name, including the .H extension and enclose each file name in quotation marks.</span></span> <span data-ttu-id="46f2e-110">Separare più nomi di file di intestazione in linguaggio C con virgole.</span><span class="sxs-lookup"><span data-stu-id="46f2e-110">Separate multiple C-language header file names with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46f2e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="46f2e-111">Remarks</span></span>

<span data-ttu-id="46f2e-112">In seguito all'istruzione **include** , il codice stub generato conterrà un'istruzione di **\# inclusione** del preprocessore C.</span><span class="sxs-lookup"><span data-stu-id="46f2e-112">As a result of the **include** statement, the generated stub code will contain a C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="46f2e-113">Quando si compilano gli stub, è necessario specificare il file di intestazione del linguaggio C.</span><span class="sxs-lookup"><span data-stu-id="46f2e-113">You supply the C-language header file when compiling the stubs.</span></span> <span data-ttu-id="46f2e-114">Le istruzioni include si basano sul meccanismo del compilatore C di ricerca della struttura di directory per i file inclusi.</span><span class="sxs-lookup"><span data-stu-id="46f2e-114">Include statements rely on the C-compiler mechanism of searching the directory structure for included files.</span></span>

> [!Note]  
> <span data-ttu-id="46f2e-115">Utilizzare la direttiva [**Import**](import.md) anziché la direttiva **include** per i file di sistema che contengono i tipi di dati che si desidera rendere disponibili per il file IDL.</span><span class="sxs-lookup"><span data-stu-id="46f2e-115">Use the [**import**](import.md) directive rather than the **include** directive for system files that contain data types you want to make available to the IDL file.</span></span> <span data-ttu-id="46f2e-116">La direttiva **Import** ignora i prototipi di funzione e consente di usare le opzioni del compilatore MIDL per ottimizzare la generazione delle routine di supporto.</span><span class="sxs-lookup"><span data-stu-id="46f2e-116">The **import** directive ignores function prototypes and allows you to use MIDL compiler switches that optimize the generation of support routines.</span></span>

 

## <a name="examples"></a><span data-ttu-id="46f2e-117">Esempi</span><span class="sxs-lookup"><span data-stu-id="46f2e-117">Examples</span></span>

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a><span data-ttu-id="46f2e-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="46f2e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f2e-119">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="46f2e-119">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="46f2e-120">**importare**</span><span class="sxs-lookup"><span data-stu-id="46f2e-120">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="46f2e-121">Importazione di file e librerie dei tipi</span><span class="sxs-lookup"><span data-stu-id="46f2e-121">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="46f2e-122">Importazione di file di intestazione di sistema</span><span class="sxs-lookup"><span data-stu-id="46f2e-122">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 





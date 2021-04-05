---
title: Risorsa HTML
description: Definisce un file HTML.
ms.assetid: d3cf8348-8c10-41d9-a061-cdce0e13abf4
keywords:
- Menu risorse HTML e altre risorse
topic_type:
- apiref
api_name:
- HTML
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db6477aed5180ae18b99f53f4ebadf9d0ad0c91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857494"
---
# <a name="html-resource"></a><span data-ttu-id="9f92d-104">Risorsa HTML</span><span class="sxs-lookup"><span data-stu-id="9f92d-104">HTML resource</span></span>

<span data-ttu-id="9f92d-105">Definisce un file HTML.</span><span class="sxs-lookup"><span data-stu-id="9f92d-105">Defines an HTML file.</span></span>

``` syntax
nameID HTML filename
```

## <a name="parameters"></a><span data-ttu-id="9f92d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f92d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f92d-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="9f92d-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="9f92d-108">Nome univoco o valore di Unsigned Integer a 16 bit che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9f92d-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="9f92d-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span><span class="sxs-lookup"><span data-stu-id="9f92d-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="9f92d-110">Nome del file HTML.</span><span class="sxs-lookup"><span data-stu-id="9f92d-110">The name of the HTML file.</span></span> <span data-ttu-id="9f92d-111">Deve essere un percorso completo o relativo se il file non si trova nella directory di lavoro corrente.</span><span class="sxs-lookup"><span data-stu-id="9f92d-111">It must be a full or relative path if the file is not in the current working directory.</span></span> <span data-ttu-id="9f92d-112">Il percorso deve essere una stringa racchiusa tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="9f92d-112">The path should be a quoted string.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9f92d-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="9f92d-113">Examples</span></span>

<span data-ttu-id="9f92d-114">Nell'esempio seguente viene definita una risorsa HTML:</span><span class="sxs-lookup"><span data-stu-id="9f92d-114">The following example defines an HTML resource:</span></span>

``` syntax
ID_RESPONSE_ERROR_PAGE  HTML "res\\responseerorpage.htm"
```

 

 





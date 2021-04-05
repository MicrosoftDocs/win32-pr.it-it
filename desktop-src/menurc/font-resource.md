---
title: Risorsa carattere
description: Definisce un file che contiene un tipo di carattere.
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- Menu delle risorse dei tipi di carattere e altre risorse
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e205d80779a1a228ee50e062f6904c1ed4a4934
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718739"
---
# <a name="font-resource"></a><span data-ttu-id="8a593-104">Risorsa carattere</span><span class="sxs-lookup"><span data-stu-id="8a593-104">FONT resource</span></span>

<span data-ttu-id="8a593-105">Definisce un file che contiene un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="8a593-105">Defines a file that contains a font.</span></span>

``` syntax
nameID FONT filename
```

## <a name="parameters"></a><span data-ttu-id="8a593-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a593-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a593-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="8a593-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="8a593-108">Valore Unsigned Integer univoco a 16 bit che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8a593-108">Unique 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="8a593-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span><span class="sxs-lookup"><span data-stu-id="8a593-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="8a593-110">Nome del file che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8a593-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="8a593-111">Il nome deve essere un nome di file valido. deve essere un percorso completo se il file non si trova nella directory di lavoro corrente.</span><span class="sxs-lookup"><span data-stu-id="8a593-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="8a593-112">Il percorso deve essere una stringa racchiusa tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="8a593-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="8a593-113">Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="8a593-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="8a593-114">Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="8a593-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8a593-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="8a593-115">Examples</span></span>

<span data-ttu-id="8a593-116">Nell'esempio seguente viene definita una singola risorsa del tipo di carattere:</span><span class="sxs-lookup"><span data-stu-id="8a593-116">The following example defines a single font resource:</span></span>

``` syntax
5 FONT  "cmroman.fnt"
```

 

 





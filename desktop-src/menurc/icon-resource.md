---
title: ICONA risorsa
description: Definisce una bitmap che definisce la forma dell'icona da usare per una determinata applicazione o un'icona animata.
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- ICONA menu risorse e altre risorse
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516732"
---
# <a name="icon-resource"></a><span data-ttu-id="18664-104">ICONA risorsa</span><span class="sxs-lookup"><span data-stu-id="18664-104">ICON resource</span></span>

<span data-ttu-id="18664-105">Definisce una bitmap che definisce la forma dell'icona da usare per una determinata applicazione o un'icona animata.</span><span class="sxs-lookup"><span data-stu-id="18664-105">Defines a bitmap that defines the shape of the icon to be used for a given application or an animated icon.</span></span>

``` syntax
nameID ICON filename
```

## <a name="parameters"></a><span data-ttu-id="18664-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="18664-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18664-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="18664-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="18664-108">Nome univoco o valore di Unsigned Integer a 16 bit che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="18664-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="18664-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span><span class="sxs-lookup"><span data-stu-id="18664-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="18664-110">Nome del file che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="18664-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="18664-111">Il nome deve essere un nome di file valido. deve essere un percorso completo se il file non si trova nella directory di lavoro corrente.</span><span class="sxs-lookup"><span data-stu-id="18664-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="18664-112">Il percorso deve essere una stringa racchiusa tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="18664-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="18664-113">Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="18664-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="18664-114">Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="18664-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="18664-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="18664-115">Remarks</span></span>

<span data-ttu-id="18664-116">Le risorse icona e cursore possono contenere più di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="18664-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="18664-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="18664-117">Examples</span></span>

<span data-ttu-id="18664-118">Nell'esempio seguente vengono definite due risorse icona:</span><span class="sxs-lookup"><span data-stu-id="18664-118">The following example defines two icon resources:</span></span>

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a><span data-ttu-id="18664-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18664-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18664-120">Uso delle icone</span><span class="sxs-lookup"><span data-stu-id="18664-120">Using Icons</span></span>](./using-icons.md)
</dt> </dl>

 

 
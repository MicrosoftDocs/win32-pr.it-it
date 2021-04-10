---
title: readonly (attributo)
description: L'attributo \ ReadOnly \ impedisce l'assegnazione a una variabile.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- attributo di sola lettura MIDL
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963034"
---
# <a name="readonly-attribute"></a><span data-ttu-id="94d02-104">readonly (attributo)</span><span class="sxs-lookup"><span data-stu-id="94d02-104">readonly attribute</span></span>

<span data-ttu-id="94d02-105">L'attributo **\[ ReadOnly \]** impedisce l'assegnazione a una variabile.</span><span class="sxs-lookup"><span data-stu-id="94d02-105">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span>

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a><span data-ttu-id="94d02-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="94d02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94d02-107">*facoltativo-attributi*</span><span class="sxs-lookup"><span data-stu-id="94d02-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="94d02-108">Zero o più attributi MIDL.</span><span class="sxs-lookup"><span data-stu-id="94d02-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="94d02-109">*tipo di dati*</span><span class="sxs-lookup"><span data-stu-id="94d02-109">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="94d02-110">Tipo di dati contenuti in base all' *identificatore*.</span><span class="sxs-lookup"><span data-stu-id="94d02-110">The type of the data contained by *identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="94d02-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="94d02-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="94d02-112">Nome con cui il software può fare riferimento al percorso di archiviazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="94d02-112">A name by which the software can refer to the data storage location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94d02-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="94d02-113">Remarks</span></span>

<span data-ttu-id="94d02-114">L'attributo **\[ ReadOnly \]** impedisce l'assegnazione a una variabile.</span><span class="sxs-lookup"><span data-stu-id="94d02-114">The **\[readonly\]** attribute prohibits assignment to a variable.</span></span> <span data-ttu-id="94d02-115">**\[ ReadOnly \]** è supportato solo a livello di parametro, non a livello di metodo.</span><span class="sxs-lookup"><span data-stu-id="94d02-115">**\[readonly\]** is only supported at the parameter level, not at the method level.</span></span>

### <a name="flags"></a><span data-ttu-id="94d02-116">Flags</span><span class="sxs-lookup"><span data-stu-id="94d02-116">Flags</span></span>

<span data-ttu-id="94d02-117">\_FREADONLY VARFLAG</span><span class="sxs-lookup"><span data-stu-id="94d02-117">VARFLAG\_FREADONLY</span></span>

## <a name="examples"></a><span data-ttu-id="94d02-118">Esempi</span><span class="sxs-lookup"><span data-stu-id="94d02-118">Examples</span></span>

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a><span data-ttu-id="94d02-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="94d02-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d02-120">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="94d02-120">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="94d02-121">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="94d02-121">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="94d02-122">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="94d02-122">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="94d02-123">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="94d02-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 
---
title: attributo dllname (STR)
description: L'attributo \ dllname \ definisce il nome della DLL che contiene i punti di ingresso per un modulo.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- attributo MIDL di dllname (STR)
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 990d277db855c2988021d19a0a756c49454546f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046729"
---
# <a name="dllnamestr-attribute"></a><span data-ttu-id="c8b2c-104">attributo dllname (STR)</span><span class="sxs-lookup"><span data-stu-id="c8b2c-104">dllname(str) attribute</span></span>

<span data-ttu-id="c8b2c-105">L'attributo **\[ dllname \]** definisce il nome della dll che contiene i punti di ingresso per un modulo.</span><span class="sxs-lookup"><span data-stu-id="c8b2c-105">The **\[dllname\]** attribute defines the name of the DLL that contains the entry points for a module.</span></span>

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
    [, optional-attribute-list]
]
module modulename
{
    elementlist
};
```

## <a name="parameters"></a><span data-ttu-id="c8b2c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8b2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8b2c-107">*UUID-numero*</span><span class="sxs-lookup"><span data-stu-id="c8b2c-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="c8b2c-108">Specifica un numero di identificazione univoco universale per il [**modulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="c8b2c-108">Specifies a universally unique identification number for the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8b2c-109">*filename*</span><span class="sxs-lookup"><span data-stu-id="c8b2c-109">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="c8b2c-110">Specifica una stringa a terminazione NULL che contiene il percorso completo del file dll.</span><span class="sxs-lookup"><span data-stu-id="c8b2c-110">Specifies a NULL-terminated string which contains the full path to the Dll file.</span></span>

</dd> <dt>

<span data-ttu-id="c8b2c-111">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="c8b2c-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c8b2c-112">Specifica un elenco di zero o più attributi dell'interfaccia MIDL.</span><span class="sxs-lookup"><span data-stu-id="c8b2c-112">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="c8b2c-113">*moduleName*</span><span class="sxs-lookup"><span data-stu-id="c8b2c-113">*modulename*</span></span> 
</dt> <dd>

<span data-ttu-id="c8b2c-114">Specifica il nome che altri componenti software possono usare per fare riferimento al modulo.</span><span class="sxs-lookup"><span data-stu-id="c8b2c-114">Specifies the name which other software components can use to refer to the module.</span></span>

</dd> <dt>

<span data-ttu-id="c8b2c-115">*elemento element*</span><span class="sxs-lookup"><span data-stu-id="c8b2c-115">*elementlist*</span></span> 
</dt> <dd>

<span data-ttu-id="c8b2c-116">Specifica una o più istruzioni di definizione degli elementi del modulo.</span><span class="sxs-lookup"><span data-stu-id="c8b2c-116">Specifies one or more module element definition statements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8b2c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8b2c-117">Remarks</span></span>

<span data-ttu-id="c8b2c-118">L'attributo **\[ dllname \]** è obbligatorio in un modulo.</span><span class="sxs-lookup"><span data-stu-id="c8b2c-118">The **\[dllname\]** attribute is required on a module.</span></span>

## <a name="examples"></a><span data-ttu-id="c8b2c-119">Esempi</span><span class="sxs-lookup"><span data-stu-id="c8b2c-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a><span data-ttu-id="c8b2c-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c8b2c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b2c-121">**modulo**</span><span class="sxs-lookup"><span data-stu-id="c8b2c-121">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="c8b2c-122">**voce**</span><span class="sxs-lookup"><span data-stu-id="c8b2c-122">**entry**</span></span>](entry.md)
</dt> <dt>

[<span data-ttu-id="c8b2c-123">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="c8b2c-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="c8b2c-124">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="c8b2c-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="c8b2c-125">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="c8b2c-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 
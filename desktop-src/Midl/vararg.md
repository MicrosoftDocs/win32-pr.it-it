---
title: vararg (attributo)
description: L'attributo \ vararg \ specifica che la funzione accetta un numero variabile di parametri. A tale scopo, l'ultimo parametro deve essere una matrice sicura di tipo VARIANT che contiene tutti i parametri rimanenti.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- attributo MIDL di vararg
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3880a3713daaff13fe827beb989dd377440af4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299752"
---
# <a name="vararg-attribute"></a><span data-ttu-id="6000c-105">vararg (attributo)</span><span class="sxs-lookup"><span data-stu-id="6000c-105">vararg attribute</span></span>

<span data-ttu-id="6000c-106">L'attributo **\[ vararg \]** specifica che la funzione accetta un numero variabile di parametri.</span><span class="sxs-lookup"><span data-stu-id="6000c-106">The **\[vararg\]** attribute specifies that the function takes a variable number of parameters.</span></span> <span data-ttu-id="6000c-107">A tale scopo, l'ultimo parametro deve essere una matrice sicura di tipo **Variant** che contiene tutti i parametri rimanenti.</span><span class="sxs-lookup"><span data-stu-id="6000c-107">To accomplish this, the last parameter must be a safe array of **VARIANT** type that contains all the remaining parameters.</span></span>

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a><span data-ttu-id="6000c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6000c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6000c-109">*facoltativo-attributi*</span><span class="sxs-lookup"><span data-stu-id="6000c-109">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="6000c-110">Specifica zero o più attributi da applicare alla funzione.</span><span class="sxs-lookup"><span data-stu-id="6000c-110">Specifies zero or more attributes to be applied to the function.</span></span> <span data-ttu-id="6000c-111">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="6000c-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="6000c-112">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="6000c-112">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="6000c-113">Tipo di dati restituiti dalla procedura remota al termine del processo.</span><span class="sxs-lookup"><span data-stu-id="6000c-113">The type of the data returned by the remote procedure upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="6000c-114">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="6000c-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6000c-115">Nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="6000c-115">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="6000c-116">*facoltativo-param-Attributes*</span><span class="sxs-lookup"><span data-stu-id="6000c-116">*optional-param-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="6000c-117">Specifica zero o più attributi da applicare al parametro della funzione immediatamente dopo l'elenco degli attributi.</span><span class="sxs-lookup"><span data-stu-id="6000c-117">Specifies zero or more attributes to be applied to the function parameter immediately following the attribute listing.</span></span>

</dd> <dt>

<span data-ttu-id="6000c-118">*param-list*</span><span class="sxs-lookup"><span data-stu-id="6000c-118">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6000c-119">Specifica tutti i parametri, Salva il parametro finale, variabile.</span><span class="sxs-lookup"><span data-stu-id="6000c-119">Specifies all the parameters, save the final, varying, parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6000c-120">*Last-param-name*</span><span class="sxs-lookup"><span data-stu-id="6000c-120">*last-param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6000c-121">Nome del parametro variabile.</span><span class="sxs-lookup"><span data-stu-id="6000c-121">The name of the varying parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6000c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="6000c-122">Remarks</span></span>

<span data-ttu-id="6000c-123">Non è possibile applicare gli **\[** attributi [**facoltativi**](optional.md) **\]** o **\[** [**DefaultValue**](defaultvalue.md) **\]** a tutti i parametri in una funzione con l'attributo **\[ vararg \]** .</span><span class="sxs-lookup"><span data-stu-id="6000c-123">You cannot apply the **\[**[**optional**](optional.md)**\]** or **\[**[**defaultvalue**](defaultvalue.md)**\]** attributes to any parameters in a function that has the **\[vararg\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="6000c-124">Esempi</span><span class="sxs-lookup"><span data-stu-id="6000c-124">Examples</span></span>

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a><span data-ttu-id="6000c-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6000c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6000c-126">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="6000c-126">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="6000c-127">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="6000c-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="6000c-128">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="6000c-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="6000c-129">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="6000c-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="6000c-130">**opzionale**</span><span class="sxs-lookup"><span data-stu-id="6000c-130">**optional**</span></span>](optional.md)
</dt> </dl>

 

 
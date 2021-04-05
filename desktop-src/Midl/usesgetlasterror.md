---
title: usesgetlasterror (attributo)
description: L'attributo \ usesgetlasterror \ segnala al chiamante che è possibile chiamare GetLastError per recuperare il codice di errore.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- attributo MIDL di usesgetlasterror
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0f403430f70fde71696ec2a35a34161f08bada9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725138"
---
# <a name="usesgetlasterror-attribute"></a><span data-ttu-id="2d9e6-104">usesgetlasterror (attributo)</span><span class="sxs-lookup"><span data-stu-id="2d9e6-104">usesgetlasterror attribute</span></span>

<span data-ttu-id="2d9e6-105">L'attributo **\[ \] usesgetlasterror** segnala al chiamante che è possibile chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per recuperare il codice di errore.</span><span class="sxs-lookup"><span data-stu-id="2d9e6-105">The **\[usesgetlasterror\]** attribute signals the caller that it can call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a><span data-ttu-id="2d9e6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d9e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d9e6-107">*Module-attributi*</span><span class="sxs-lookup"><span data-stu-id="2d9e6-107">*module-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="2d9e6-108">Zero o più attributi MIDL che verranno applicati al [**modulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="2d9e6-108">Zero or more MIDL attributes that will be applied to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d9e6-109">*nome modulo*</span><span class="sxs-lookup"><span data-stu-id="2d9e6-109">*module-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2d9e6-110">Nome dell'identificatore del [**modulo**](module.md).</span><span class="sxs-lookup"><span data-stu-id="2d9e6-110">The identifier name of the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d9e6-111">*ID di ingresso*</span><span class="sxs-lookup"><span data-stu-id="2d9e6-111">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="2d9e6-112">Specifica il punto di ingresso del modulo, ovvero il nome della funzione o il numero di identificazione intero.</span><span class="sxs-lookup"><span data-stu-id="2d9e6-112">Specifies the module entry point–function name or integer-identification number.</span></span>

</dd> <dt>

<span data-ttu-id="2d9e6-113">*altri attributi*</span><span class="sxs-lookup"><span data-stu-id="2d9e6-113">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="2d9e6-114">Zero o più attributi MIDL che verranno applicati alla procedura remota.</span><span class="sxs-lookup"><span data-stu-id="2d9e6-114">Zero or more MIDL attributes that will be applied to the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="2d9e6-115">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="2d9e6-115">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="2d9e6-116">Tipo di dati che la procedura remota restituirà al completamento.</span><span class="sxs-lookup"><span data-stu-id="2d9e6-116">The type of the data that the remote procedure will return upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="2d9e6-117">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="2d9e6-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2d9e6-118">Nome della procedura remota come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="2d9e6-118">The name of the remote procedure as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="2d9e6-119">*param-list*</span><span class="sxs-lookup"><span data-stu-id="2d9e6-119">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2d9e6-120">Zero o più parametri per la procedura remota.</span><span class="sxs-lookup"><span data-stu-id="2d9e6-120">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d9e6-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d9e6-121">Remarks</span></span>

<span data-ttu-id="2d9e6-122">È possibile impostare l'attributo **\[ \] usesgetlasterror** in un punto di ingresso del modulo, se tale punto di ingresso usa la funzione di Windows [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) per restituire i codici di errore.</span><span class="sxs-lookup"><span data-stu-id="2d9e6-122">The **\[usesgetlasterror\]** attribute can be set on a module entry point, if that entry point uses the Windows function [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return error codes.</span></span> <span data-ttu-id="2d9e6-123">L'attributo indica al chiamante che, se si verifica un errore durante la chiamata a tale funzione, il chiamante può quindi chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per recuperare il codice di errore.</span><span class="sxs-lookup"><span data-stu-id="2d9e6-123">The attribute tells the caller that, if there is an error when calling that function, the caller can then call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

## <a name="examples"></a><span data-ttu-id="2d9e6-124">Esempi</span><span class="sxs-lookup"><span data-stu-id="2d9e6-124">Examples</span></span>

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="2d9e6-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2d9e6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d9e6-126">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="2d9e6-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="2d9e6-127">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="2d9e6-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="2d9e6-128">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="2d9e6-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 
---
title: dual (attributo)
description: L'attributo dual identifica un'interfaccia che espone proprietà e metodi tramite IDispatch e direttamente tramite il VTBL.
ms.assetid: 1c214f10-57eb-4a05-99a8-a09770666a74
keywords:
- MIDL attributo doppio
topic_type:
- apiref
api_name:
- dual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39a9e44de464f58fd1ffc0606551b9a0203ae9e9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963064"
---
# <a name="dual-attribute"></a><span data-ttu-id="3332b-104">dual (attributo)</span><span class="sxs-lookup"><span data-stu-id="3332b-104">dual attribute</span></span>

<span data-ttu-id="3332b-105">L'attributo **Dual** identifica un'interfaccia che espone proprietà e metodi tramite [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e direttamente tramite il VTBL.</span><span class="sxs-lookup"><span data-stu-id="3332b-105">The **dual** attribute identifies an interface that exposes properties and methods through [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and directly through the VTBL.</span></span>

``` syntax
[
    uuid(uuid-number), 
    oleautomation,
    dual 
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="3332b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3332b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3332b-107">*UUID-numero*</span><span class="sxs-lookup"><span data-stu-id="3332b-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="3332b-108">Specifica un numero di identificazione univoco universale per l'interfaccia</span><span class="sxs-lookup"><span data-stu-id="3332b-108">Specifies a universally unique identification number for the interface</span></span>

</dd> <dt>

<span data-ttu-id="3332b-109">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="3332b-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3332b-110">Specifica un elenco di zero o più attributi MIDL aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="3332b-110">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="3332b-111">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="3332b-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3332b-112">Nome dell'interfaccia a cui verrà applicato l'attributo **doppio** .</span><span class="sxs-lookup"><span data-stu-id="3332b-112">The name of the interface to which the **dual** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3332b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3332b-113">Remarks</span></span>

<span data-ttu-id="3332b-114">Le interfacce identificate dall'attributo **duale** devono essere compatibili con l'automazione ed essere derivate da [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span><span class="sxs-lookup"><span data-stu-id="3332b-114">Interfaces identified by the **dual** attribute must be compatible with Automation and be derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span> <span data-ttu-id="3332b-115">Questo attributo non è consentito in dispinterfaces.</span><span class="sxs-lookup"><span data-stu-id="3332b-115">This attribute is not allowed on dispinterfaces.</span></span>

<span data-ttu-id="3332b-116">L'attributo **duale** crea un'interfaccia che è sia un'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che un'interfaccia Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="3332b-116">The **dual** attribute creates an interface that is both an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface and a Component Object Model (COM) interface.</span></span> <span data-ttu-id="3332b-117">Le prime sette voci di VTBL per un'interfaccia duale sono i sette membri di **IDispatch** e le voci rimanenti sono per l'accesso diretto ai membri dell'interfaccia duale.</span><span class="sxs-lookup"><span data-stu-id="3332b-117">The first seven entries of the VTBL for a dual interface are the seven members of **IDispatch**, and the remaining entries are for direct access to members of the dual interface.</span></span> <span data-ttu-id="3332b-118">Tutti i parametri e i tipi restituiti specificati per i membri di un'interfaccia duale devono essere tipi compatibili con l'automazione.</span><span class="sxs-lookup"><span data-stu-id="3332b-118">All the parameters and return types specified for members of a dual interface must be Automation-compatible types.</span></span>

<span data-ttu-id="3332b-119">Tutti i membri di un'interfaccia duale devono passare un HRESULT come valore restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="3332b-119">All members of a dual interface must pass an HRESULT as the function return value.</span></span> <span data-ttu-id="3332b-120">I membri, ad esempio le funzioni di accesso alle proprietà, che devono restituire altri valori, devono specificare l'ultimo parametro [**out**](out-idl.md), [**retval**](retval.md), che indica un parametro di output che restituisce il valore della funzione.</span><span class="sxs-lookup"><span data-stu-id="3332b-120">Members, such as property accessor functions, that need to return other values, should specify the last parameter as [**out**](out-idl.md), [**retval**](retval.md), indicating an output parameter that returns the value of the function.</span></span> <span data-ttu-id="3332b-121">Inoltre, i membri che devono supportare più impostazioni locali devono passare un parametro [**LCID**](lcid.md) .</span><span class="sxs-lookup"><span data-stu-id="3332b-121">In addition, members that need to support multiple locales should pass an [**lcid**](lcid.md) parameter.</span></span>

<span data-ttu-id="3332b-122">Una doppia interfaccia fornisce sia per la velocità di associazione diretta di VTBL sia per la flessibilità del binding [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="3332b-122">A dual interface provides for both the speed of direct VTBL binding and the flexibility of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) binding.</span></span> <span data-ttu-id="3332b-123">Per questo motivo, le interfacce duali sono consigliate quando possibile.</span><span class="sxs-lookup"><span data-stu-id="3332b-123">For this reason, dual interfaces are recommended whenever possible.</span></span>

> [!Note]  
> <span data-ttu-id="3332b-124">Se l'applicazione accede ai dati degli oggetti eseguendo il cast del puntatore *this* all'interno della chiamata di interfaccia, è consigliabile controllare i puntatori VTBL nell'oggetto in base ai puntatori VTBL per assicurarsi di essere connessi al proxy appropriato.</span><span class="sxs-lookup"><span data-stu-id="3332b-124">If your application accesses object data by casting the *this* pointer within the interface call, you should check the VTBL pointers in the object against your own VTBL pointers to ensure that you are connected to the appropriate proxy.</span></span>

 

<span data-ttu-id="3332b-125">Se si specifica **Dual** su un'interfaccia, l'interfaccia è compatibile con l'automazione e pertanto \_ vengono impostati i flag TYPEFLAG FDUAL e TypeFlag \_ FOLEAUTOMATION.</span><span class="sxs-lookup"><span data-stu-id="3332b-125">Specifying **dual** on an interface implies that the interface is compatible with Automation, and therefore causes both the TYPEFLAG\_FDUAL and TYPEFLAG\_FOLEAUTOMATION flags to be set.</span></span>

### <a name="flags"></a><span data-ttu-id="3332b-126">Flags</span><span class="sxs-lookup"><span data-stu-id="3332b-126">Flags</span></span>

<span data-ttu-id="3332b-127">TYPEFLAG \_ FDUAL, TypeFlag \_ FOLEAUTOMATION</span><span class="sxs-lookup"><span data-stu-id="3332b-127">TYPEFLAG\_FDUAL, TYPEFLAG\_FOLEAUTOMATION</span></span>

## <a name="examples"></a><span data-ttu-id="3332b-128">Esempi</span><span class="sxs-lookup"><span data-stu-id="3332b-128">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    oleautomation, dual
]
interface IHello : IDispatch
{
    //Diverse properties and methods defined here.
};
```

## <a name="see-also"></a><span data-ttu-id="3332b-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3332b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3332b-130">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="3332b-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="3332b-131">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="3332b-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="3332b-132">**LCID**</span><span class="sxs-lookup"><span data-stu-id="3332b-132">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="3332b-133">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="3332b-133">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="3332b-134">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="3332b-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="3332b-135">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="3332b-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="3332b-136">**out**</span><span class="sxs-lookup"><span data-stu-id="3332b-136">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="3332b-137">**retval**</span><span class="sxs-lookup"><span data-stu-id="3332b-137">**retval**</span></span>](retval.md)
</dt> </dl>

 

 
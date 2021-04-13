---
title: Attributo id
description: L'attributo \ ID \ specifica un DISPID per una funzione membro, ovvero una proprietà o un metodo, in un'interfaccia o in un'interfaccia dispatch.
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- attributo ID MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c57d8ea818bbd7b8fd5bd35816e6b7227eb917
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398883"
---
# <a name="id-attribute"></a><span data-ttu-id="f5f66-104">Attributo id</span><span class="sxs-lookup"><span data-stu-id="f5f66-104">id attribute</span></span>

<span data-ttu-id="f5f66-105">L'attributo **\[ ID \]** specifica un DISPID per una funzione membro, ovvero una proprietà o un metodo, in un'interfaccia o in un'interfaccia dispatch.</span><span class="sxs-lookup"><span data-stu-id="f5f66-105">The **\[id\]** attribute specifies a DISPID for a member function (either a property or a method, in an interface or dispinterface).</span></span>

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="f5f66-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5f66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5f66-107">*ID-NUM*</span><span class="sxs-lookup"><span data-stu-id="f5f66-107">*id-num*</span></span> 
</dt> <dd>

<span data-ttu-id="f5f66-108">DISPID per la funzione.</span><span class="sxs-lookup"><span data-stu-id="f5f66-108">DISPID for the function.</span></span>

</dd> <dt>

<span data-ttu-id="f5f66-109">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="f5f66-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f5f66-110">Specifica un elenco di zero o più attributi dell'interfaccia MIDL.</span><span class="sxs-lookup"><span data-stu-id="f5f66-110">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="f5f66-111">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="f5f66-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f5f66-112">Specifica il tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="f5f66-112">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="f5f66-113">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="f5f66-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f5f66-114">Specifica il nome della funzione nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="f5f66-114">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="f5f66-115">*facoltativo-parameter-list*</span><span class="sxs-lookup"><span data-stu-id="f5f66-115">*optional-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f5f66-116">Zero o più parametri di funzione.</span><span class="sxs-lookup"><span data-stu-id="f5f66-116">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5f66-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5f66-117">Remarks</span></span>

<span data-ttu-id="f5f66-118">Utilizzare l'attributo **\[ \] ID** quando si desidera assegnare un DISPID standard ( \_ ad esempio, un valore DISPID, un DISPID NEWENUM e \_ così via) a un metodo o una proprietà oppure quando si implementa il proprio **IDispatch:: Invoke** anziché delegare a **DispInvoke** / **ITypeInfo:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="f5f66-118">Use the **\[id\]** attribute when you want to assign a standard DISPID (like DISPID\_VALUE, DISPID\_NEWENUM etc.) to a method or property, or when you implement your own **IDispatch::Invoke** instead of delegating to **DispInvoke**/**ITypeInfo::Invoke**.</span></span>

<span data-ttu-id="f5f66-119">Se non si usa l'attributo **\[ ID \]** in un'interfaccia, il compilatore MIDL assegnerà un DISPID per l'utente.</span><span class="sxs-lookup"><span data-stu-id="f5f66-119">If you do not use the **\[id\]** attribute on an interface, the MIDL compiler will assign a DISPID for you.</span></span> <span data-ttu-id="f5f66-120">Tuttavia, quando si specifica un'interfaccia dispatch usando proprietà e metodi, è necessario specificare un DISPID per ogni proprietà e metodo.</span><span class="sxs-lookup"><span data-stu-id="f5f66-120">However, when you specify a dispinterface by using properties and methods, you must specify a DISPID for every property and method.</span></span>

<span data-ttu-id="f5f66-121">*ID-NUM* è un valore integrale positivo a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f5f66-121">The *id-num* is a 32-bit positive integral value.</span></span> <span data-ttu-id="f5f66-122">Gli ID negativi sono riservati per l'uso da automazione.</span><span class="sxs-lookup"><span data-stu-id="f5f66-122">Negative IDs are reserved for use by Automation.</span></span>

## <a name="examples"></a><span data-ttu-id="f5f66-123">Esempi</span><span class="sxs-lookup"><span data-stu-id="f5f66-123">Examples</span></span>

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a><span data-ttu-id="f5f66-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f5f66-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5f66-125">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="f5f66-125">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="f5f66-126">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="f5f66-126">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="f5f66-127">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="f5f66-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f5f66-128">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="f5f66-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="f5f66-129">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="f5f66-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 
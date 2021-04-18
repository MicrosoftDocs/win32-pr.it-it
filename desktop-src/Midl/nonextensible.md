---
title: Attributo nonextensible
description: L'attributo \ nonextensible \ specifica che l'implementazione di IDispatch include solo le proprietà e i metodi elencati nella descrizione dell'interfaccia e non può essere estesa con membri aggiuntivi in fase di esecuzione.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- attributo MIDL non estendibile
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e591ea4ab0647449ca9296b3b14a4aab9fff6991
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299635"
---
# <a name="nonextensible-attribute"></a><span data-ttu-id="3c8a7-104">Attributo nonextensible</span><span class="sxs-lookup"><span data-stu-id="3c8a7-104">nonextensible attribute</span></span>

<span data-ttu-id="3c8a7-105">L'attributo non **\[ \] estendibile** specifica che l'implementazione di [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) include solo le proprietà e i metodi elencati nella descrizione dell'interfaccia e non può essere estesa con membri aggiuntivi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3c8a7-105">The **\[nonextensible\]** attribute specifies that the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) implementation includes only the properties and methods listed in the interface description and cannot be extended with additional members at run time.</span></span> <span data-ttu-id="3c8a7-106">Per impostazione predefinita, l'automazione presuppone che le interfacce possano aggiungere membri in fase di esecuzione, ovvero presuppone che siano estendibili.</span><span class="sxs-lookup"><span data-stu-id="3c8a7-106">(By default, Automation assumes that interfaces may add members at run time; that is, it assumes they are extensible.)</span></span>

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="3c8a7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c8a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c8a7-108">*UUID-numero*</span><span class="sxs-lookup"><span data-stu-id="3c8a7-108">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="3c8a7-109">Specifica un numero di identificazione univoco universale per l' [**interfaccia**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="3c8a7-109">Specifies a universally unique identification number for the [**interface**](interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c8a7-110">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="3c8a7-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3c8a7-111">Specifica un elenco di zero o più attributi dell'interfaccia MIDL.</span><span class="sxs-lookup"><span data-stu-id="3c8a7-111">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="3c8a7-112">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="3c8a7-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3c8a7-113">Specifica il nome dell' [**interfaccia**](interface.md) o dell'interfaccia [**Dispatch**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="3c8a7-113">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c8a7-114">*interfaccia-definizione*</span><span class="sxs-lookup"><span data-stu-id="3c8a7-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="3c8a7-115">Specifica le istruzioni IDL che formano la definizione dell' [**interfaccia**](interface.md) o dell'interfaccia [**Dispatch**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="3c8a7-115">Specifies IDL statements that form the definition of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c8a7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c8a7-116">Remarks</span></span>

<span data-ttu-id="3c8a7-117">È possibile applicare l'attributo non **\[ estendibile \]** a un'interfaccia o a un'interfaccia dispatch.</span><span class="sxs-lookup"><span data-stu-id="3c8a7-117">You can apply the **\[nonextensible\]** attribute to either an interface or a dispinterface.</span></span> <span data-ttu-id="3c8a7-118">Tuttavia, un'interfaccia deve avere anche gli **\[** attributi [**Dual**](dual.md) **\]** e **\[** [**oleautomation**](oleautomation.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="3c8a7-118">However, an interface must also have the **\[**[**dual**](dual.md)**\]** and **\[**[**oleautomation**](oleautomation.md)**\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="3c8a7-119">Flags</span><span class="sxs-lookup"><span data-stu-id="3c8a7-119">Flags</span></span>

<span data-ttu-id="3c8a7-120">\_FNONEXTENSIBLE TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="3c8a7-120">TYPEFLAG\_FNONEXTENSIBLE</span></span>

## <a name="examples"></a><span data-ttu-id="3c8a7-121">Esempi</span><span class="sxs-lookup"><span data-stu-id="3c8a7-121">Examples</span></span>

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a><span data-ttu-id="3c8a7-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3c8a7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c8a7-123">Contenuto di una libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3c8a7-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="3c8a7-124">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="3c8a7-124">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="3c8a7-125">**Dual**</span><span class="sxs-lookup"><span data-stu-id="3c8a7-125">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="3c8a7-126">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="3c8a7-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="3c8a7-127">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="3c8a7-127">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="3c8a7-128">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="3c8a7-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="3c8a7-129">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="3c8a7-129">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="3c8a7-130">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="3c8a7-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 
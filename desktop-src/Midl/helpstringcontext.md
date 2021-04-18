---
title: attributo helpstringcontext
description: L'attributo \ helpstringcontext \ specifica un identificatore di contesto della guida a 32 bit nel file della guida. È possibile applicare l'attributo \ helpstringcontext \ a librerie, interfacce, interfacce dispatch, moduli, coclassi, istruzioni typedef, proprietà, parametri e metodi.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- attributo MIDL di helpstringcontext
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72ddded3beb768543f2f990aa9d656fba1fa8b98
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299083"
---
# <a name="helpstringcontext-attribute"></a><span data-ttu-id="d1565-105">attributo helpstringcontext</span><span class="sxs-lookup"><span data-stu-id="d1565-105">helpstringcontext attribute</span></span>

<span data-ttu-id="d1565-106">L'attributo **\[ helpstringcontext \]** specifica un identificatore di contesto della guida a 32 bit nel file della guida.</span><span class="sxs-lookup"><span data-stu-id="d1565-106">The **\[helpstringcontext\]** attribute specifies a 32-bit Help context identifier in the Help file.</span></span> <span data-ttu-id="d1565-107">È possibile applicare l' **\[ attributo \] helpstringcontext** a [**librerie**](library.md), [**interfacce, interfacce**](interface.md) [**Dispatch**](dispinterface.md), [**moduli**](module.md), [**coclassi**](coclass.md), istruzioni [**typedef**](typedef.md) , proprietà, parametri e metodi.</span><span class="sxs-lookup"><span data-stu-id="d1565-107">You can apply the **\[helpstringcontext\]** attribute to [**library**](library.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**coclass**](coclass.md), [**typedef**](typedef.md) statements, properties, parameters and methods.</span></span>

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a><span data-ttu-id="d1565-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1565-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1565-109">*ContextId*</span><span class="sxs-lookup"><span data-stu-id="d1565-109">*contextid*</span></span> 
</dt> <dd>

<span data-ttu-id="d1565-110">Intero univoco che identifica il testo della Guida associato all'istruzione MIDL corrente.</span><span class="sxs-lookup"><span data-stu-id="d1565-110">A unique integer that identifies the help text associated with the current MIDL statement.</span></span>

</dd> <dt>

<span data-ttu-id="d1565-111">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="d1565-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d1565-112">Zero o più attributi MIDL.</span><span class="sxs-lookup"><span data-stu-id="d1565-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="d1565-113">*IDL-Statement*</span><span class="sxs-lookup"><span data-stu-id="d1565-113">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="d1565-114">Istruzione MIDL a cui verrà applicato l'attributo **\[ helpstringcontext \]** .</span><span class="sxs-lookup"><span data-stu-id="d1565-114">The MIDL statement to which the **\[helpstringcontext\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1565-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1565-115">Remarks</span></span>

<span data-ttu-id="d1565-116">Usare le funzioni **GetDocumentation2** nelle interfacce **ITypeLib2** e **ITypeInfo2** per recuperare la stringa della guida.</span><span class="sxs-lookup"><span data-stu-id="d1565-116">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="d1565-117">Esempi</span><span class="sxs-lookup"><span data-stu-id="d1565-117">Examples</span></span>

``` syntax
[
    uuid(. . .),
    helpstringcontext(103),
    version(1.0)
]
library Lines
{
    [
        uuid(. . .), 
        helpstringcontext(102),
        oleautomation,
        dual
    ]
    interface ILine : IDispatch
    {
        [propget, helpstringcontext(100)] HRESULT Color([out, retval] long* ReturnVal); 
        [propput, helpstringcontext(101)] HRESULT Color([in] long rgb);
    }
};
```

 

 





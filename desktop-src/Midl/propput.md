---
title: propput (attributo)
description: L'attributo \ propput \ specifica una funzione di impostazione di proprietà. La proprietà deve avere lo stesso nome della funzione.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- attributo MIDL di propput
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bf5520a3f4f4872801145064f49a8108cf602a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117611"
---
# <a name="propput-attribute"></a><span data-ttu-id="a2455-105">propput (attributo)</span><span class="sxs-lookup"><span data-stu-id="a2455-105">propput attribute</span></span>

<span data-ttu-id="a2455-106">L'attributo **\[ propput \]** specifica una funzione di impostazione di proprietà.</span><span class="sxs-lookup"><span data-stu-id="a2455-106">The **\[propput\]** attribute specifies a property-setting function.</span></span> <span data-ttu-id="a2455-107">La proprietà deve avere lo stesso nome della funzione *.*</span><span class="sxs-lookup"><span data-stu-id="a2455-107">The property must have the same name as the function *.*</span></span>

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="a2455-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2455-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2455-109">*facoltativo-Property-Attributes*</span><span class="sxs-lookup"><span data-stu-id="a2455-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="a2455-110">Zero o più attributi della proprietà.</span><span class="sxs-lookup"><span data-stu-id="a2455-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="a2455-111">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="a2455-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="a2455-112">Tipo di dati restituiti dalla procedura remota.</span><span class="sxs-lookup"><span data-stu-id="a2455-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a2455-113">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="a2455-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a2455-114">Nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="a2455-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a2455-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="a2455-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="a2455-116">Zero o più parametri per la procedura remota.</span><span class="sxs-lookup"><span data-stu-id="a2455-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2455-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2455-117">Remarks</span></span>

<span data-ttu-id="a2455-118">Una funzione con l'attributo **\[ propput \]** deve avere anche l'ultimo parametro, ovvero un parametro **\[** [**con l'attributo in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a2455-118">A function that has the **\[propput\]** attribute must also have, as its last parameter, a parameter that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="a2455-119">**\[** [](propget.md) **\]** **\[ \]** **\[** [](propputref.md) **\]** Per una funzione è possibile specificare al massimo uno dei propget, propput e propputref.</span><span class="sxs-lookup"><span data-stu-id="a2455-119">At most, one of **\[**[**propget**](propget.md)**\]**, **\[propput\]** and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="a2455-120">Se l' **\[** attributo [**LCID**](lcid.md) **\]** viene usato nell'elenco di parametri di una funzione che contiene un parametro con l'attributo **\[ propput \]** , il parametro **\[ LCID \]** deve essere il secondo all'ultimo.</span><span class="sxs-lookup"><span data-stu-id="a2455-120">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[propput\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="a2455-121">Flags</span><span class="sxs-lookup"><span data-stu-id="a2455-121">Flags</span></span>

<span data-ttu-id="a2455-122">RICHIAMA \_ PROPERTYPUT</span><span class="sxs-lookup"><span data-stu-id="a2455-122">INVOKE\_PROPERTYPUT</span></span>

## <a name="examples"></a><span data-ttu-id="a2455-123">Esempi</span><span class="sxs-lookup"><span data-stu-id="a2455-123">Examples</span></span>

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a><span data-ttu-id="a2455-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a2455-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2455-125">Differenze tra MIDL e MKTYPLIB</span><span class="sxs-lookup"><span data-stu-id="a2455-125">Differences Between MIDL and MKTYPLIB</span></span>](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[<span data-ttu-id="a2455-126">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="a2455-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="a2455-127">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="a2455-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="a2455-128">**propget**</span><span class="sxs-lookup"><span data-stu-id="a2455-128">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="a2455-129">**propputref**</span><span class="sxs-lookup"><span data-stu-id="a2455-129">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="a2455-130">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="a2455-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 
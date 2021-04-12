---
title: coclass (attributo)
description: L'istruzione coclass fornisce un elenco delle interfacce supportate per un oggetto Component.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- attributo coclass MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398960"
---
# <a name="coclass-attribute"></a><span data-ttu-id="fa9da-104">coclass (attributo)</span><span class="sxs-lookup"><span data-stu-id="fa9da-104">coclass attribute</span></span>

<span data-ttu-id="fa9da-105">L'istruzione **coclass** fornisce un elenco delle interfacce supportate per un oggetto Component.</span><span class="sxs-lookup"><span data-stu-id="fa9da-105">The **coclass** statement provides a listing of the supported interfaces for a component object.</span></span>

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a><span data-ttu-id="fa9da-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa9da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa9da-107">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="fa9da-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fa9da-108">L' **\[** attributo [**UUID**](uuid.md) **\]** è obbligatorio in una **coclasse**.</span><span class="sxs-lookup"><span data-stu-id="fa9da-108">The **\[**[**uuid**](uuid.md)**\]** attribute is required on a **coclass**.</span></span> <span data-ttu-id="fa9da-109">Si tratta dello stesso **\[ UUID \]** registrato come CLSID nel database di registrazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="fa9da-109">This is the same **\[uuid\]** that is registered as a CLSID in the system registration database.</span></span> <span data-ttu-id="fa9da-110">Gli **\[** attributi [**helpstring**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**licensed**](licensed.md) **\]** , **\[** [**Version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** e **\[** [**appobject**](appobject.md) **\]** sono accettati, ma non necessari, prima di una definizione di **coclasse** .</span><span class="sxs-lookup"><span data-stu-id="fa9da-110">The **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**licensed**](licensed.md)**\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, and **\[**[**appobject**](appobject.md)**\]** attributes are accepted, but not required, before a **coclass** definition.</span></span>

</dd> <dt>

<span data-ttu-id="fa9da-111">*ClassName*</span><span class="sxs-lookup"><span data-stu-id="fa9da-111">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="fa9da-112">Nome con cui l'oggetto comune è noto nella libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="fa9da-112">Name by which the common object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="fa9da-113">*Interface-attributi*</span><span class="sxs-lookup"><span data-stu-id="fa9da-113">*interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="fa9da-114">Attributi facoltativi per l'interfaccia o l'interfaccia dispatch.</span><span class="sxs-lookup"><span data-stu-id="fa9da-114">Optional attributes for the interface or dispinterface.</span></span> <span data-ttu-id="fa9da-115">Gli **\[** attributi [**source**](source.md) **\]** , **\[** [**default**](default.md) **\]** e **\[** [**Restricted**](restricted.md) **\]** sono accettati in un'interfaccia o in un'interfaccia dispatch all'interno di una **coclasse**.</span><span class="sxs-lookup"><span data-stu-id="fa9da-115">The **\[**[**source**](source.md)**\]**, **\[**[**default**](default.md)**\]**, and **\[**[**restricted**](restricted.md)**\]** attributes are accepted on an interface or dispinterface within a **coclass**.</span></span>

</dd> <dt>

<span data-ttu-id="fa9da-116">*NomeInterfaccia*</span><span class="sxs-lookup"><span data-stu-id="fa9da-116">*interfacename*</span></span> 
</dt> <dd>

<span data-ttu-id="fa9da-117">Interfaccia dichiarata con la parola chiave [**Interface**](interface.md) o interfaccia dispatch dichiarata con la parola chiave [**Dispatch**](dispinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="fa9da-117">Either an interface declared with the [**interface**](interface.md) keyword, or a dispinterface declared with the [**dispinterface**](dispinterface.md) keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa9da-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa9da-118">Remarks</span></span>

<span data-ttu-id="fa9da-119">Il Component Object Model Microsoft definisce una classe come implementazione che consente **QueryInterface** tra un set di interfacce.</span><span class="sxs-lookup"><span data-stu-id="fa9da-119">The Microsoft Component Object Model defines a class as an implementation that allows **QueryInterface** between a set of interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="fa9da-120">Esempi</span><span class="sxs-lookup"><span data-stu-id="fa9da-120">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a><span data-ttu-id="fa9da-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fa9da-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa9da-122">**appobject**</span><span class="sxs-lookup"><span data-stu-id="fa9da-122">**appobject**</span></span>](appobject.md)
</dt> <dt>

[<span data-ttu-id="fa9da-123">**controllo**</span><span class="sxs-lookup"><span data-stu-id="fa9da-123">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="fa9da-124">**predefinita**</span><span class="sxs-lookup"><span data-stu-id="fa9da-124">**default**</span></span>](default.md)
</dt> <dt>

[<span data-ttu-id="fa9da-125">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="fa9da-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="fa9da-126">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="fa9da-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="fa9da-127">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="fa9da-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="fa9da-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="fa9da-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="fa9da-129">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="fa9da-129">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="fa9da-130">**nascosto**</span><span class="sxs-lookup"><span data-stu-id="fa9da-130">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="fa9da-131">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="fa9da-131">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="fa9da-132">**licensed**</span><span class="sxs-lookup"><span data-stu-id="fa9da-132">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="fa9da-133">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="fa9da-133">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="fa9da-134">**limitato**</span><span class="sxs-lookup"><span data-stu-id="fa9da-134">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="fa9da-135">**origine**</span><span class="sxs-lookup"><span data-stu-id="fa9da-135">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="fa9da-136">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="fa9da-136">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="fa9da-137">**uuid**</span><span class="sxs-lookup"><span data-stu-id="fa9da-137">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="fa9da-138">**Versione**</span><span class="sxs-lookup"><span data-stu-id="fa9da-138">**version**</span></span>](version.md)
</dt> </dl>

 

 
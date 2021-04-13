---
title: appobject (attributo)
description: L'attributo \ appobject \ identifica la coclasse come oggetto applicazione, che è associato a un'applicazione EXE completa.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- attributo MIDL di appobject
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d937d4a83306bc0c29f3c8c806bc043febec6a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398909"
---
# <a name="appobject-attribute"></a><span data-ttu-id="ce193-104">appobject (attributo)</span><span class="sxs-lookup"><span data-stu-id="ce193-104">appobject attribute</span></span>

<span data-ttu-id="ce193-105">L'attributo **\[ appobject \]** identifica la [**coclasse**](coclass.md) come oggetto applicazione, che è associato a un'applicazione exe completa.</span><span class="sxs-lookup"><span data-stu-id="ce193-105">The **\[appobject\]** attribute identifies the [**coclass**](coclass.md) as an application object, which is associated with a full EXE application.</span></span>

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a><span data-ttu-id="ce193-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce193-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce193-107">*UUID-numero*</span><span class="sxs-lookup"><span data-stu-id="ce193-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="ce193-108">Specifica un numero di identificazione univoco universale per la [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="ce193-108">Specifies a universally unique identification number for the [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce193-109">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="ce193-109">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ce193-110">Specifica zero o più attributi applicabili all'istruzione [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="ce193-110">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="ce193-111">Gli attributi **di coclasse** consentiti sono [**\[ helpstring \]**](helpstring.md) [**\[ \]**](helpcontext.md) [**\[ \]**](version.md) [**\[ \]**](hidden.md) [**\[ \]**](control.md) [**\[ \]**](licensed.md), HelpContext, licensed, Version, Control e Hidden.</span><span class="sxs-lookup"><span data-stu-id="ce193-111">Allowable **coclass** attributes are [**\[helpstring\]**](helpstring.md), [**\[helpcontext\]**](helpcontext.md), [**\[licensed\]**](licensed.md), [**\[version\]**](version.md), [**\[control\]**](control.md), and [**\[hidden\]**](hidden.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce193-112">*ClassName*</span><span class="sxs-lookup"><span data-stu-id="ce193-112">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="ce193-113">Specifica il nome in base al quale l'oggetto componente è noto nella libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="ce193-113">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="ce193-114">*definizione di coclasse*</span><span class="sxs-lookup"><span data-stu-id="ce193-114">*coclass definition*</span></span> 
</dt> <dd>

<span data-ttu-id="ce193-115">Specifica le istruzioni che compongono la definizione della [**coclasse**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="ce193-115">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce193-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce193-116">Remarks</span></span>

<span data-ttu-id="ce193-117">L'attributo **\[ appobject \]** indica anche che le funzioni e le proprietà della [**coclasse**](coclass.md) sono disponibili a livello globale nella libreria dei tipi corrente.</span><span class="sxs-lookup"><span data-stu-id="ce193-117">The **\[appobject\]** attribute also indicates that the functions and properties of the [**coclass**](coclass.md) are globally available in the current type library.</span></span>

<span data-ttu-id="ce193-118">La rappresentazione TypeFlag per questo attributo è TYPEFLAG \_ FAPPOBJECT</span><span class="sxs-lookup"><span data-stu-id="ce193-118">The typeflag representation for this attribute is TYPEFLAG\_FAPPOBJECT</span></span>

## <a name="examples"></a><span data-ttu-id="ce193-119">Esempi</span><span class="sxs-lookup"><span data-stu-id="ce193-119">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="ce193-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ce193-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce193-121">**coclass**</span><span class="sxs-lookup"><span data-stu-id="ce193-121">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="ce193-122">**controllo**</span><span class="sxs-lookup"><span data-stu-id="ce193-122">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="ce193-123">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="ce193-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="ce193-124">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="ce193-124">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="ce193-125">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="ce193-125">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="ce193-126">**nascosto**</span><span class="sxs-lookup"><span data-stu-id="ce193-126">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="ce193-127">**licensed**</span><span class="sxs-lookup"><span data-stu-id="ce193-127">**licensed**</span></span>](licensed.md)
</dt> <dt>

[<span data-ttu-id="ce193-128">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="ce193-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="ce193-129">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="ce193-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="ce193-130">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="ce193-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="ce193-131">**Versione**</span><span class="sxs-lookup"><span data-stu-id="ce193-131">**version**</span></span>](version.md)
</dt> </dl>

 

 
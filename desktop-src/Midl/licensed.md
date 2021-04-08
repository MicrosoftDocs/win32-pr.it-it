---
title: licensed (attributo)
description: L'attributo \ licensed \ indica che la coclasse a cui si applica è concessa in licenza ed è necessario crearne un'istanza usando IClassFactory2.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- attributo MIDL con licenza
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f24d8b6136cab86615e74838737bbda543b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046613"
---
# <a name="licensed-attribute"></a><span data-ttu-id="7bc88-104">licensed (attributo)</span><span class="sxs-lookup"><span data-stu-id="7bc88-104">licensed attribute</span></span>

<span data-ttu-id="7bc88-105">L'attributo **\[ licensed \]** indica che la [**coclasse**](coclass.md) a cui si applica è concessa in licenza ed è necessario crearne un'istanza utilizzando [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).</span><span class="sxs-lookup"><span data-stu-id="7bc88-105">The **\[licensed\]** attribute indicates that the [**coclass**](coclass.md) to which it applies is licensed, and must be instantiated using [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).</span></span>

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a><span data-ttu-id="7bc88-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bc88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bc88-107">*elenco attributi*</span><span class="sxs-lookup"><span data-stu-id="7bc88-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc88-108">Specifica zero o più attributi applicabili all'istruzione [**coclass**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="7bc88-108">Specifies zero or more attributes that apply to the [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="7bc88-109">Gli attributi di **coclasse** consentiti sono **\[** [**helpstring**](helpstring.md) **\]** **\[** [](helpcontext.md) **\]** **\[ \]**, HelpContext, licensed, **\[** [**Version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** e **\[** [**Hidden**](hidden.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7bc88-109">Allowable **coclass** attributes are **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[licensed\]**, **\[**[**version**](version.md)**\]**, **\[**[**control**](control.md)**\]**, and **\[**[**hidden**](hidden.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="7bc88-110">*ClassName*</span><span class="sxs-lookup"><span data-stu-id="7bc88-110">*classname*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc88-111">Specifica il nome in base al quale l'oggetto componente è noto nella libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="7bc88-111">Specifies the name by which the component object is known in the type library.</span></span>

</dd> <dt>

<span data-ttu-id="7bc88-112">*coclasse-definizione*</span><span class="sxs-lookup"><span data-stu-id="7bc88-112">*coclass-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc88-113">Specifica le istruzioni che compongono la definizione della [**coclasse**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="7bc88-113">Specifies statements that make up the [**coclass**](coclass.md) definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bc88-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bc88-114">Remarks</span></span>

<span data-ttu-id="7bc88-115">Le licenze sono una funzionalità di COM che consente di controllare la creazione di oggetti.</span><span class="sxs-lookup"><span data-stu-id="7bc88-115">Licensing is a feature of COM that provides control over object creation.</span></span> <span data-ttu-id="7bc88-116">Gli oggetti con licenza possono essere creati solo dai client autorizzati a utilizzarli.</span><span class="sxs-lookup"><span data-stu-id="7bc88-116">Licensed objects can be created only by clients that are authorized to use them.</span></span> <span data-ttu-id="7bc88-117">Le licenze sono implementate in COM tramite l'interfaccia [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) e dal supporto di un codice di licenza che può essere passato in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7bc88-117">Licensing is implemented in COM through the [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) interface and by support for a license key that can be passed at run time.</span></span>

### <a name="flags"></a><span data-ttu-id="7bc88-118">Flags</span><span class="sxs-lookup"><span data-stu-id="7bc88-118">Flags</span></span>

<span data-ttu-id="7bc88-119">\_FLICENSED TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="7bc88-119">TYPEFLAG\_FLICENSED</span></span>

## <a name="examples"></a><span data-ttu-id="7bc88-120">Esempi</span><span class="sxs-lookup"><span data-stu-id="7bc88-120">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a><span data-ttu-id="7bc88-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7bc88-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bc88-122">**coclass**</span><span class="sxs-lookup"><span data-stu-id="7bc88-122">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="7bc88-123">Contenuto di una libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7bc88-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="7bc88-124">**controllo**</span><span class="sxs-lookup"><span data-stu-id="7bc88-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="7bc88-125">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="7bc88-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="7bc88-126">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="7bc88-126">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="7bc88-127">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="7bc88-127">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="7bc88-128">**nascosto**</span><span class="sxs-lookup"><span data-stu-id="7bc88-128">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="7bc88-129">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="7bc88-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="7bc88-130">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="7bc88-130">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="7bc88-131">**Versione**</span><span class="sxs-lookup"><span data-stu-id="7bc88-131">**version**</span></span>](version.md)
</dt> </dl>

 

 
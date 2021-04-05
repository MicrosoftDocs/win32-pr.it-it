---
title: attributo Hyper
description: La parola chiave Hyper indica un intero a 64 bit che può essere dichiarato come con segno o senza segno.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- attributo MIDL Hyper
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57da7c0d54e5b9ffcd47f76b22825d13b0a8cff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718070"
---
# <a name="hyper-attribute"></a><span data-ttu-id="9a3d9-104">attributo Hyper</span><span class="sxs-lookup"><span data-stu-id="9a3d9-104">hyper attribute</span></span>

<span data-ttu-id="9a3d9-105">La parola chiave **Hyper** indica un intero a 64 bit che può essere dichiarato come con segno o senza segno.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-105">The keyword **hyper** indicates a 64-bit integer that can be declared as either signed or unsigned.</span></span>

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="9a3d9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a3d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a3d9-107">*elenco di dichiaratori*</span><span class="sxs-lookup"><span data-stu-id="9a3d9-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9a3d9-108">Specifica uno o più dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="9a3d9-109">I dichiaratori di funzione e le dichiarazioni di campi di bit non sono consentiti nelle strutture trasmesse in chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="9a3d9-110">Questi dichiaratori sono consentiti in strutture non trasmesse. Separare più dichiaratori con virgole.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a3d9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a3d9-111">Remarks</span></span>

<span data-ttu-id="9a3d9-112">Il tipo **Hyper** è uno dei tipi di base del linguaggio di definizione dell'interfaccia (IDL).</span><span class="sxs-lookup"><span data-stu-id="9a3d9-112">The **hyper** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="9a3d9-113">Il tipo **Hyper** può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro).</span><span class="sxs-lookup"><span data-stu-id="9a3d9-113">The **hyper** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="9a3d9-114">Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="9a3d9-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="9a3d9-115">Per le piattaforme a 16 bit, il compilatore MIDL sostituisce interi senza segno con **MIDL \_ uhyper**.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-115">For 16-bit platforms, the MIDL compiler replaces unsigned hyper integers with **MIDL\_uhyper**.</span></span> <span data-ttu-id="9a3d9-116">Ciò consente di definire interfacce con interi senza segno su piattaforme che non supportano direttamente interi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-116">This allows interfaces with unsigned hyper integers to be defined on platforms that do not directly support 64-bit integers.</span></span> <span data-ttu-id="9a3d9-117">**MIDL \_ uhyper** è definito nei file di intestazione RPC.</span><span class="sxs-lookup"><span data-stu-id="9a3d9-117">**MIDL\_uhyper** is defined in the RPC header files.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="9a3d9-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a3d9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a3d9-119">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="9a3d9-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="9a3d9-120">**const**</span><span class="sxs-lookup"><span data-stu-id="9a3d9-120">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="9a3d9-121">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="9a3d9-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="9a3d9-122">**typedef**</span><span class="sxs-lookup"><span data-stu-id="9a3d9-122">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 





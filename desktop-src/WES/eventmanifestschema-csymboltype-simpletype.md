---
title: Tipo semplice CSymbolType (registro eventi di Windows)
description: 'Tipo semplice CSymbolType (registro eventi di Windows): definisce un nome di simbolo C/C++ valido.'
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- EventLog di tipo semplice CSymbolType
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0c8c17a9f4bb7e86b573d60187ffffd55c6cb96
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090619"
---
# <a name="csymboltype-simple-type-windows-event-log"></a><span data-ttu-id="98ffe-104">Tipo semplice CSymbolType (registro eventi di Windows)</span><span class="sxs-lookup"><span data-stu-id="98ffe-104">CSymbolType Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="98ffe-105">Definisce un nome di simbolo C/C++ valido.</span><span class="sxs-lookup"><span data-stu-id="98ffe-105">Defines a valid C/C++ symbol name.</span></span>

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="98ffe-106">Modelli</span><span class="sxs-lookup"><span data-stu-id="98ffe-106">Patterns</span></span>

<span data-ttu-id="98ffe-107">Il **tipo semplice CSymbolType** è **un tipo xs:string** limitato dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="98ffe-107">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="98ffe-108">Il nome del simbolo può essere vuoto o contenere caratteri alfanumerici e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="98ffe-108">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="98ffe-109">Se il nome è vuoto, il compilatore di messaggi genererà il nome del simbolo.</span><span class="sxs-lookup"><span data-stu-id="98ffe-109">If the name is empty, the message compiler will generate the symbol name.</span></span> <span data-ttu-id="98ffe-110">Se si specifica un nome, il nome deve iniziare con un carattere di sottolineatura ( \_ ) o un carattere alfabetico.</span><span class="sxs-lookup"><span data-stu-id="98ffe-110">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="remarks"></a><span data-ttu-id="98ffe-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="98ffe-111">Remarks</span></span>

<span data-ttu-id="98ffe-112">Se il nome del simbolo è vuoto, il compilatore di messaggi usa l'attributo **name** dell'elemento che si sta definendo per generare il nome del simbolo.</span><span class="sxs-lookup"><span data-stu-id="98ffe-112">If the symbol name is empty, the message compiler uses the **name** attribute of the element that you are defining to generate the symbol name.</span></span> <span data-ttu-id="98ffe-113">Il compilatore sostituisce tutti i caratteri non alfanumerici e le cifre iniziali con caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="98ffe-113">The compiler replaces any non-alphanumeric characters and leading digits with underscores.</span></span> <span data-ttu-id="98ffe-114">Ad esempio, se l'attributo **name** del canale è Microsoft-Windows-SampleProvider/Operational, il compilatore userebbe Microsoft Windows SampleProvider Operational come \_ nome del \_ \_ simbolo.</span><span class="sxs-lookup"><span data-stu-id="98ffe-114">For example, if the channel's **name** attribute is Microsoft-Windows-SampleProvider/Operational, the compiler would use Microsoft\_Windows\_SampleProvider\_Operational as the symbol name.</span></span>

## <a name="requirements"></a><span data-ttu-id="98ffe-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98ffe-115">Requirements</span></span>



| <span data-ttu-id="98ffe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="98ffe-116">Requirement</span></span> | <span data-ttu-id="98ffe-117">Valore</span><span class="sxs-lookup"><span data-stu-id="98ffe-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="98ffe-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98ffe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="98ffe-119">Solo app desktop di Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="98ffe-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="98ffe-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98ffe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="98ffe-121">Solo app desktop di Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="98ffe-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 






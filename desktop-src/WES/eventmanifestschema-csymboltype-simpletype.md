---
title: Tipo semplice CSymbolType (registro eventi di Windows)
description: Definisce un nome di simbolo C/C++ valido.
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- Log eventi di tipo semplice CSymbolType
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67b0ccb7c573aa4d71c038f9133cea7c95cdfbd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301557"
---
# <a name="csymboltype-simple-type-windows-event-log"></a><span data-ttu-id="21a65-104">Tipo semplice CSymbolType (registro eventi di Windows)</span><span class="sxs-lookup"><span data-stu-id="21a65-104">CSymbolType Simple Type (Windows Event Log)</span></span>

<span data-ttu-id="21a65-105">Definisce un nome di simbolo C/C++ valido.</span><span class="sxs-lookup"><span data-stu-id="21a65-105">Defines a valid C/C++ symbol name.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="21a65-106">Modelli</span><span class="sxs-lookup"><span data-stu-id="21a65-106">Patterns</span></span>

<span data-ttu-id="21a65-107">Il tipo semplice **CSymbolType** è **xs: String** limitato dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="21a65-107">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="21a65-108">Il nome del simbolo può essere vuoto o contenere caratteri alfanumerici e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="21a65-108">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="21a65-109">Se il nome è vuoto, il compilatore del messaggio genererà il nome del simbolo.</span><span class="sxs-lookup"><span data-stu-id="21a65-109">If the name is empty, the message compiler will generate the symbol name.</span></span> <span data-ttu-id="21a65-110">Se si specifica un nome, il nome deve iniziare con un carattere di sottolineatura ( \_ ) o un carattere alfabetico.</span><span class="sxs-lookup"><span data-stu-id="21a65-110">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="remarks"></a><span data-ttu-id="21a65-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="21a65-111">Remarks</span></span>

<span data-ttu-id="21a65-112">Se il nome del simbolo è vuoto, il compilatore di messaggi utilizzerà l'attributo **Name** dell'elemento che si sta definendo per generare il nome del simbolo.</span><span class="sxs-lookup"><span data-stu-id="21a65-112">If the symbol name is empty, the message compiler uses the **name** attribute of the element that you are defining to generate the symbol name.</span></span> <span data-ttu-id="21a65-113">Il compilatore sostituisce tutti i caratteri non alfanumerici e le cifre iniziali con caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="21a65-113">The compiler replaces any non-alphanumeric characters and leading digits with underscores.</span></span> <span data-ttu-id="21a65-114">Se, ad esempio, l'attributo **Name** del canale è Microsoft-Windows-SampleProvider/Operational, il compilatore utilizzerà Microsoft \_ Windows \_ SampleProvider \_ Operational come nome del simbolo.</span><span class="sxs-lookup"><span data-stu-id="21a65-114">For example, if the channel's **name** attribute is Microsoft-Windows-SampleProvider/Operational, the compiler would use Microsoft\_Windows\_SampleProvider\_Operational as the symbol name.</span></span>

## <a name="requirements"></a><span data-ttu-id="21a65-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21a65-115">Requirements</span></span>



| <span data-ttu-id="21a65-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="21a65-116">Requirement</span></span> | <span data-ttu-id="21a65-117">Valore</span><span class="sxs-lookup"><span data-stu-id="21a65-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="21a65-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21a65-118">Minimum supported client</span></span><br/> | <span data-ttu-id="21a65-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="21a65-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="21a65-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21a65-120">Minimum supported server</span></span><br/> | <span data-ttu-id="21a65-121">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="21a65-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 






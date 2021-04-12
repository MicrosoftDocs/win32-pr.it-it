---
title: Tipo semplice strTableRef
description: Definisce una stringa che fa riferimento a una stringa di messaggio definita in una tabella di stringhe nel manifesto o in un file di messaggio (. MC).
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- Log eventi di tipo semplice strTableRef
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b7db446af056987e2aa25cd1483e9e53c01d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517998"
---
# <a name="strtableref-simple-type"></a><span data-ttu-id="5a460-104">Tipo semplice strTableRef</span><span class="sxs-lookup"><span data-stu-id="5a460-104">strTableRef Simple Type</span></span>

<span data-ttu-id="5a460-105">Definisce una stringa che fa riferimento a una stringa di messaggio definita in una tabella di stringhe nel manifesto o in un file di messaggio (. MC).</span><span class="sxs-lookup"><span data-stu-id="5a460-105">Defines a string that references a message string that is defined in a string table in the manifest or in a message (.mc) file.</span></span>

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="5a460-106">Modelli</span><span class="sxs-lookup"><span data-stu-id="5a460-106">Patterns</span></span>

<span data-ttu-id="5a460-107">Il tipo semplice **strTableRef** è **xs: String** limitato dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="5a460-107">The **strTableRef** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    <span data-ttu-id="5a460-108">Il formato della stringa deve essere $string. *stringid* o $MC.*SymbolId*.</span><span class="sxs-lookup"><span data-stu-id="5a460-108">The string must be of the form, $string.*stringid* or $mc.*symbolid*.</span></span> <span data-ttu-id="5a460-109">Se la stringa è nel formato $string. *stringid* deve fare riferimento a una stringa nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto.</span><span class="sxs-lookup"><span data-stu-id="5a460-109">If the string is of the form, $string.*stringid*, it must reference a string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <span data-ttu-id="5a460-110">Se la stringa è nel formato $mc.*SymbolId*, deve fare riferimento a un simbolo definito nel file di messaggio.</span><span class="sxs-lookup"><span data-stu-id="5a460-110">If the string is of the form, $mc.*symbolid*, it must reference a symbol defined in the message file.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a460-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a460-111">Requirements</span></span>



| <span data-ttu-id="5a460-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a460-112">Requirement</span></span> | <span data-ttu-id="5a460-113">Valore</span><span class="sxs-lookup"><span data-stu-id="5a460-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5a460-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a460-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5a460-115">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5a460-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5a460-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a460-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5a460-117">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a460-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 






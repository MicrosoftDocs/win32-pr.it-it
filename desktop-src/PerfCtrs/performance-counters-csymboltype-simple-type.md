---
description: Definisce un nome di simbolo C/C++ valido.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Tipo semplice CSymbolType (contatori delle prestazioni)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 418b5119046a89d93814ed8ac8bd427dc554bf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967506"
---
# <a name="csymboltype-simple-type-performance-counters"></a><span data-ttu-id="0d790-103">Tipo semplice CSymbolType (contatori delle prestazioni)</span><span class="sxs-lookup"><span data-stu-id="0d790-103">CSymbolType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="0d790-104">Definisce un nome di simbolo C/C++ valido.</span><span class="sxs-lookup"><span data-stu-id="0d790-104">Defines a valid C/C++ symbol name.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="0d790-105">Modelli</span><span class="sxs-lookup"><span data-stu-id="0d790-105">Patterns</span></span>

<span data-ttu-id="0d790-106">Il tipo semplice **CSymbolType** è **xs: String** limitato dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="0d790-106">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="0d790-107">Il nome del simbolo può essere vuoto o contenere caratteri alfanumerici e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="0d790-107">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="0d790-108">Se si specifica un nome, il nome deve iniziare con un carattere di sottolineatura ( \_ ) o un carattere alfabetico.</span><span class="sxs-lookup"><span data-stu-id="0d790-108">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d790-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d790-109">Requirements</span></span>



| <span data-ttu-id="0d790-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d790-110">Requirement</span></span> | <span data-ttu-id="0d790-111">Valore</span><span class="sxs-lookup"><span data-stu-id="0d790-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0d790-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d790-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0d790-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d790-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0d790-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d790-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0d790-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0d790-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





---
description: 'Tipo semplice CSymbolType (contatori delle prestazioni): definisce un nome di simbolo C/C++ valido.'
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Tipo semplice CSymbolType (contatori delle prestazioni)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0771bb1dffc006abf8e02e6c391278f7d0b03f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084229"
---
# <a name="csymboltype-simple-type-performance-counters"></a><span data-ttu-id="f3748-103">Tipo semplice CSymbolType (contatori delle prestazioni)</span><span class="sxs-lookup"><span data-stu-id="f3748-103">CSymbolType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="f3748-104">Definisce un nome di simbolo C/C++ valido.</span><span class="sxs-lookup"><span data-stu-id="f3748-104">Defines a valid C/C++ symbol name.</span></span>

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

## <a name="patterns"></a><span data-ttu-id="f3748-105">Modelli</span><span class="sxs-lookup"><span data-stu-id="f3748-105">Patterns</span></span>

<span data-ttu-id="f3748-106">Il **tipo semplice CSymbolType** è **un tipo xs:string** limitato dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="f3748-106">The **CSymbolType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    <span data-ttu-id="f3748-107">Il nome del simbolo può essere vuoto o contenere caratteri alfanumerici e caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="f3748-107">The symbol name can be empty or contain alphanumeric characters and underscores.</span></span> <span data-ttu-id="f3748-108">Se si specifica un nome, il nome deve iniziare con un carattere di sottolineatura ( \_ ) o un carattere alfabetico.</span><span class="sxs-lookup"><span data-stu-id="f3748-108">If you specify a name, the name must begin with an underscore (\_) or an alphabetical character.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3748-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3748-109">Requirements</span></span>



| <span data-ttu-id="f3748-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3748-110">Requirement</span></span> | <span data-ttu-id="f3748-111">Valore</span><span class="sxs-lookup"><span data-stu-id="f3748-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3748-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3748-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f3748-113">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f3748-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f3748-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3748-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f3748-115">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3748-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





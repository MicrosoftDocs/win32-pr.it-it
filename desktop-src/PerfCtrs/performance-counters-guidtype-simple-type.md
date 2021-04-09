---
description: Definisce un tipo di identificatore univoco globale nel formato del registro di sistema.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Tipo semplice GUIDType (contatori delle prestazioni)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 758509a564c26db493fa2e9ed971aba71878cdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881742"
---
# <a name="guidtype-simple-type-performance-counters"></a><span data-ttu-id="1b3ab-103">Tipo semplice GUIDType (contatori delle prestazioni)</span><span class="sxs-lookup"><span data-stu-id="1b3ab-103">GUIDType Simple Type (Performance Counters)</span></span>

<span data-ttu-id="1b3ab-104">Definisce un tipo di identificatore univoco globale nel formato del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1b3ab-104">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="1b3ab-105">Modelli</span><span class="sxs-lookup"><span data-stu-id="1b3ab-105">Patterns</span></span>

<span data-ttu-id="1b3ab-106">Il tipo semplice **GUIDType** è **xs: String** limitato dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="1b3ab-106">The **GUIDType** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="1b3ab-107">Il valore deve essere un tipo di identificatore univoco globale nel formato del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1b3ab-107">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="1b3ab-108">Ad esempio, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="1b3ab-108">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="1b3ab-109">Usare GUIDGen.exe o UUIDGen.exe per creare un GUID.</span><span class="sxs-lookup"><span data-stu-id="1b3ab-109">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b3ab-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b3ab-110">Requirements</span></span>



| <span data-ttu-id="1b3ab-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b3ab-111">Requirement</span></span> | <span data-ttu-id="1b3ab-112">Valore</span><span class="sxs-lookup"><span data-stu-id="1b3ab-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1b3ab-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b3ab-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1b3ab-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b3ab-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1b3ab-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b3ab-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1b3ab-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b3ab-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





---
title: Tipo semplice versionType
description: Definisce un modello che specifica una versione di un'attività.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- Utilità di pianificazione di tipo semplice versionType
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df7010c6ecba29ad0ade80ce403018dd626d01cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340483"
---
# <a name="versiontype-simple-type"></a><span data-ttu-id="09a5e-104">Tipo semplice versionType</span><span class="sxs-lookup"><span data-stu-id="09a5e-104">versionType Simple Type</span></span>

<span data-ttu-id="09a5e-105">Definisce un modello che specifica una versione di un'attività.</span><span class="sxs-lookup"><span data-stu-id="09a5e-105">Defines a pattern that specifies a version of a task.</span></span>

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="09a5e-106">Modelli</span><span class="sxs-lookup"><span data-stu-id="09a5e-106">Patterns</span></span>

<span data-ttu-id="09a5e-107">Il tipo semplice **versionType** è una **stringa** limitata dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="09a5e-107">The **versionType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\d+(\.\d+){1,3}`

    <span data-ttu-id="09a5e-108">Double seguito da uno, due o tre valori Double.</span><span class="sxs-lookup"><span data-stu-id="09a5e-108">A double followed by one, two, or three doubles.</span></span> <span data-ttu-id="09a5e-109">Ad esempio, 1,2 o 1.2.3.</span><span class="sxs-lookup"><span data-stu-id="09a5e-109">For example, 1.2, or 1.2.3.</span></span>

## <a name="requirements"></a><span data-ttu-id="09a5e-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09a5e-110">Requirements</span></span>



| <span data-ttu-id="09a5e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="09a5e-111">Requirement</span></span> | <span data-ttu-id="09a5e-112">Valore</span><span class="sxs-lookup"><span data-stu-id="09a5e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="09a5e-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09a5e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="09a5e-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09a5e-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="09a5e-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09a5e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="09a5e-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09a5e-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






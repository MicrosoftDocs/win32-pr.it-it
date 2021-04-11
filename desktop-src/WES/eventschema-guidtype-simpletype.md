---
title: Tipo semplice GUIDType (schema di eventi)
description: Definisce un tipo di identificatore univoco globale nel formato del registro di sistema. | Tipo semplice GUIDType (schema di eventi)
ms.assetid: dbc305ef-6f07-4a70-9013-b89ccec889ea
keywords:
- Log eventi di tipo semplice GUIDType
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07635bc43ff07d65eee5f32786818ca7dad8dd64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352771"
---
# <a name="guidtype-simple-type-event-schema"></a><span data-ttu-id="7ff68-105">Tipo semplice GUIDType (schema di eventi)</span><span class="sxs-lookup"><span data-stu-id="7ff68-105">GUIDType simple type (Event Schema)</span></span>

<span data-ttu-id="7ff68-106">Definisce un tipo di identificatore univoco globale nel formato del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7ff68-106">Defines a globally unique identifier type, in Registry format.</span></span>

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="7ff68-107">Modelli</span><span class="sxs-lookup"><span data-stu-id="7ff68-107">Patterns</span></span>

<span data-ttu-id="7ff68-108">Il tipo semplice **GUIDType** è una stringa limitata dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="7ff68-108">The **GUIDType** simple type is a string that is restricted by the following pattern:</span></span>

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="7ff68-109">Il valore deve essere un tipo di identificatore univoco globale nel formato del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7ff68-109">The value must be a globally unique identifier type in Registry format.</span></span> <span data-ttu-id="7ff68-110">Ad esempio, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span><span class="sxs-lookup"><span data-stu-id="7ff68-110">For example, {5b2fc63a-8af4-44cb-960c-aefdced908d6}.</span></span> <span data-ttu-id="7ff68-111">Usare GUIDGen.exe o UUIDGen.exe per creare un GUID.</span><span class="sxs-lookup"><span data-stu-id="7ff68-111">Use GUIDGen.exe or UUIDGen.exe to create a GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff68-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ff68-112">Requirements</span></span>



| <span data-ttu-id="7ff68-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ff68-113">Requirement</span></span> | <span data-ttu-id="7ff68-114">Valore</span><span class="sxs-lookup"><span data-stu-id="7ff68-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ff68-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ff68-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff68-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ff68-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7ff68-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ff68-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff68-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ff68-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






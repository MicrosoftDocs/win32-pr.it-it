---
description: Definisce un tipo stringa per il nome o la descrizione di un profilo del criterio LAN wireless.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: Tipo semplice nameType (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8a2c0bdf281e27ba7a85271fe7777076ada9ff2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318261"
---
# <a name="nametype-simple-type-lan_policy"></a><span data-ttu-id="3e683-103">Tipo semplice nameType (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="3e683-103">nameType Simple Type (LAN_policy)</span></span>

<span data-ttu-id="3e683-104">Il tipo semplice nameType definisce un tipo stringa per il nome o la descrizione di un profilo di criteri LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="3e683-104">The nameType simple type defines a string type for either the name or the description of a wireless LAN policy profile.</span></span> <span data-ttu-id="3e683-105">I nomi e le descrizioni sono stringhe con almeno un carattere e una lunghezza massima di 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="3e683-105">Names and descriptions are strings that are at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="3e683-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e683-106">Requirements</span></span>



| <span data-ttu-id="3e683-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e683-107">Requirement</span></span> | <span data-ttu-id="3e683-108">Valore</span><span class="sxs-lookup"><span data-stu-id="3e683-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3e683-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e683-109">Minimum supported client</span></span><br/> | <span data-ttu-id="3e683-110">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e683-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3e683-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e683-111">Minimum supported server</span></span><br/> | <span data-ttu-id="3e683-112">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3e683-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





---
description: Includere il nome o una descrizione di un profilo LAN wireless.
ms.assetid: cb30d76f-051f-4b90-a0e0-24088a99ca9b
title: Tipo semplice nameType (LAN_policy) (profilo)
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
ms.openlocfilehash: e73e8bd013836767e2a943616407aea9f563fea2
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334340"
---
# <a name="nametype-simple-type-lan_policy-for-profileschema"></a><span data-ttu-id="41ffc-103">Tipo semplice nameType (LAN_policy) per profileschema</span><span class="sxs-lookup"><span data-stu-id="41ffc-103">nameType Simple Type (LAN_policy) for profileschema</span></span>

<span data-ttu-id="41ffc-104">Il tipo semplice nameType può contenere il nome o una descrizione di un profilo LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="41ffc-104">The nameType simple type can contain either the name or a description of a wireless LAN profile.</span></span> <span data-ttu-id="41ffc-105">Il valore della stringa deve avere una lunghezza compresa tra 1 e 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="41ffc-105">This string value must be between 1 and 255 characters long.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="41ffc-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41ffc-106">Requirements</span></span>



| <span data-ttu-id="41ffc-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="41ffc-107">Requirement</span></span> | <span data-ttu-id="41ffc-108">Valore</span><span class="sxs-lookup"><span data-stu-id="41ffc-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="41ffc-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41ffc-109">Minimum supported client</span></span><br/> | <span data-ttu-id="41ffc-110">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="41ffc-110">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="41ffc-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41ffc-111">Minimum supported server</span></span><br/> | <span data-ttu-id="41ffc-112">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41ffc-112">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="41ffc-113">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="41ffc-113">Redistributable</span></span><br/>          | <span data-ttu-id="41ffc-114">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="41ffc-114">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 





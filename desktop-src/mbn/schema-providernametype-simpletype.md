---
description: Definisce un tipo stringa per l'elemento ProviderName nel profilo Mobile Broadband.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: Tipo semplice providerNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: df61473358a9ed4453bc28f1b5c7974082e515bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526022"
---
# <a name="providernametype-simple-type"></a><span data-ttu-id="323d4-103">Tipo semplice providerNameType</span><span class="sxs-lookup"><span data-stu-id="323d4-103">providerNameType Simple Type</span></span>

<span data-ttu-id="323d4-104">Il tipo semplice **providerNameType** definisce un tipo stringa per l'elemento [**providerName**](schema-providername-providertype-element.md) nel profilo Mobile Broadband.</span><span class="sxs-lookup"><span data-stu-id="323d4-104">The **providerNameType** simple type defines a string type for the [**ProviderName**](schema-providername-providertype-element.md) element in the Mobile Broadband profile.</span></span> <span data-ttu-id="323d4-105">Questa stringa ha una lunghezza compresa tra almeno un carattere e un massimo di 20 caratteri.</span><span class="sxs-lookup"><span data-stu-id="323d4-105">This string is at least one character long and at most 20 characters long.</span></span>

``` syntax
<xs:simpleType name="providerNameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="20"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="323d4-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="323d4-106">Requirements</span></span>



| <span data-ttu-id="323d4-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="323d4-107">Requirement</span></span> | <span data-ttu-id="323d4-108">Valore</span><span class="sxs-lookup"><span data-stu-id="323d4-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="323d4-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="323d4-109">Minimum supported client</span></span><br/> | <span data-ttu-id="323d4-110">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="323d4-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="323d4-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="323d4-111">Minimum supported server</span></span><br/> | <span data-ttu-id="323d4-112">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="323d4-112">None supported</span></span><br/>                         |



 

 





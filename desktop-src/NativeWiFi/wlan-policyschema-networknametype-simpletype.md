---
description: Definisce un tipo stringa per gli identificatori dei set di servizi (SSID).
ms.assetid: c9e79a3d-7d5c-4320-ade2-40124de00920
title: Tipo semplice networkNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkNameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6b6463644e1bd174be256d51b34ae2ae4ad9ce07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968308"
---
# <a name="networknametype-simple-type"></a><span data-ttu-id="53218-103">Tipo semplice networkNameType</span><span class="sxs-lookup"><span data-stu-id="53218-103">networkNameType Simple Type</span></span>

<span data-ttu-id="53218-104">Il tipo semplice networkNameType definisce un tipo stringa per gli identificatori dei set di servizi (SSID).</span><span class="sxs-lookup"><span data-stu-id="53218-104">The networkNameType simple type defines a string type for service set identifiers (SSIDs).</span></span> <span data-ttu-id="53218-105">Un SSID è una stringa con una lunghezza di almeno un carattere e una lunghezza massima di 32 caratteri.</span><span class="sxs-lookup"><span data-stu-id="53218-105">A SSID is a string that is at least one character long and at most 32 characters long.</span></span>

``` syntax
<xs:simpleType name="networkNameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="32"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="53218-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53218-106">Requirements</span></span>



| <span data-ttu-id="53218-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="53218-107">Requirement</span></span> | <span data-ttu-id="53218-108">Valore</span><span class="sxs-lookup"><span data-stu-id="53218-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53218-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53218-109">Minimum supported client</span></span><br/> | <span data-ttu-id="53218-110">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53218-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53218-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53218-111">Minimum supported server</span></span><br/> | <span data-ttu-id="53218-112">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53218-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





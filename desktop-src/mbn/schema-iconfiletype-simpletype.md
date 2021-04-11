---
description: Definisce un tipo stringa per l'elemento ICONFilePath nel profilo Mobile Broadband.
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: Tipo semplice iconFileType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: 168c2709f8b3049270711e286a35fbbd11e1ffef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129014"
---
# <a name="iconfiletype-simple-type"></a><span data-ttu-id="e0ff5-103">Tipo semplice iconFileType</span><span class="sxs-lookup"><span data-stu-id="e0ff5-103">iconFileType Simple Type</span></span>

<span data-ttu-id="e0ff5-104">Il tipo semplice **iconFileType** definisce un tipo stringa per l'elemento [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) nel profilo Mobile Broadband.</span><span class="sxs-lookup"><span data-stu-id="e0ff5-104">The **iconFileType** simple type defines a string type for the [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) element in the Mobile Broadband profile.</span></span> <span data-ttu-id="e0ff5-105">Questa stringa ha una lunghezza compresa tra almeno un carattere e una lunghezza massima di 1024 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e0ff5-105">This string is at least one character long and at most 1024 characters long.</span></span>

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="e0ff5-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0ff5-106">Requirements</span></span>



| <span data-ttu-id="e0ff5-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0ff5-107">Requirement</span></span> | <span data-ttu-id="e0ff5-108">Valore</span><span class="sxs-lookup"><span data-stu-id="e0ff5-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="e0ff5-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0ff5-109">Minimum supported client</span></span><br/> | <span data-ttu-id="e0ff5-110">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e0ff5-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="e0ff5-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0ff5-111">Minimum supported server</span></span><br/> | <span data-ttu-id="e0ff5-112">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e0ff5-112">None supported</span></span><br/>                         |



 

 





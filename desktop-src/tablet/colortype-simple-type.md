---
description: Definisce il tipo utilizzato per specificare i valori validi per il colore di determinati elementi in un file XML del journal.
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: Tipo semplice ColorType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305695"
---
# <a name="colortype-simple-type"></a><span data-ttu-id="28749-103">Tipo semplice ColorType</span><span class="sxs-lookup"><span data-stu-id="28749-103">ColorType Simple Type</span></span>

<span data-ttu-id="28749-104">Definisce il tipo utilizzato per specificare i valori validi per il colore di determinati elementi in un file XML del journal.</span><span class="sxs-lookup"><span data-stu-id="28749-104">Defines the type that is used to specify valid values for the color of certain elements in a Journal XML file.</span></span>

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="28749-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="28749-105">Remarks</span></span>

<span data-ttu-id="28749-106">Un colore può essere un valore RGB esadecimale nel formato \# RRGGBB.</span><span class="sxs-lookup"><span data-stu-id="28749-106">A color can be a hexadecimal RGB value in the format \#RRGGBB.</span></span> <span data-ttu-id="28749-107">Deve corrispondere all'espressione regolare seguente: \# \[ 0-9A-fa-F \] {6} .</span><span class="sxs-lookup"><span data-stu-id="28749-107">It must match the following regular expression: \#\[0-9a-fA-F\]{6}.</span></span> <span data-ttu-id="28749-108">Ad esempio: " \# 4a79B5".</span><span class="sxs-lookup"><span data-stu-id="28749-108">For example: "\#4a79B5".</span></span>

## <a name="requirements"></a><span data-ttu-id="28749-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28749-109">Requirements</span></span>



| <span data-ttu-id="28749-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="28749-110">Requirement</span></span> | <span data-ttu-id="28749-111">Valore</span><span class="sxs-lookup"><span data-stu-id="28749-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="28749-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28749-112">Minimum supported client</span></span><br/> | <span data-ttu-id="28749-113">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="28749-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="28749-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28749-114">Minimum supported server</span></span><br/> | <span data-ttu-id="28749-115">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="28749-115">None supported</span></span><br/>                                     |



 

 





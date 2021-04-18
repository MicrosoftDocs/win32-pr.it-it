---
title: Tipo semplice pathType
description: Definisce il numero minimo e massimo di caratteri per una stringa che definisce un percorso di file.
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- Utilità di pianificazione di tipo semplice pathType
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302685"
---
# <a name="pathtype-simple-type"></a><span data-ttu-id="1de5e-104">Tipo semplice pathType</span><span class="sxs-lookup"><span data-stu-id="1de5e-104">pathType Simple Type</span></span>

<span data-ttu-id="1de5e-105">Definisce il numero minimo e massimo di caratteri per una stringa che definisce un percorso di file.</span><span class="sxs-lookup"><span data-stu-id="1de5e-105">Defines the minimum and maximum number of characters for a string that defines a file path.</span></span> <span data-ttu-id="1de5e-106">Il percorso non può essere una stringa vuota e deve essere composto da meno di 260 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1de5e-106">The path cannot be an empty string, and must be less than 260 characters.</span></span>

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="1de5e-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1de5e-107">Requirements</span></span>



| <span data-ttu-id="1de5e-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="1de5e-108">Requirement</span></span> | <span data-ttu-id="1de5e-109">Valore</span><span class="sxs-lookup"><span data-stu-id="1de5e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1de5e-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1de5e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="1de5e-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1de5e-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1de5e-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1de5e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="1de5e-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1de5e-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






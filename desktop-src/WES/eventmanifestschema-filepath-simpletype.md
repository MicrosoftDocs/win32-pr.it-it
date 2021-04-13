---
title: Tipo semplice FilePath
description: Definisce una stringa che contiene il percorso completo di un file.
ms.assetid: a9b8f40a-fecd-4325-b068-a5aca3133134
keywords:
- Log eventi di tipo semplice FilePath
topic_type:
- apiref
api_name:
- filePath
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 492580634c1a48c88df6f50de2582c215ec7ecb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475610"
---
# <a name="filepath-simple-type"></a><span data-ttu-id="56b98-104">Tipo semplice FilePath</span><span class="sxs-lookup"><span data-stu-id="56b98-104">filePath Simple Type</span></span>

<span data-ttu-id="56b98-105">Definisce una stringa che contiene il percorso completo di un file.</span><span class="sxs-lookup"><span data-stu-id="56b98-105">Defines a string that contains a fully qualified path to a file.</span></span> <span data-ttu-id="56b98-106">Il percorso può contenere variabili di ambiente.</span><span class="sxs-lookup"><span data-stu-id="56b98-106">The path may contain environment variables.</span></span>

``` syntax
<xs:simpleType name="filePath">
    <xs:restriction
        base="xs:string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="56b98-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56b98-107">Requirements</span></span>



| <span data-ttu-id="56b98-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="56b98-108">Requirement</span></span> | <span data-ttu-id="56b98-109">Valore</span><span class="sxs-lookup"><span data-stu-id="56b98-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="56b98-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56b98-110">Minimum supported client</span></span><br/> | <span data-ttu-id="56b98-111">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="56b98-111">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="56b98-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56b98-112">Minimum supported server</span></span><br/> | <span data-ttu-id="56b98-113">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="56b98-113">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 






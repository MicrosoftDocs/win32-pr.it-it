---
title: Tipo semplice LengthType
description: Definisce un tipo di lunghezza utilizzato per specificare il numero di byte o caratteri di un elemento di dati a lunghezza variabile, ad esempio dati binari o una stringa ANSI o Unicode.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- Log eventi di tipo semplice LengthType
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341203"
---
# <a name="lengthtype-simple-type"></a><span data-ttu-id="15e8d-104">Tipo semplice LengthType</span><span class="sxs-lookup"><span data-stu-id="15e8d-104">LengthType Simple Type</span></span>

<span data-ttu-id="15e8d-105">Definisce un tipo di lunghezza utilizzato per specificare il numero di byte o caratteri di un elemento di dati a lunghezza variabile, ad esempio dati binari o una stringa ANSI o Unicode.</span><span class="sxs-lookup"><span data-stu-id="15e8d-105">Defines a length type that is used to specify the number of bytes or characters in a variable length data item such as binary data or an ANSI or Unicode string.</span></span> <span data-ttu-id="15e8d-106">Il valore può essere specificato come valore xs: unsignedShort o come stringa che fa riferimento al nome del nodo dell'elemento dati che contiene il valore short senza segno.</span><span class="sxs-lookup"><span data-stu-id="15e8d-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsigned short value.</span></span>

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="15e8d-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15e8d-107">Requirements</span></span>



| <span data-ttu-id="15e8d-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="15e8d-108">Requirement</span></span> | <span data-ttu-id="15e8d-109">Valore</span><span class="sxs-lookup"><span data-stu-id="15e8d-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="15e8d-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15e8d-110">Minimum supported client</span></span><br/> | <span data-ttu-id="15e8d-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15e8d-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="15e8d-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15e8d-112">Minimum supported server</span></span><br/> | <span data-ttu-id="15e8d-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="15e8d-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






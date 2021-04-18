---
title: Tipo complesso UserDataType
description: Definisce un frammento XML che specifica il layout dei dati dell'evento.
ms.assetid: 25147ace-cc36-43cc-ad85-6a1714f43dbe
keywords:
- Log eventi di tipo complesso UserDataType
topic_type:
- apiref
api_name:
- UserDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31186fbcc833219b6523f1fdeb986532984eb7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301096"
---
# <a name="userdatatype-complex-type"></a><span data-ttu-id="c4f58-104">Tipo complesso UserDataType</span><span class="sxs-lookup"><span data-stu-id="c4f58-104">UserDataType Complex Type</span></span>

<span data-ttu-id="c4f58-105">Definisce un frammento XML che specifica il layout dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c4f58-105">Defines an XML fragment that specifies the layout of the event data.</span></span>

``` syntax
<xs:complexType name="UserDataType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="c4f58-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4f58-106">Requirements</span></span>



| <span data-ttu-id="c4f58-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4f58-107">Requirement</span></span> | <span data-ttu-id="c4f58-108">Valore</span><span class="sxs-lookup"><span data-stu-id="c4f58-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c4f58-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4f58-109">Minimum supported client</span></span><br/> | <span data-ttu-id="c4f58-110">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4f58-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c4f58-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4f58-111">Minimum supported server</span></span><br/> | <span data-ttu-id="c4f58-112">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c4f58-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






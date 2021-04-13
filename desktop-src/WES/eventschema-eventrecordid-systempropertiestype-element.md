---
title: Elemento EventRecordID (SystemPropertiesType)
description: Numero di record assegnato all'evento quando è stato registrato.
ms.assetid: d042de4d-e532-432e-bba2-1876a26860a4
keywords:
- EventLog elemento EventRecordID
topic_type:
- apiref
api_name:
- EventRecordID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb937d075bc0ff5fc1cf8bf1335d1274aee4fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400299"
---
# <a name="eventrecordid-systempropertiestype-element"></a><span data-ttu-id="3a112-104">Elemento EventRecordID (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="3a112-104">EventRecordID (SystemPropertiesType) Element</span></span>

<span data-ttu-id="3a112-105">Numero di record assegnato all'evento quando è stato registrato.</span><span class="sxs-lookup"><span data-stu-id="3a112-105">The record number assigned to the event when it was logged.</span></span>

``` syntax
<xs:element name="EventRecordID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedLong"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="3a112-106">L'elemento **EventRecordID** è definito dal tipo complesso [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3a112-106">The **EventRecordID** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a112-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a112-107">Requirements</span></span>



| <span data-ttu-id="3a112-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a112-108">Requirement</span></span> | <span data-ttu-id="3a112-109">Valore</span><span class="sxs-lookup"><span data-stu-id="3a112-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a112-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a112-110">Minimum supported client</span></span><br/> | <span data-ttu-id="3a112-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a112-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3a112-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a112-112">Minimum supported server</span></span><br/> | <span data-ttu-id="3a112-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a112-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






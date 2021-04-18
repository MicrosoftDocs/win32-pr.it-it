---
title: Tipo complesso XmlType
description: Definisce un frammento XML.
ms.assetid: ac6ce2a2-4584-4181-9a39-aceab85d5c51
keywords:
- Log eventi di tipo complesso XmlType
topic_type:
- apiref
api_name:
- XmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a4d71d7f4f2685d6c5f1c0626392c79436b68d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400605"
---
# <a name="xmltype-complex-type"></a><span data-ttu-id="05c27-104">Tipo complesso XmlType</span><span class="sxs-lookup"><span data-stu-id="05c27-104">XmlType Complex Type</span></span>

<span data-ttu-id="05c27-105">Definisce un frammento XML.</span><span class="sxs-lookup"><span data-stu-id="05c27-105">Defines an XML fragment.</span></span> <span data-ttu-id="05c27-106">Qualsiasi istanza dello schema è consentita. il nodo di livello superiore del frammento deve contenere un attributo dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="05c27-106">Any schema instance is allowed; the top-level node in the fragment must contain a namespace attribute.</span></span>

``` syntax
<xs:complexType name="XmlType">
    <xs:sequence>
        <xs:any
            processContents="skip"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="05c27-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05c27-107">Requirements</span></span>



| <span data-ttu-id="05c27-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="05c27-108">Requirement</span></span> | <span data-ttu-id="05c27-109">Valore</span><span class="sxs-lookup"><span data-stu-id="05c27-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05c27-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05c27-110">Minimum supported client</span></span><br/> | <span data-ttu-id="05c27-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05c27-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05c27-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05c27-112">Minimum supported server</span></span><br/> | <span data-ttu-id="05c27-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05c27-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






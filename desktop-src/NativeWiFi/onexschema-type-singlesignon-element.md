---
description: Specifica quando viene eseguito l'accesso Single Sign-on.
ms.assetid: 23a7ab31-b29d-4f45-a384-bb2d2c18230f
title: Elemento Type (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 947c8801e5b2534f4c3b4e548a2a2f2c7a4250d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307831"
---
# <a name="type-singlesignon-element"></a><span data-ttu-id="53c6d-103">Elemento Type (singleSignOn)</span><span class="sxs-lookup"><span data-stu-id="53c6d-103">type (singleSignOn) Element</span></span>

<span data-ttu-id="53c6d-104">L'elemento Type (singleSignOn) specifica quando viene eseguito l'accesso Single Sign-on.</span><span class="sxs-lookup"><span data-stu-id="53c6d-104">The type (singleSignOn) element specifies when single sign on is performed.</span></span> <span data-ttu-id="53c6d-105">Quando è impostato su `preLogon` , l'accesso Single Sign-on viene eseguito prima dell'accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="53c6d-105">When set to `preLogon`, single sign on is performed before the user logs on.</span></span> <span data-ttu-id="53c6d-106">Quando è impostato su `postLogon` , Single Sign-on viene eseguito immediatamente dopo l'accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="53c6d-106">When set to `postLogon`, single sign on is performed immediately after the user logs on.</span></span>

<span data-ttu-id="53c6d-107">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.</span><span class="sxs-lookup"><span data-stu-id="53c6d-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="type"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="preLogon"
             />
            <xs:enumeration
                value="postLogon"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="53c6d-108">L'elemento **Type** è definito dall'elemento [**singleSignOn**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="53c6d-108">The **type** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="53c6d-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53c6d-109">Requirements</span></span>



| <span data-ttu-id="53c6d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="53c6d-110">Requirement</span></span> | <span data-ttu-id="53c6d-111">Valore</span><span class="sxs-lookup"><span data-stu-id="53c6d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53c6d-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53c6d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="53c6d-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53c6d-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53c6d-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53c6d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="53c6d-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53c6d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53c6d-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53c6d-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="53c6d-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="53c6d-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="53c6d-118">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="53c6d-118">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="53c6d-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="53c6d-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="53c6d-120">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="53c6d-120">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 





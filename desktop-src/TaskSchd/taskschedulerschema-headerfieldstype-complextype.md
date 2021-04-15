---
title: Tipo complesso headerFieldsType
description: Definisce gli elementi che specificano i campi per un'intestazione di posta elettronica.
ms.assetid: 1ad1b62d-5aca-4be4-b956-6f8c64761b2b
keywords:
- Utilità di pianificazione di tipo complesso headerFieldsType
topic_type:
- apiref
api_name:
- headerFieldsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edb783972217d0455eb2ee25fed31cf20e5b774b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475964"
---
# <a name="headerfieldstype-complex-type"></a><span data-ttu-id="92424-104">Tipo complesso headerFieldsType</span><span class="sxs-lookup"><span data-stu-id="92424-104">headerFieldsType Complex Type</span></span>

<span data-ttu-id="92424-105">Definisce gli elementi che specificano i campi per un'intestazione di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="92424-105">Defines the elements that specify the fields for an email header.</span></span>

``` syntax
<xs:complexType name="headerFieldsType">
    <xs:sequence>
        <xs:element name="HeaderField"
            type="headerFieldType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="92424-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="92424-106">Child elements</span></span>



| <span data-ttu-id="92424-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="92424-107">Element</span></span>                                                                         | <span data-ttu-id="92424-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="92424-108">Type</span></span>                                                                       | <span data-ttu-id="92424-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92424-109">Description</span></span>                                       |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="92424-110">**HeaderField**</span><span class="sxs-lookup"><span data-stu-id="92424-110">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="92424-111">**headerFieldType**</span><span class="sxs-lookup"><span data-stu-id="92424-111">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="92424-112">Specifica un campo in un'intestazione di messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="92424-112">Specifies a field in an email header.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="92424-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92424-113">Requirements</span></span>



| <span data-ttu-id="92424-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="92424-114">Requirement</span></span> | <span data-ttu-id="92424-115">Valore</span><span class="sxs-lookup"><span data-stu-id="92424-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="92424-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92424-116">Minimum supported client</span></span><br/> | <span data-ttu-id="92424-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92424-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="92424-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92424-118">Minimum supported server</span></span><br/> | <span data-ttu-id="92424-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92424-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






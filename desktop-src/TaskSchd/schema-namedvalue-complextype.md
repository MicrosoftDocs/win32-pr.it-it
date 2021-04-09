---
title: Tipo complesso namedValue
description: Definisce un nome associato a un valore in una coppia nome-valore.
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- Utilità di pianificazione di tipo complesso namedValue
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39d6990194350dcc032d42838f30bdd7339b0d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964516"
---
# <a name="namedvalue-complex-type"></a><span data-ttu-id="a8884-104">Tipo complesso namedValue</span><span class="sxs-lookup"><span data-stu-id="a8884-104">namedValue Complex Type</span></span>

<span data-ttu-id="a8884-105">Definisce un nome associato a un valore in una coppia nome-valore.</span><span class="sxs-lookup"><span data-stu-id="a8884-105">Defines a name that is associated with a value in a name-value pair.</span></span>

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="a8884-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="a8884-106">Attributes</span></span>



| <span data-ttu-id="a8884-107">Nome</span><span class="sxs-lookup"><span data-stu-id="a8884-107">Name</span></span> | <span data-ttu-id="a8884-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8884-108">Type</span></span>                                                                    | <span data-ttu-id="a8884-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8884-109">Description</span></span>                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8884-110">name</span><span class="sxs-lookup"><span data-stu-id="a8884-110">name</span></span> | [<span data-ttu-id="a8884-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="a8884-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="a8884-112">Specifica il nome associato a un valore in una coppia nome-valore.</span><span class="sxs-lookup"><span data-stu-id="a8884-112">Specifies the name that is associated with a value in a name-value pair.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="a8884-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8884-113">Requirements</span></span>



| <span data-ttu-id="a8884-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8884-114">Requirement</span></span> | <span data-ttu-id="a8884-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a8884-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8884-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8884-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a8884-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8884-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8884-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8884-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a8884-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8884-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






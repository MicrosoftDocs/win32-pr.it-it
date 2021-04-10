---
title: Tipo complesso networkSettingsType
description: Definisce gli elementi che forniscono le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- Utilità di pianificazione di tipo complesso networkSettingsType
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964434"
---
# <a name="networksettingstype-complex-type"></a><span data-ttu-id="7f674-104">Tipo complesso networkSettingsType</span><span class="sxs-lookup"><span data-stu-id="7f674-104">networkSettingsType Complex Type</span></span>

<span data-ttu-id="7f674-105">Definisce gli elementi che forniscono le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="7f674-105">Defines the elements that provide the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7f674-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7f674-106">Child elements</span></span>



| <span data-ttu-id="7f674-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7f674-107">Element</span></span>                                                              | <span data-ttu-id="7f674-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7f674-108">Type</span></span>                                                        | <span data-ttu-id="7f674-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f674-109">Description</span></span>                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f674-110">**ID**</span><span class="sxs-lookup"><span data-stu-id="7f674-110">**Id**</span></span>](taskschedulerschema-id-networksettingstype-element.md)     | [<span data-ttu-id="7f674-111">**guidType**</span><span class="sxs-lookup"><span data-stu-id="7f674-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md) | <span data-ttu-id="7f674-112">Specifica un valore GUID che identifica un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="7f674-112">Specifies a GUID value that identifies a network profile.</span></span> <br/>                       |
| [<span data-ttu-id="7f674-113">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7f674-113">**Name**</span></span>](taskschedulerschema-name-networksettingstype-element.md) | <span data-ttu-id="7f674-114">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="7f674-114">nonEmptyString</span></span>                                              | <span data-ttu-id="7f674-115">Specifica il nome di un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="7f674-115">Specifies the name of a network profile.</span></span> <span data-ttu-id="7f674-116">Il nome viene usato a scopo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="7f674-116">The name is used for display purposes.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="7f674-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f674-117">Requirements</span></span>



| <span data-ttu-id="7f674-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f674-118">Requirement</span></span> | <span data-ttu-id="7f674-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7f674-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7f674-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f674-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7f674-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f674-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7f674-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f674-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7f674-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f674-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






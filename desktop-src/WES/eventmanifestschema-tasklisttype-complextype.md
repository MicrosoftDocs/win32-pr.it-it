---
title: Tipo complesso TaskListType
description: Definisce un elenco di attività utilizzate per identificare i componenti di un'applicazione.
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- Log eventi di tipo complesso TaskListType
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad427743242ada8901e904fc4e03620ccc72f405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400198"
---
# <a name="tasklisttype-complex-type"></a><span data-ttu-id="88a03-104">Tipo complesso TaskListType</span><span class="sxs-lookup"><span data-stu-id="88a03-104">TaskListType Complex Type</span></span>

<span data-ttu-id="88a03-105">Definisce un elenco di attività utilizzate per identificare i componenti di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="88a03-105">Defines a list of tasks that are used to identify the components of an application.</span></span>

``` syntax
<xs:complexType name="TaskListType">
    <xs:sequence>
        <xs:element name="task"
            type="TaskType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="88a03-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="88a03-106">Child elements</span></span>



| <span data-ttu-id="88a03-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="88a03-107">Element</span></span>                                                       | <span data-ttu-id="88a03-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="88a03-108">Type</span></span>                                                         | <span data-ttu-id="88a03-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88a03-109">Description</span></span>                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="88a03-110">**attività**</span><span class="sxs-lookup"><span data-stu-id="88a03-110">**task**</span></span>](eventmanifestschema-task-tasklisttype-element.md) | [<span data-ttu-id="88a03-111">**TaskType**</span><span class="sxs-lookup"><span data-stu-id="88a03-111">**TaskType**</span></span>](eventmanifestschema-tasktype-complextype.md) | <span data-ttu-id="88a03-112">Definisce un componente o un sottocomponente di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="88a03-112">Defines a component or subcomponent of an application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="88a03-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88a03-113">Requirements</span></span>



| <span data-ttu-id="88a03-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="88a03-114">Requirement</span></span> | <span data-ttu-id="88a03-115">Valore</span><span class="sxs-lookup"><span data-stu-id="88a03-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="88a03-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88a03-116">Minimum supported client</span></span><br/> | <span data-ttu-id="88a03-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88a03-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="88a03-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88a03-118">Minimum supported server</span></span><br/> | <span data-ttu-id="88a03-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="88a03-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






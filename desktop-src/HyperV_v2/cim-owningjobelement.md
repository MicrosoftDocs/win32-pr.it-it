---
description: Rappresenta un'associazione tra un processo e l'elemento gestito che ha creato il processo.
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: Classe CIM_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OwningJobElement
- CIM_OwningJobElement.OwningElement
- CIM_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9d3879104a8f7406ff24dc2f63b79b51eb2fa58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317210"
---
# <a name="cim_owningjobelement-class"></a><span data-ttu-id="47f44-103">CIM \_ OwningJobElement (classe)</span><span class="sxs-lookup"><span data-stu-id="47f44-103">CIM\_OwningJobElement class</span></span>

<span data-ttu-id="47f44-104">Rappresenta un'associazione tra un processo e l'elemento gestito che ha creato il processo.</span><span class="sxs-lookup"><span data-stu-id="47f44-104">Represents an association between a job and the managed element that created the job.</span></span> <span data-ttu-id="47f44-105">Poiché un processo può spostarsi tra i sistemi e l'elemento gestito potrebbe non esistere per l'intera durata del processo, in alcuni casi, questa associazione potrebbe non essere possibile o esistere solo per una parte dell'esistenza del processo.</span><span class="sxs-lookup"><span data-stu-id="47f44-105">Since a job might move between systems, and the managed element might not exist for the entire duration of the job, in some cases, this association might not be possible or might only exist for a portion of the existence of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f44-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47f44-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::System::Processing"), ModelCorrespondence("CIM_Job.Owner"), AMENDMENT]
class CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  CIM_Job            REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="47f44-107">Members</span><span class="sxs-lookup"><span data-stu-id="47f44-107">Members</span></span>

<span data-ttu-id="47f44-108">La classe **CIM \_ OwningJobElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="47f44-108">The **CIM\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="47f44-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="47f44-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47f44-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="47f44-110">Properties</span></span>

<span data-ttu-id="47f44-111">La classe **CIM \_ OwningJobElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="47f44-111">The **CIM\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47f44-112">**Proprietàelement**</span><span class="sxs-lookup"><span data-stu-id="47f44-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f44-113">Tipo di dati **: \_ processo CIM**</span><span class="sxs-lookup"><span data-stu-id="47f44-113">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="47f44-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="47f44-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47f44-115">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47f44-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="47f44-116">Riferimento al processo creato dall'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="47f44-116">A reference to the job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="47f44-117">**OwningElement**</span><span class="sxs-lookup"><span data-stu-id="47f44-117">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f44-118">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="47f44-118">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="47f44-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="47f44-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47f44-120">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="47f44-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="47f44-121">Riferimento all'elemento gestito che ha creato il processo.</span><span class="sxs-lookup"><span data-stu-id="47f44-121">A reference to the managed element that created the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47f44-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47f44-122">Requirements</span></span>



| <span data-ttu-id="47f44-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="47f44-123">Requirement</span></span> | <span data-ttu-id="47f44-124">Valore</span><span class="sxs-lookup"><span data-stu-id="47f44-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f44-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47f44-125">Minimum supported client</span></span><br/> | <span data-ttu-id="47f44-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="47f44-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="47f44-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47f44-127">Minimum supported server</span></span><br/> | <span data-ttu-id="47f44-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="47f44-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="47f44-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="47f44-129">Namespace</span></span><br/>                | <span data-ttu-id="47f44-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="47f44-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="47f44-131">MOF</span><span class="sxs-lookup"><span data-stu-id="47f44-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47f44-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47f44-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="47f44-133">DLL</span><span class="sxs-lookup"><span data-stu-id="47f44-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47f44-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="47f44-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


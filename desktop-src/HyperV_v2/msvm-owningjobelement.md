---
description: Rappresenta un'associazione tra un processo e l'elemento gestito responsabile della creazione del processo.
ms.assetid: 1a100c7e-7e17-47dd-b730-c05c5e4dccda
title: Classe Msvm_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_OwningJobElement
- Msvm_OwningJobElement.OwningElement
- Msvm_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 34aa6f390d21a37421e09f30f9a775784717be9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318325"
---
# <a name="msvm_owningjobelement-class"></a><span data-ttu-id="2f76b-103">\_Classe MSVM OwningJobElement</span><span class="sxs-lookup"><span data-stu-id="2f76b-103">Msvm\_OwningJobElement class</span></span>

<span data-ttu-id="2f76b-104">Rappresenta un'associazione tra un processo e l'elemento gestito responsabile della creazione del processo.</span><span class="sxs-lookup"><span data-stu-id="2f76b-104">Represents an association between a job and the managed element responsible for the creation of the job.</span></span>

<span data-ttu-id="2f76b-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2f76b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f76b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f76b-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_OwningJobElement : CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  Msvm_ConcreteJob   REF OwnedElement;
};
```

## <a name="members"></a><span data-ttu-id="2f76b-107">Members</span><span class="sxs-lookup"><span data-stu-id="2f76b-107">Members</span></span>

<span data-ttu-id="2f76b-108">La **classe \_ OwningJobElement di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2f76b-108">The **Msvm\_OwningJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="2f76b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2f76b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f76b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2f76b-110">Properties</span></span>

<span data-ttu-id="2f76b-111">La **classe \_ OwningJobElement di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2f76b-111">The **Msvm\_OwningJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f76b-112">**Proprietàelement**</span><span class="sxs-lookup"><span data-stu-id="2f76b-112">**OwnedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f76b-113">Tipo di dati: **[ **MSVM \_ ConcreteJob**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="2f76b-113">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2f76b-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f76b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f76b-115">Processo creato dall'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="2f76b-115">The job created by the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="2f76b-116">**OwningElement**</span><span class="sxs-lookup"><span data-stu-id="2f76b-116">**OwningElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f76b-117">Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="2f76b-117">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="2f76b-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f76b-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f76b-119">Elemento gestito responsabile della creazione del processo.</span><span class="sxs-lookup"><span data-stu-id="2f76b-119">The managed element responsible for the creation of the job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f76b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f76b-120">Requirements</span></span>



| <span data-ttu-id="2f76b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f76b-121">Requirement</span></span> | <span data-ttu-id="2f76b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2f76b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f76b-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f76b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2f76b-124">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2f76b-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2f76b-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f76b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2f76b-126">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2f76b-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f76b-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2f76b-127">Namespace</span></span><br/>                | <span data-ttu-id="2f76b-128">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2f76b-128">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2f76b-129">MOF</span><span class="sxs-lookup"><span data-stu-id="2f76b-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f76b-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f76b-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f76b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2f76b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f76b-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f76b-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


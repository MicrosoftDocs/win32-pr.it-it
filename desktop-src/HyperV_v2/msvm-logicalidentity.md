---
description: Associa due elementi gestiti che rappresentano aspetti diversi della stessa entità sottostante.
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Classe Msvm_LogicalIdentity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2f8d2ee522fde3769c08bcbb78611b99eed8e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529047"
---
# <a name="msvm_logicalidentity-class"></a><span data-ttu-id="837f1-103">\_Classe MSVM LogicalIdentity</span><span class="sxs-lookup"><span data-stu-id="837f1-103">Msvm\_LogicalIdentity class</span></span>

<span data-ttu-id="837f1-104">Associa due elementi gestiti che rappresentano aspetti diversi della stessa entità sottostante.</span><span class="sxs-lookup"><span data-stu-id="837f1-104">Associates two managed elements that represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="837f1-105">Questa classe deriva da [**\_ LogicalIdentity CIM**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).</span><span class="sxs-lookup"><span data-stu-id="837f1-105">This class derives from [**CIM\_LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).</span></span>

<span data-ttu-id="837f1-106">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="837f1-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="837f1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="837f1-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="837f1-108">Members</span><span class="sxs-lookup"><span data-stu-id="837f1-108">Members</span></span>

<span data-ttu-id="837f1-109">La **classe \_ LogicalIdentity di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="837f1-109">The **Msvm\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="837f1-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="837f1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="837f1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="837f1-111">Properties</span></span>

<span data-ttu-id="837f1-112">La **classe \_ LogicalIdentity di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="837f1-112">The **Msvm\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="837f1-113">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="837f1-113">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="837f1-114">Tipo di dati **: \_ LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="837f1-114">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="837f1-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="837f1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="837f1-116">Riferimento a un aspetto alternativo dell'entità di sistema.</span><span class="sxs-lookup"><span data-stu-id="837f1-116">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="837f1-117">**SystemElement**</span><span class="sxs-lookup"><span data-stu-id="837f1-117">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="837f1-118">Tipo di dati **: \_ LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="837f1-118">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="837f1-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="837f1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="837f1-120">Riferimento a un aspetto dell'elemento logico.</span><span class="sxs-lookup"><span data-stu-id="837f1-120">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="837f1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="837f1-121">Requirements</span></span>



| <span data-ttu-id="837f1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="837f1-122">Requirement</span></span> | <span data-ttu-id="837f1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="837f1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="837f1-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="837f1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="837f1-125">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="837f1-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="837f1-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="837f1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="837f1-127">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="837f1-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="837f1-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="837f1-128">Namespace</span></span><br/>                | <span data-ttu-id="837f1-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="837f1-129">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="837f1-130">MOF</span><span class="sxs-lookup"><span data-stu-id="837f1-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="837f1-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="837f1-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="837f1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="837f1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="837f1-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="837f1-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="837f1-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="837f1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="837f1-135">**\_LOGICALIDENTITY CIM**</span><span class="sxs-lookup"><span data-stu-id="837f1-135">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dt>

[<span data-ttu-id="837f1-136">**\_LOGICALIDENTITY CIM**</span><span class="sxs-lookup"><span data-stu-id="837f1-136">**CIM\_LogicalIdentity**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 


---
description: Associa una testa video alla scheda video che la contiene.
ms.assetid: d15f4350-1529-4246-9ea2-8453e52516c6
title: Classe CIM_VideoHeadOnController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHeadOnController
- CIM_VideoHeadOnController.Antecedent
- CIM_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18178e6d9d7f1e684af1d4fe74336e1f2a02eedc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310560"
---
# <a name="cim_videoheadoncontroller-class"></a><span data-ttu-id="e018d-103">CIM \_ VideoHeadOnController (classe)</span><span class="sxs-lookup"><span data-stu-id="e018d-103">CIM\_VideoHeadOnController class</span></span>

<span data-ttu-id="e018d-104">Associa una testa video alla scheda video che la contiene.</span><span class="sxs-lookup"><span data-stu-id="e018d-104">Associates a video head with the video adapter that contains it.</span></span>

## <a name="syntax"></a><span data-ttu-id="e018d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e018d-105">Syntax</span></span>

``` syntax
[Association, Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHeadOnController : CIM_HostedDependency
{
  CIM_DisplayController REF Antecedent;
  CIM_VideoHead         REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e018d-106">Members</span><span class="sxs-lookup"><span data-stu-id="e018d-106">Members</span></span>

<span data-ttu-id="e018d-107">La classe **CIM \_ VideoHeadOnController** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e018d-107">The **CIM\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="e018d-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e018d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e018d-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e018d-109">Properties</span></span>

<span data-ttu-id="e018d-110">La classe **CIM \_ VideoHeadOnController** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e018d-110">The **CIM\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e018d-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="e018d-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e018d-112">Tipo di dati: **CIM \_ DisplayController**</span><span class="sxs-lookup"><span data-stu-id="e018d-112">Data type: **CIM\_DisplayController**</span></span>
</dt> <dt>

<span data-ttu-id="e018d-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e018d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e018d-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e018d-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e018d-115">Scheda video che include l'intestazione.</span><span class="sxs-lookup"><span data-stu-id="e018d-115">The video adapter that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="e018d-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="e018d-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e018d-117">Tipo di dati: **CIM \_ VideoHead**</span><span class="sxs-lookup"><span data-stu-id="e018d-117">Data type: **CIM\_VideoHead**</span></span>
</dt> <dt>

<span data-ttu-id="e018d-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e018d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e018d-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e018d-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e018d-120">L'intestazione della scheda video.</span><span class="sxs-lookup"><span data-stu-id="e018d-120">The head on the video adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e018d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e018d-121">Requirements</span></span>



| <span data-ttu-id="e018d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e018d-122">Requirement</span></span> | <span data-ttu-id="e018d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e018d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e018d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e018d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e018d-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e018d-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e018d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e018d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e018d-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e018d-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e018d-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e018d-128">Namespace</span></span><br/>                | <span data-ttu-id="e018d-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e018d-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e018d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e018d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e018d-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e018d-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e018d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e018d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e018d-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e018d-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e018d-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e018d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e018d-135">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="e018d-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 


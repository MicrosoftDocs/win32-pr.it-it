---
description: Fornisce informazioni aggiuntive da utilizzare con il metodo CreateReferencePoint della \_ classe VirtualSystemReferencePointService di MSVM.
ms.assetid: 6b997ba5-871c-4c33-9ed5-b9a13cbfaacd
title: Classe Msvm_VirtualSystemReferencePointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointSettingData
- Msvm_VirtualSystemReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea36f9504d9c2d6b7e875f32bb7cd0a0efd167da
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320462"
---
# <a name="msvm_virtualsystemreferencepointsettingdata-class"></a><span data-ttu-id="331cb-103">\_Classe MSVM VirtualSystemReferencePointSettingData</span><span class="sxs-lookup"><span data-stu-id="331cb-103">Msvm\_VirtualSystemReferencePointSettingData class</span></span>

<span data-ttu-id="331cb-104">Fornisce informazioni aggiuntive da utilizzare con il metodo [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) della classe [**\_ VirtualSystemReferencePointService di MSVM**](msvm-virtualsystemreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="331cb-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="331cb-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="331cb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="331cb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="331cb-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="331cb-107">Members</span><span class="sxs-lookup"><span data-stu-id="331cb-107">Members</span></span>

<span data-ttu-id="331cb-108">La **classe \_ VirtualSystemReferencePointSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="331cb-108">The **Msvm\_VirtualSystemReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="331cb-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="331cb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="331cb-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="331cb-110">Properties</span></span>

<span data-ttu-id="331cb-111">La **classe \_ VirtualSystemReferencePointSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="331cb-111">The **Msvm\_VirtualSystemReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="331cb-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="331cb-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="331cb-113">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="331cb-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="331cb-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="331cb-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="331cb-115">Livello di coerenza del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="331cb-115">The consistency level of the reference point.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="331cb-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="331cb-116">Requirements</span></span>



| <span data-ttu-id="331cb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="331cb-117">Requirement</span></span> | <span data-ttu-id="331cb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="331cb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="331cb-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="331cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="331cb-120">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="331cb-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="331cb-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="331cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="331cb-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="331cb-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="331cb-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="331cb-123">Namespace</span></span><br/>                | <span data-ttu-id="331cb-124">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="331cb-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="331cb-125">MOF</span><span class="sxs-lookup"><span data-stu-id="331cb-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="331cb-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="331cb-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="331cb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="331cb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="331cb-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="331cb-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="331cb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="331cb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="331cb-130">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="331cb-130">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 





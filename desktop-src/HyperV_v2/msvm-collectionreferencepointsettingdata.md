---
description: Fornisce informazioni aggiuntive da utilizzare con il metodo CreateReferencePoint della \_ classe CollectionReferencePointService di MSVM.
ms.assetid: abf7953a-e10e-4dab-962f-a7dde5126fbe
title: Classe Msvm_CollectionReferencePointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointSettingData
- Msvm_CollectionReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ac05518a3ea9512745e9d2391c2d8cf1d387c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130698"
---
# <a name="msvm_collectionreferencepointsettingdata-class"></a><span data-ttu-id="a49c4-103">\_Classe MSVM CollectionReferencePointSettingData</span><span class="sxs-lookup"><span data-stu-id="a49c4-103">Msvm\_CollectionReferencePointSettingData class</span></span>

<span data-ttu-id="a49c4-104">Fornisce informazioni aggiuntive da utilizzare con il metodo [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) della classe [**\_ CollectionReferencePointService di MSVM**](msvm-collectionreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a49c4-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="a49c4-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a49c4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a49c4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a49c4-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="a49c4-107">Members</span><span class="sxs-lookup"><span data-stu-id="a49c4-107">Members</span></span>

<span data-ttu-id="a49c4-108">La **classe \_ CollectionReferencePointSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a49c4-108">The **Msvm\_CollectionReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a49c4-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a49c4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a49c4-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a49c4-110">Properties</span></span>

<span data-ttu-id="a49c4-111">La **classe \_ CollectionReferencePointSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a49c4-111">The **Msvm\_CollectionReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a49c4-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="a49c4-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a49c4-113">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a49c4-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a49c4-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="a49c4-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a49c4-115">Livello di coerenza del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="a49c4-115">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a49c4-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a49c4-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="a49c4-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Coerente** con l'applicazione (1)</span><span class="sxs-lookup"><span data-stu-id="a49c4-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a49c4-118">Il punto di riferimento indica un punto nel tempo in cui il sistema virtuale si trova in uno stato di arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="a49c4-118">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="a49c4-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Coerente con l'arresto anomalo** (2)</span><span class="sxs-lookup"><span data-stu-id="a49c4-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a49c4-120">Il punto di riferimento indica un punto nel tempo in cui il sistema virtuale era in uno stato coerente con l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a49c4-120">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a49c4-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a49c4-121">Requirements</span></span>



| <span data-ttu-id="a49c4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a49c4-122">Requirement</span></span> | <span data-ttu-id="a49c4-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a49c4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a49c4-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a49c4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a49c4-125">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a49c4-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a49c4-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a49c4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a49c4-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a49c4-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a49c4-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a49c4-128">Namespace</span></span><br/>                | <span data-ttu-id="a49c4-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a49c4-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a49c4-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a49c4-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a49c4-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a49c4-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a49c4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a49c4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a49c4-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a49c4-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a49c4-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a49c4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a49c4-135">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="a49c4-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 





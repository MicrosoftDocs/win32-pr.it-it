---
description: Fornisce informazioni aggiuntive da utilizzare con il metodo ExportReferencePoint della \_ classe VirtualSystemReferencePointService di MSVM.
ms.assetid: 4897fad4-3a3f-47bc-837d-2e36434b3fab
title: Classe Msvm_VirtualSystemReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportSettingData
- Msvm_VirtualSystemReferencePointExportSettingData.BaseReferencePoint
- Msvm_VirtualSystemReferencePointExportSettingData.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65fc16f409fd79782ec4a91f223dfc754563f8bb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104058452"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a><span data-ttu-id="c8b80-103">\_Classe MSVM VirtualSystemReferencePointExportSettingData</span><span class="sxs-lookup"><span data-stu-id="c8b80-103">Msvm\_VirtualSystemReferencePointExportSettingData class</span></span>

<span data-ttu-id="c8b80-104">Fornisce informazioni aggiuntive da utilizzare con il metodo [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) della classe [**\_ VirtualSystemReferencePointService di MSVM**](msvm-virtualsystemreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="c8b80-104">Provides additional information to be used with the [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="c8b80-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c8b80-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b80-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8b80-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointExportSettingData : CIM_SettingData
{
  String BaseReferencePoint;
  String DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="c8b80-107">Members</span><span class="sxs-lookup"><span data-stu-id="c8b80-107">Members</span></span>

<span data-ttu-id="c8b80-108">La **classe \_ VirtualSystemReferencePointExportSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c8b80-108">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c8b80-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c8b80-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8b80-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c8b80-110">Properties</span></span>

<span data-ttu-id="c8b80-111">La **classe \_ VirtualSystemReferencePointExportSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c8b80-111">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8b80-112">**BaseReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="c8b80-112">**BaseReferencePoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b80-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c8b80-113">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="c8b80-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c8b80-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8b80-115">Percorso del punto di riferimento di base rispetto al quale eseguire l'esportazione.</span><span class="sxs-lookup"><span data-stu-id="c8b80-115">Path of the base reference point with respect to which export should be performed.</span></span>

</dd> <dt>

<span data-ttu-id="c8b80-116">**DisksToExport**</span><span class="sxs-lookup"><span data-stu-id="c8b80-116">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b80-117">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c8b80-117">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="c8b80-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c8b80-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8b80-119">ID dell'istanza WMI dei dischi per i quali è necessario esportare i dati.</span><span class="sxs-lookup"><span data-stu-id="c8b80-119">WMI instance IDs of the disks for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8b80-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8b80-120">Requirements</span></span>



| <span data-ttu-id="c8b80-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8b80-121">Requirement</span></span> | <span data-ttu-id="c8b80-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c8b80-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b80-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8b80-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b80-124">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c8b80-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c8b80-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8b80-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b80-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c8b80-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c8b80-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c8b80-127">Namespace</span></span><br/>                | <span data-ttu-id="c8b80-128">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c8b80-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c8b80-129">MOF</span><span class="sxs-lookup"><span data-stu-id="c8b80-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8b80-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8b80-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8b80-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c8b80-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8b80-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c8b80-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c8b80-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8b80-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b80-134">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="c8b80-134">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 





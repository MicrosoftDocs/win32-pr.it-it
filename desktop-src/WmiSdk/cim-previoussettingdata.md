---
description: Associazione tra un sistema virtuale e i dati di impostazione dello snapshot che è l'elemento padre del sistema virtuale.
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: Classe CIM_PreviousSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 4422d590714b82120b610dc4eeb9377a385519d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326971"
---
# <a name="cim_previoussettingdata-class"></a><span data-ttu-id="d4f43-103">CIM \_ PreviousSettingData (classe)</span><span class="sxs-lookup"><span data-stu-id="d4f43-103">CIM\_PreviousSettingData class</span></span>

<span data-ttu-id="d4f43-104">Associazione tra un sistema virtuale e i dati di impostazione dello snapshot che è l'elemento padre del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="d4f43-104">An association between a virtual system and the setting data of the snapshot which is the parent to the virtual system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4f43-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="d4f43-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d4f43-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d4f43-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d4f43-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d4f43-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f43-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4f43-108">Syntax</span></span>

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a><span data-ttu-id="d4f43-109">Members</span><span class="sxs-lookup"><span data-stu-id="d4f43-109">Members</span></span>

<span data-ttu-id="d4f43-110">La classe **CIM \_ PreviousSettingData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d4f43-110">The **CIM\_PreviousSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d4f43-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d4f43-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d4f43-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d4f43-112">Properties</span></span>

<span data-ttu-id="d4f43-113">La classe **CIM \_ PreviousSettingData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d4f43-113">The **CIM\_PreviousSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4f43-114">**PreviousObject**</span><span class="sxs-lookup"><span data-stu-id="d4f43-114">**PreviousObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4f43-115">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="d4f43-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d4f43-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d4f43-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4f43-117">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="d4f43-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d4f43-118">I dati dell'impostazione dello snapshot padre di questo computer.</span><span class="sxs-lookup"><span data-stu-id="d4f43-118">The snapshot setting data that is the parent of this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="d4f43-119">**Destinazione**</span><span class="sxs-lookup"><span data-stu-id="d4f43-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4f43-120">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="d4f43-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d4f43-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d4f43-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4f43-122">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="d4f43-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d4f43-123">Sistema del computer che era la destinazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d4f43-123">The computer system that was the target of the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4f43-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4f43-124">Requirements</span></span>



| <span data-ttu-id="d4f43-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4f43-125">Requirement</span></span> | <span data-ttu-id="d4f43-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d4f43-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="d4f43-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d4f43-127">Namespace</span></span><br/> | <span data-ttu-id="d4f43-128">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d4f43-128">Root\\CIMV2</span></span><br/> |



 

 





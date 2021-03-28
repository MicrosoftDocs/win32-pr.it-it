---
description: Questa classe è la classe del tipo di evento per gli eventi di i/o divisi. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 0eb1f712-8b1c-4de1-b701-5c7dbabb0f55
title: Classe SplitIo_Info
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo_Info
- SplitIo_Info.ParentIrp
- SplitIo_Info.ChildIrp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 469c8f04664f72b88e5a4378cb318b52f32fba24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884625"
---
# <a name="splitio_info-class"></a><span data-ttu-id="d3db0-104">\_Classe SplitIo info</span><span class="sxs-lookup"><span data-stu-id="d3db0-104">SplitIo\_Info class</span></span>

<span data-ttu-id="d3db0-105">Questa classe è la classe del tipo di evento per gli eventi di i/o divisi.</span><span class="sxs-lookup"><span data-stu-id="d3db0-105">This class is the event type class for split IO events.</span></span>

<span data-ttu-id="d3db0-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="d3db0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3db0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3db0-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"VolMgr"}]
class SplitIo_Info : SplitIo
{
  uint32 ParentIrp;
  uint32 ChildIrp;
};
```

## <a name="members"></a><span data-ttu-id="d3db0-108">Members</span><span class="sxs-lookup"><span data-stu-id="d3db0-108">Members</span></span>

<span data-ttu-id="d3db0-109">La classe **SplitIo \_ info** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d3db0-109">The **SplitIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="d3db0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d3db0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d3db0-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d3db0-111">Properties</span></span>

<span data-ttu-id="d3db0-112">La classe **SplitIo \_ info** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3db0-112">The **SplitIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d3db0-113">**ChildIrp**</span><span class="sxs-lookup"><span data-stu-id="d3db0-113">**ChildIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3db0-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d3db0-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3db0-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3db0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3db0-116">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="d3db0-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d3db0-117">Pacchetto di richieste IO figlio.</span><span class="sxs-lookup"><span data-stu-id="d3db0-117">Child IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="d3db0-118">**ParentIrp**</span><span class="sxs-lookup"><span data-stu-id="d3db0-118">**ParentIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3db0-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d3db0-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3db0-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3db0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3db0-121">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="d3db0-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d3db0-122">Pacchetto della richiesta i/o padre.</span><span class="sxs-lookup"><span data-stu-id="d3db0-122">Parent IO request packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3db0-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3db0-123">Remarks</span></span>

<span data-ttu-id="d3db0-124">Indica che il gestore del volume ha suddiviso l'IRP in due IRP.</span><span class="sxs-lookup"><span data-stu-id="d3db0-124">Indicates that the volume manager split the IRP into two IRPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3db0-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3db0-125">Requirements</span></span>



| <span data-ttu-id="d3db0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3db0-126">Requirement</span></span> | <span data-ttu-id="d3db0-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d3db0-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d3db0-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3db0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d3db0-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3db0-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d3db0-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3db0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d3db0-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3db0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





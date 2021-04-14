---
description: Questa classe è la classe del tipo di evento per gli eventi del registro di sistema. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 93031f3e-963f-46a6-9355-988eefd94836
title: Classe Registry_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V0_TypeGroup1
- Registry_V0_TypeGroup1.Status
- Registry_V0_TypeGroup1.KeyHandle
- Registry_V0_TypeGroup1.ElapsedTime
- Registry_V0_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9a72a0d6ddfe5e441b21dff4ba58fa3bb37457a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977631"
---
# <a name="registry_v0_typegroup1-class"></a><span data-ttu-id="0dec9-104">\_ \_ Classe TypeGroup1 del registro di sistema V0</span><span class="sxs-lookup"><span data-stu-id="0dec9-104">Registry\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="0dec9-105">Questa classe è la classe del tipo di evento per gli eventi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0dec9-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="0dec9-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="0dec9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dec9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0dec9-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush"}]
class Registry_V0_TypeGroup1 : Registry_V0
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="0dec9-108">Members</span><span class="sxs-lookup"><span data-stu-id="0dec9-108">Members</span></span>

<span data-ttu-id="0dec9-109">La **classe \_ \_ TypeGroup1 del registro di sistema V0** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0dec9-109">The **Registry\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="0dec9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0dec9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0dec9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0dec9-111">Properties</span></span>

<span data-ttu-id="0dec9-112">La **classe \_ \_ TypeGroup1 del registro di sistema V0** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0dec9-112">The **Registry\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0dec9-113">ElapsedTime</span><span class="sxs-lookup"><span data-stu-id="0dec9-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dec9-114">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="0dec9-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="0dec9-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0dec9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0dec9-116">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="0dec9-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="0dec9-117">Tempo trascorso per l'operazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0dec9-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="0dec9-118">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="0dec9-118">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dec9-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dec9-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dec9-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0dec9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0dec9-121">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="0dec9-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0dec9-122">Handle per la chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0dec9-122">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="0dec9-123">KeyName</span><span class="sxs-lookup"><span data-stu-id="0dec9-123">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dec9-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0dec9-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0dec9-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0dec9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0dec9-126">Qualificatori: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="0dec9-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="0dec9-127">nome della chiave del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0dec9-127">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="0dec9-128">Stato</span><span class="sxs-lookup"><span data-stu-id="0dec9-128">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0dec9-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0dec9-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0dec9-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0dec9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0dec9-131">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="0dec9-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="0dec9-132">Valore NTSTATUS dell'operazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0dec9-132">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0dec9-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0dec9-133">Requirements</span></span>



| <span data-ttu-id="0dec9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dec9-134">Requirement</span></span> | <span data-ttu-id="0dec9-135">Valore</span><span class="sxs-lookup"><span data-stu-id="0dec9-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0dec9-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0dec9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0dec9-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0dec9-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0dec9-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0dec9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0dec9-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0dec9-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0dec9-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0dec9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dec9-141">**Registro di sistema \_ V0**</span><span class="sxs-lookup"><span data-stu-id="0dec9-141">**Registry\_V0**</span></span>](registry-v0.md)
</dt> </dl>

 

 





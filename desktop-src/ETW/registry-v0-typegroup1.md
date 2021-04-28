---
description: 'Registry_V0_TypeGroup1: questa classe è la classe del tipo di evento per gli eventi del Registro di sistema. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 93031f3e-963f-46a6-9355-988eefd94836
title: Registry_V0_TypeGroup1 classe
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
ms.openlocfilehash: 86f6d695afa2e05c87a076cf88ed8023e9416beb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106189"
---
# <a name="registry_v0_typegroup1-class"></a><span data-ttu-id="36f49-104">Classe \_ \_ TypeGroup1 registry V0</span><span class="sxs-lookup"><span data-stu-id="36f49-104">Registry\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="36f49-105">Questa classe è la classe del tipo di evento per gli eventi del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="36f49-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="36f49-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="36f49-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f49-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36f49-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="36f49-108">Members</span><span class="sxs-lookup"><span data-stu-id="36f49-108">Members</span></span>

<span data-ttu-id="36f49-109">La **classe \_ \_ TypeGroup1 Registry V0** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="36f49-109">The **Registry\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="36f49-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="36f49-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36f49-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="36f49-111">Properties</span></span>

<span data-ttu-id="36f49-112">La **classe \_ \_ TypeGroup1 Registry V0** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="36f49-112">The **Registry\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36f49-113">ElapsedTime</span><span class="sxs-lookup"><span data-stu-id="36f49-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f49-114">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="36f49-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="36f49-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36f49-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f49-116">Qualificatori: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="36f49-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="36f49-117">Tempo trascorso dell'operazione del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="36f49-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="36f49-118">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="36f49-118">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f49-119">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="36f49-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36f49-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36f49-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f49-121">Qualificatori: WmiDataId(2), Pointer</span><span class="sxs-lookup"><span data-stu-id="36f49-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="36f49-122">Handle per la chiave del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="36f49-122">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="36f49-123">KeyName</span><span class="sxs-lookup"><span data-stu-id="36f49-123">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f49-124">Tipo di dati: **string**</span><span class="sxs-lookup"><span data-stu-id="36f49-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36f49-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36f49-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f49-126">Qualificatori: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="36f49-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="36f49-127">nome della chiave del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="36f49-127">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="36f49-128">Stato</span><span class="sxs-lookup"><span data-stu-id="36f49-128">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36f49-129">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="36f49-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="36f49-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="36f49-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36f49-131">Qualificatori: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="36f49-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="36f49-132">Valore NTSTATUS dell'operazione del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="36f49-132">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36f49-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36f49-133">Requirements</span></span>



| <span data-ttu-id="36f49-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="36f49-134">Requirement</span></span> | <span data-ttu-id="36f49-135">Valore</span><span class="sxs-lookup"><span data-stu-id="36f49-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="36f49-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36f49-136">Minimum supported client</span></span><br/> | <span data-ttu-id="36f49-137">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="36f49-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="36f49-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36f49-138">Minimum supported server</span></span><br/> | <span data-ttu-id="36f49-139">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="36f49-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="36f49-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36f49-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f49-141">**Registro \_ di sistema V0**</span><span class="sxs-lookup"><span data-stu-id="36f49-141">**Registry\_V0**</span></span>](registry-v0.md)
</dt> </dl>

 

 





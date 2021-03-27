---
description: Questa classe è la classe del tipo di evento per gli eventi del registro di sistema. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 59c455a0-af7e-4fd5-9af4-07ff72ee0545
title: Classe Registry_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1_TypeGroup1
- Registry_V1_TypeGroup1.Status
- Registry_V1_TypeGroup1.KeyHandle
- Registry_V1_TypeGroup1.ElapsedTime
- Registry_V1_TypeGroup1.Index
- Registry_V1_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2cd77ad0c12769c657b4e7c23c1fe1993a248481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879514"
---
# <a name="registry_v1_typegroup1-class"></a><span data-ttu-id="4ec21-104">\_ \_ Classe TypeGroup1 del registro di sistema V1</span><span class="sxs-lookup"><span data-stu-id="4ec21-104">Registry\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="4ec21-105">Questa classe è la classe del tipo di evento per gli eventi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4ec21-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="4ec21-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="4ec21-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ec21-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ec21-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "RunDown"}]
class Registry_V1_TypeGroup1 : Registry
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  uint32 Index;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="4ec21-108">Members</span><span class="sxs-lookup"><span data-stu-id="4ec21-108">Members</span></span>

<span data-ttu-id="4ec21-109">La **classe \_ \_ TypeGroup1 del registro di sistema V1** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4ec21-109">The **Registry\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="4ec21-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4ec21-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ec21-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4ec21-111">Properties</span></span>

<span data-ttu-id="4ec21-112">Per la classe **\_ \_ TypeGroup1 del registro di sistema V1** sono presenti queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4ec21-112">The **Registry\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ec21-113">ElapsedTime</span><span class="sxs-lookup"><span data-stu-id="4ec21-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec21-114">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="4ec21-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ec21-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4ec21-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ec21-116">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="4ec21-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="4ec21-117">Tempo trascorso per l'operazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4ec21-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="4ec21-118">Indice</span><span class="sxs-lookup"><span data-stu-id="4ec21-118">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec21-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ec21-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ec21-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4ec21-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ec21-121">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="4ec21-121">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="4ec21-122">Indice della sottochiave per l'operazione del registro di sistema (ad esempio EnumerateKey).</span><span class="sxs-lookup"><span data-stu-id="4ec21-122">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="4ec21-123">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="4ec21-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec21-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ec21-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ec21-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4ec21-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ec21-126">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="4ec21-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4ec21-127">Handle per la chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4ec21-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="4ec21-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="4ec21-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec21-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4ec21-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ec21-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4ec21-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ec21-131">Qualificatori: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="4ec21-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="4ec21-132">nome della chiave del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4ec21-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="4ec21-133">Stato</span><span class="sxs-lookup"><span data-stu-id="4ec21-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec21-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ec21-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ec21-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4ec21-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ec21-136">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="4ec21-136">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4ec21-137">Valore NTSTATUS dell'operazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4ec21-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ec21-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ec21-138">Requirements</span></span>



| <span data-ttu-id="4ec21-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ec21-139">Requirement</span></span> | <span data-ttu-id="4ec21-140">Valore</span><span class="sxs-lookup"><span data-stu-id="4ec21-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4ec21-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ec21-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4ec21-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4ec21-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4ec21-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ec21-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4ec21-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4ec21-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4ec21-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ec21-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec21-146">**Registro**</span><span class="sxs-lookup"><span data-stu-id="4ec21-146">**Registry**</span></span>](registry.md)
</dt> <dt>

[<span data-ttu-id="4ec21-147">**Registro di sistema \_ V1**</span><span class="sxs-lookup"><span data-stu-id="4ec21-147">**Registry\_V1**</span></span>](registry-v1.md)
</dt> </dl>

 

 





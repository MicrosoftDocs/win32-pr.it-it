---
description: Questa classe è la classe del tipo di evento per gli eventi del registro di sistema. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 8d0e9d97-3837-46da-a217-13e943580352
title: Classe Registry_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_TypeGroup1
- Registry_TypeGroup1.InitialTime
- Registry_TypeGroup1.Status
- Registry_TypeGroup1.Index
- Registry_TypeGroup1.KeyHandle
- Registry_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bfbf0157141473be4cc2460659912dc662ef7c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977815"
---
# <a name="registry_typegroup1-class"></a><span data-ttu-id="4e089-104">Classe TypeGroup1 del registro di sistema \_</span><span class="sxs-lookup"><span data-stu-id="4e089-104">Registry\_TypeGroup1 class</span></span>

<span data-ttu-id="4e089-105">Questa classe è la classe del tipo di evento per gli eventi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4e089-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="4e089-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="4e089-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e089-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e089-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "KCBCreate", "KCBDelete", "KCBRundownBegin", "KCBRundownEnd", "Virtualize", "Close"}]
class Registry_TypeGroup1 : Registry
{
  sint64 InitialTime;
  uint32 Status;
  uint32 Index;
  uint32 KeyHandle;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="4e089-108">Members</span><span class="sxs-lookup"><span data-stu-id="4e089-108">Members</span></span>

<span data-ttu-id="4e089-109">La **classe \_ TypeGroup1 del registro di sistema** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4e089-109">The **Registry\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="4e089-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e089-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e089-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e089-111">Properties</span></span>

<span data-ttu-id="4e089-112">La **classe \_ TypeGroup1 del registro di sistema** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4e089-112">The **Registry\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e089-113">Indice</span><span class="sxs-lookup"><span data-stu-id="4e089-113">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e089-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e089-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e089-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e089-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e089-116">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="4e089-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="4e089-117">Indice della sottochiave per l'operazione del registro di sistema (ad esempio EnumerateKey).</span><span class="sxs-lookup"><span data-stu-id="4e089-117">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="4e089-118">InitialTime</span><span class="sxs-lookup"><span data-stu-id="4e089-118">InitialTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e089-119">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="4e089-119">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="4e089-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e089-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e089-121">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="4e089-121">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="4e089-122">Ora iniziale dell'operazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4e089-122">Initial time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="4e089-123">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="4e089-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e089-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e089-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e089-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e089-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e089-126">Qualificatori: WmiDataId (4), puntatore</span><span class="sxs-lookup"><span data-stu-id="4e089-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4e089-127">Handle per la chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4e089-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="4e089-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="4e089-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e089-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4e089-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e089-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e089-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e089-131">Qualificatori: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="4e089-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="4e089-132">nome della chiave del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4e089-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="4e089-133">Stato</span><span class="sxs-lookup"><span data-stu-id="4e089-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e089-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e089-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e089-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e089-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e089-136">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="4e089-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4e089-137">Valore NTSTATUS dell'operazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4e089-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e089-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e089-138">Requirements</span></span>



| <span data-ttu-id="4e089-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e089-139">Requirement</span></span> | <span data-ttu-id="4e089-140">Valore</span><span class="sxs-lookup"><span data-stu-id="4e089-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4e089-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e089-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4e089-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e089-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4e089-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e089-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4e089-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e089-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e089-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e089-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e089-146">**Registro**</span><span class="sxs-lookup"><span data-stu-id="4e089-146">**Registry**</span></span>](registry.md)
</dt> </dl>

 

 





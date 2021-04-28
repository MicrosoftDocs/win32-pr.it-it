---
description: 'Registry_V1_TypeGroup1: questa classe è la classe del tipo di evento per gli eventi del Registro di sistema. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 59c455a0-af7e-4fd5-9af4-07ff72ee0545
title: Registry_V1_TypeGroup1 classe
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
ms.openlocfilehash: ab0326f92d1b084f471f3dc1b57322f69aa645fd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106159"
---
# <a name="registry_v1_typegroup1-class"></a><span data-ttu-id="4b60a-104">Classe TypeGroup1 del Registro di \_ \_ sistema V1</span><span class="sxs-lookup"><span data-stu-id="4b60a-104">Registry\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="4b60a-105">Questa classe è la classe del tipo di evento per gli eventi del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4b60a-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="4b60a-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="4b60a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b60a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b60a-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="4b60a-108">Members</span><span class="sxs-lookup"><span data-stu-id="4b60a-108">Members</span></span>

<span data-ttu-id="4b60a-109">La **classe \_ \_ TypeGroup1 Registry V1** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4b60a-109">The **Registry\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="4b60a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b60a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b60a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b60a-111">Properties</span></span>

<span data-ttu-id="4b60a-112">La **classe \_ \_ TypeGroup1 Registry V1** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4b60a-112">The **Registry\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b60a-113">ElapsedTime</span><span class="sxs-lookup"><span data-stu-id="4b60a-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b60a-114">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="4b60a-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="4b60a-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b60a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b60a-116">Qualificatori: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="4b60a-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="4b60a-117">Tempo trascorso dell'operazione del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4b60a-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="4b60a-118">Indice</span><span class="sxs-lookup"><span data-stu-id="4b60a-118">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b60a-119">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4b60a-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b60a-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b60a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b60a-121">Qualificatori: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="4b60a-121">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="4b60a-122">Indice della sottochiave per l'operazione del Registro di sistema, ad esempio EnumerateKey.</span><span class="sxs-lookup"><span data-stu-id="4b60a-122">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="4b60a-123">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="4b60a-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b60a-124">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4b60a-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b60a-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b60a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b60a-126">Qualificatori: WmiDataId(2), Pointer</span><span class="sxs-lookup"><span data-stu-id="4b60a-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4b60a-127">Handle per la chiave del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4b60a-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="4b60a-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="4b60a-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b60a-129">Tipo di dati: **string**</span><span class="sxs-lookup"><span data-stu-id="4b60a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b60a-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b60a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b60a-131">Qualificatori: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="4b60a-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="4b60a-132">nome della chiave del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4b60a-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="4b60a-133">Stato</span><span class="sxs-lookup"><span data-stu-id="4b60a-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b60a-134">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4b60a-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4b60a-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b60a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b60a-136">Qualificatori: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="4b60a-136">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4b60a-137">Valore NTSTATUS dell'operazione del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4b60a-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b60a-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b60a-138">Requirements</span></span>



| <span data-ttu-id="4b60a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b60a-139">Requirement</span></span> | <span data-ttu-id="4b60a-140">Valore</span><span class="sxs-lookup"><span data-stu-id="4b60a-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4b60a-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b60a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4b60a-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b60a-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4b60a-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b60a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4b60a-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b60a-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4b60a-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b60a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b60a-146">**Registro**</span><span class="sxs-lookup"><span data-stu-id="4b60a-146">**Registry**</span></span>](registry.md)
</dt> <dt>

[<span data-ttu-id="4b60a-147">**Registro \_ di sistema V1**</span><span class="sxs-lookup"><span data-stu-id="4b60a-147">**Registry\_V1**</span></span>](registry-v1.md)
</dt> </dl>

 

 





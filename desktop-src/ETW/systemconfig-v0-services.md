---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: Classe SystemConfig_V0_Services
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Services
- SystemConfig_V0_Services.ServiceName
- SystemConfig_V0_Services.DisplayName
- SystemConfig_V0_Services.ProcessName
- SystemConfig_V0_Services.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6c061c6a0c4cbb3e807bcb3418155b1194fcfa28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349321"
---
# <a name="systemconfig_v0_services-class"></a><span data-ttu-id="645f4-103">\_ \_ Classe dei servizi SystemConfig V0</span><span class="sxs-lookup"><span data-stu-id="645f4-103">SystemConfig\_V0\_Services class</span></span>

<span data-ttu-id="645f4-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="645f4-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="645f4-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="645f4-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="645f4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="645f4-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_V0_Services : SystemConfig_V0
{
  char16 ServiceName[];
  char16 DisplayName[];
  char16 ProcessName[];
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="645f4-107">Members</span><span class="sxs-lookup"><span data-stu-id="645f4-107">Members</span></span>

<span data-ttu-id="645f4-108">La classe dei **\_ \_ Servizi SystemConfig V0** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="645f4-108">The **SystemConfig\_V0\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="645f4-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="645f4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="645f4-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="645f4-110">Properties</span></span>

<span data-ttu-id="645f4-111">La **classe \_ \_ dei servizi SystemConfig V0** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="645f4-111">The **SystemConfig\_V0\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="645f4-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="645f4-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645f4-113">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="645f4-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="645f4-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="645f4-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="645f4-115">Qualificatori: **WmiDataId** (2), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="645f4-115">Qualifiers: **WmiDataId** (2), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="645f4-116">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="645f4-116">Display name of the service.</span></span> <span data-ttu-id="645f4-117">Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="645f4-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="645f4-118">Tuttavia, i nomi visualizzati vengono sempre confrontati senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="645f4-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="645f4-119">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="645f4-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645f4-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="645f4-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="645f4-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="645f4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="645f4-122">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="645f4-122">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="645f4-123">Identificatore del processo in cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="645f4-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="645f4-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="645f4-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645f4-125">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="645f4-125">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="645f4-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="645f4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="645f4-127">Qualificatori: **WmiDataId** (3), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="645f4-127">Qualifiers: **WmiDataId** (3), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="645f4-128">Nome del processo in cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="645f4-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="645f4-129">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="645f4-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="645f4-130">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="645f4-130">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="645f4-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="645f4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="645f4-132">Qualificatori: **WmiDataId** (1), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="645f4-132">Qualifiers: **WmiDataId** (1), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="645f4-133">Identificatore univoco del servizio.</span><span class="sxs-lookup"><span data-stu-id="645f4-133">Unique identifier of the service.</span></span> <span data-ttu-id="645f4-134">L'identificatore fornisce un'indicazione delle funzionalità fornite dal servizio.</span><span class="sxs-lookup"><span data-stu-id="645f4-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="645f4-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="645f4-135">Requirements</span></span>



| <span data-ttu-id="645f4-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="645f4-136">Requirement</span></span> | <span data-ttu-id="645f4-137">Valore</span><span class="sxs-lookup"><span data-stu-id="645f4-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="645f4-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="645f4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="645f4-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="645f4-139">None supported</span></span><br/>                            |
| <span data-ttu-id="645f4-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="645f4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="645f4-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="645f4-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="645f4-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="645f4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="645f4-143">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="645f4-143">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 





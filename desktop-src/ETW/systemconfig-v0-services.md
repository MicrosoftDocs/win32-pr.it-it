---
description: 'SystemConfig_V0_Services: questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.'
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: SystemConfig_V0_Services classe
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
ms.openlocfilehash: b69ca7cf4ee4e16a5fbcb6a5f10c659f713ab458
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105929"
---
# <a name="systemconfig_v0_services-class"></a><span data-ttu-id="7e084-103">Classe SystemConfig \_ V0 \_ Services</span><span class="sxs-lookup"><span data-stu-id="7e084-103">SystemConfig\_V0\_Services class</span></span>

<span data-ttu-id="7e084-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="7e084-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="7e084-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="7e084-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e084-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e084-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="7e084-107">Members</span><span class="sxs-lookup"><span data-stu-id="7e084-107">Members</span></span>

<span data-ttu-id="7e084-108">La **classe SystemConfig \_ V0 \_ Services** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7e084-108">The **SystemConfig\_V0\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="7e084-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7e084-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e084-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7e084-110">Properties</span></span>

<span data-ttu-id="7e084-111">La **classe SystemConfig \_ V0 \_ Services** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7e084-111">The **SystemConfig\_V0\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e084-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="7e084-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e084-113">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="7e084-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="7e084-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7e084-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e084-115">Qualificatori: **WmiDataId** (2), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="7e084-115">Qualifiers: **WmiDataId** (2), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="7e084-116">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="7e084-116">Display name of the service.</span></span> <span data-ttu-id="7e084-117">Il nome viene mantenuto senza distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="7e084-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="7e084-118">Tuttavia, i nomi visualizzati vengono sempre confrontati senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="7e084-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="7e084-119">**Processid**</span><span class="sxs-lookup"><span data-stu-id="7e084-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e084-120">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="7e084-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e084-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7e084-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e084-122">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="7e084-122">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="7e084-123">Identificatore del processo in cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="7e084-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="7e084-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="7e084-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e084-125">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="7e084-125">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="7e084-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7e084-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e084-127">Qualificatori: **WmiDataId** (3), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="7e084-127">Qualifiers: **WmiDataId** (3), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="7e084-128">Nome del processo in cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="7e084-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="7e084-129">**Servicename**</span><span class="sxs-lookup"><span data-stu-id="7e084-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e084-130">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="7e084-130">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="7e084-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7e084-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e084-132">Qualificatori: **WmiDataId** (1), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="7e084-132">Qualifiers: **WmiDataId** (1), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="7e084-133">Identificatore univoco del servizio.</span><span class="sxs-lookup"><span data-stu-id="7e084-133">Unique identifier of the service.</span></span> <span data-ttu-id="7e084-134">L'identificatore fornisce un'indicazione della funzionalità fornita dal servizio.</span><span class="sxs-lookup"><span data-stu-id="7e084-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e084-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e084-135">Requirements</span></span>



| <span data-ttu-id="7e084-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e084-136">Requirement</span></span> | <span data-ttu-id="7e084-137">Valore</span><span class="sxs-lookup"><span data-stu-id="7e084-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e084-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e084-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7e084-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7e084-139">None supported</span></span><br/>                            |
| <span data-ttu-id="7e084-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e084-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7e084-141">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e084-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e084-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e084-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e084-143">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="7e084-143">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 





---
description: 'SystemConfig_Services: questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.'
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: SystemConfig_Services classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 754b0e10c3882911c6e91fc2590c11739c3f7531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106059"
---
# <a name="systemconfig_services-class"></a><span data-ttu-id="f79f8-103">Classe SystemConfig \_ Services</span><span class="sxs-lookup"><span data-stu-id="f79f8-103">SystemConfig\_Services class</span></span>

<span data-ttu-id="f79f8-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="f79f8-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="f79f8-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="f79f8-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f79f8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f79f8-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a><span data-ttu-id="f79f8-107">Members</span><span class="sxs-lookup"><span data-stu-id="f79f8-107">Members</span></span>

<span data-ttu-id="f79f8-108">La **classe SystemConfig \_ Services** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f79f8-108">The **SystemConfig\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="f79f8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f79f8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f79f8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f79f8-110">Properties</span></span>

<span data-ttu-id="f79f8-111">La **classe SystemConfig \_ Services** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f79f8-111">The **SystemConfig\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f79f8-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="f79f8-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f79f8-113">Tipo di dati: **matrice di** stringhe</span><span class="sxs-lookup"><span data-stu-id="f79f8-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f79f8-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f79f8-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f79f8-115">Qualificatori: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span><span class="sxs-lookup"><span data-stu-id="f79f8-115">Qualifiers: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="f79f8-116">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="f79f8-116">Display name of the service.</span></span> <span data-ttu-id="f79f8-117">Il nome viene mantenuto senza distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="f79f8-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="f79f8-118">Tuttavia, i nomi visualizzati vengono sempre confrontati senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f79f8-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="f79f8-119">**Processid**</span><span class="sxs-lookup"><span data-stu-id="f79f8-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f79f8-120">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f79f8-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f79f8-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f79f8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f79f8-122">Qualificatori: **WmiDataId** (1), **Format("x")**</span><span class="sxs-lookup"><span data-stu-id="f79f8-122">Qualifiers: **WmiDataId** (1), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="f79f8-123">Identificatore del processo in cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="f79f8-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="f79f8-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="f79f8-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f79f8-125">Tipo di dati: **matrice di** stringhe</span><span class="sxs-lookup"><span data-stu-id="f79f8-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f79f8-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f79f8-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f79f8-127">Qualificatori: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span><span class="sxs-lookup"><span data-stu-id="f79f8-127">Qualifiers: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="f79f8-128">Nome del processo in cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="f79f8-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="f79f8-129">**Servicename**</span><span class="sxs-lookup"><span data-stu-id="f79f8-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f79f8-130">Tipo di dati: **matrice di** stringhe</span><span class="sxs-lookup"><span data-stu-id="f79f8-130">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f79f8-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f79f8-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f79f8-132">Qualificatori: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span><span class="sxs-lookup"><span data-stu-id="f79f8-132">Qualifiers: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="f79f8-133">Identificatore univoco del servizio.</span><span class="sxs-lookup"><span data-stu-id="f79f8-133">Unique identifier of the service.</span></span> <span data-ttu-id="f79f8-134">L'identificatore fornisce un'indicazione della funzionalità fornita dal servizio.</span><span class="sxs-lookup"><span data-stu-id="f79f8-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> <dt>

<span data-ttu-id="f79f8-135">**ServiceState**</span><span class="sxs-lookup"><span data-stu-id="f79f8-135">**ServiceState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f79f8-136">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f79f8-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f79f8-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f79f8-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f79f8-138">Qualificatori: **WmiDataId** (2), **Format("x")**</span><span class="sxs-lookup"><span data-stu-id="f79f8-138">Qualifiers: **WmiDataId** (2), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="f79f8-139">Stato corrente del servizio.</span><span class="sxs-lookup"><span data-stu-id="f79f8-139">Current state of the service.</span></span> <span data-ttu-id="f79f8-140">Per i valori possibili, vedere **il membro dwCurrentState** di **SERVICE STATUS \_ \_ PROCESS**.</span><span class="sxs-lookup"><span data-stu-id="f79f8-140">For possible values, see the **dwCurrentState** member of **SERVICE\_STATUS\_PROCESS**.</span></span>

</dd> <dt>

<span data-ttu-id="f79f8-141">**SubProcessTag**</span><span class="sxs-lookup"><span data-stu-id="f79f8-141">**SubProcessTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f79f8-142">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f79f8-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f79f8-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f79f8-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f79f8-144">Qualificatori: **WmiDataId** (3), **Format("x")**</span><span class="sxs-lookup"><span data-stu-id="f79f8-144">Qualifiers: **WmiDataId** (3), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="f79f8-145">Identifica il servizio.</span><span class="sxs-lookup"><span data-stu-id="f79f8-145">Identifies the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f79f8-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f79f8-146">Requirements</span></span>



| <span data-ttu-id="f79f8-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f79f8-147">Requirement</span></span> | <span data-ttu-id="f79f8-148">Valore</span><span class="sxs-lookup"><span data-stu-id="f79f8-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f79f8-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f79f8-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f79f8-150">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f79f8-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f79f8-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f79f8-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f79f8-152">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f79f8-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f79f8-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f79f8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f79f8-154">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="f79f8-154">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 





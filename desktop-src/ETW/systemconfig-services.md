---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: Classe SystemConfig_Services
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
ms.openlocfilehash: 97b4d2a56f2ed739403681875e0be4d9e21481ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977471"
---
# <a name="systemconfig_services-class"></a><span data-ttu-id="0c0f9-103">\_Classe dei servizi SystemConfig</span><span class="sxs-lookup"><span data-stu-id="0c0f9-103">SystemConfig\_Services class</span></span>

<span data-ttu-id="0c0f9-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="0c0f9-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c0f9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c0f9-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="0c0f9-107">Members</span><span class="sxs-lookup"><span data-stu-id="0c0f9-107">Members</span></span>

<span data-ttu-id="0c0f9-108">La classe dei **\_ Servizi SystemConfig** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0c0f9-108">The **SystemConfig\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="0c0f9-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c0f9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c0f9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c0f9-110">Properties</span></span>

<span data-ttu-id="0c0f9-111">La **classe \_ dei servizi SystemConfig** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-111">The **SystemConfig\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c0f9-112">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f9-113">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c0f9-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c0f9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c0f9-115">Qualificatori: **WmiDataId** (5), **StringTermination ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-115">Qualifiers: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="0c0f9-116">Nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-116">Display name of the service.</span></span> <span data-ttu-id="0c0f9-117">Il nome viene mantenuto con la distinzione tra maiuscole e minuscole in Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="0c0f9-118">Tuttavia, i nomi visualizzati vengono sempre confrontati senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="0c0f9-119">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f9-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c0f9-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c0f9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c0f9-122">Qualificatori: **WmiDataId** (1), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-122">Qualifiers: **WmiDataId** (1), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="0c0f9-123">Identificatore del processo in cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="0c0f9-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f9-125">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c0f9-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c0f9-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c0f9-127">Qualificatori: **WmiDataId** (6), **StringTermination ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-127">Qualifiers: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="0c0f9-128">Nome del processo in cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="0c0f9-129">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f9-130">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-130">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c0f9-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c0f9-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c0f9-132">Qualificatori: **WmiDataId** (4), **StringTermination ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-132">Qualifiers: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="0c0f9-133">Identificatore univoco del servizio.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-133">Unique identifier of the service.</span></span> <span data-ttu-id="0c0f9-134">L'identificatore fornisce un'indicazione delle funzionalità fornite dal servizio.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> <dt>

<span data-ttu-id="0c0f9-135">**ServiceState**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-135">**ServiceState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f9-136">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c0f9-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c0f9-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c0f9-138">Qualificatori: **WmiDataId** (2), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-138">Qualifiers: **WmiDataId** (2), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="0c0f9-139">Stato corrente del servizio.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-139">Current state of the service.</span></span> <span data-ttu-id="0c0f9-140">Per i valori possibili, vedere il membro **dwCurrentState** del **processo di \_ stato \_ del servizio**.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-140">For possible values, see the **dwCurrentState** member of **SERVICE\_STATUS\_PROCESS**.</span></span>

</dd> <dt>

<span data-ttu-id="0c0f9-141">**SubProcessTag**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-141">**SubProcessTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c0f9-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c0f9-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c0f9-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c0f9-144">Qualificatori: **WmiDataId** (3), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-144">Qualifiers: **WmiDataId** (3), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="0c0f9-145">Identifica il servizio.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-145">Identifies the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c0f9-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c0f9-146">Requirements</span></span>



| <span data-ttu-id="0c0f9-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c0f9-147">Requirement</span></span> | <span data-ttu-id="0c0f9-148">Valore</span><span class="sxs-lookup"><span data-stu-id="0c0f9-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0c0f9-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c0f9-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0c0f9-150">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c0f9-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0c0f9-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c0f9-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0c0f9-152">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c0f9-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c0f9-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c0f9-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c0f9-154">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="0c0f9-154">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 





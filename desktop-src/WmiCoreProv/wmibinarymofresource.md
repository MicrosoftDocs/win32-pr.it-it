---
description: Il provider di classi WDM definisce la classe WMIBinaryMofResource nello \\ \\ spazio dei nomi WMI radice per supportare l'attività di tenere traccia dello stato dei dati nel repository WMI.
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: Classe WMIBinaryMofResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879974"
---
# <a name="wmibinarymofresource-class"></a><span data-ttu-id="c6a98-103">Classe WMIBinaryMofResource</span><span class="sxs-lookup"><span data-stu-id="c6a98-103">WMIBinaryMofResource class</span></span>

<span data-ttu-id="c6a98-104">Il provider di classi WDM definisce la classe **WMIBinaryMofResource** nello \\ \\ spazio dei nomi WMI radice per supportare l'attività di tenere traccia dello stato dei dati nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="c6a98-104">The WDM class provider defines the **WMIBinaryMofResource** class in the \\root\\wmi namespace to support the task of keeping track of the status of data in the WMI repository.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6a98-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6a98-105">Syntax</span></span>

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="c6a98-106">Members</span><span class="sxs-lookup"><span data-stu-id="c6a98-106">Members</span></span>

<span data-ttu-id="c6a98-107">La classe **WMIBinaryMofResource** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c6a98-107">The **WMIBinaryMofResource** class has these types of members:</span></span>

-   [<span data-ttu-id="c6a98-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6a98-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6a98-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6a98-109">Properties</span></span>

<span data-ttu-id="c6a98-110">La classe **WMIBinaryMofResource** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c6a98-110">The **WMIBinaryMofResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6a98-111">**HighDateTime**</span><span class="sxs-lookup"><span data-stu-id="c6a98-111">**HighDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a98-112">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6a98-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a98-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6a98-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6a98-114">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c6a98-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c6a98-115">Metà alta dell'indicatore di data e ora.</span><span class="sxs-lookup"><span data-stu-id="c6a98-115">High half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="c6a98-116">**LowDateTime**</span><span class="sxs-lookup"><span data-stu-id="c6a98-116">**LowDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a98-117">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6a98-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a98-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6a98-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6a98-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c6a98-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c6a98-120">Metà inferiore dell'indicatore di data e ora.</span><span class="sxs-lookup"><span data-stu-id="c6a98-120">Low half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="c6a98-121">**MofProcessed**</span><span class="sxs-lookup"><span data-stu-id="c6a98-121">**MofProcessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a98-122">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c6a98-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c6a98-123">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c6a98-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c6a98-124">Flag che indica se il file con estensione MOF è stato elaborato completamente.</span><span class="sxs-lookup"><span data-stu-id="c6a98-124">Flag indicating whether the .mof file was fully processed.</span></span>

</dd> <dt>

<span data-ttu-id="c6a98-125">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c6a98-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a98-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c6a98-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6a98-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6a98-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6a98-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c6a98-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c6a98-129">Nome del driver WDM abilitato con un file MOF binario compilato correttamente nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="c6a98-129">Name of the WDM enabled driver that has a binary MOF file successfully compiled in the WMI repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6a98-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6a98-130">Remarks</span></span>

<span data-ttu-id="c6a98-131">Il provider di classi WDM crea un'istanza di **WMIBinaryMofResource** per ogni driver WDM che fornisce un file MOF binario.</span><span class="sxs-lookup"><span data-stu-id="c6a98-131">The WDM class provider creates an instance of **WMIBinaryMofResource** for each WDM driver that supplies a binary MOF file.</span></span>

<span data-ttu-id="c6a98-132">Ogni volta che WMI inizializza il provider, il provider confronta il timestamp con il timestamp del file di immagine del driver.</span><span class="sxs-lookup"><span data-stu-id="c6a98-132">Whenever WMI initializes the provider, the provider compares the timestamp with the timestamp of the driver image file.</span></span> <span data-ttu-id="c6a98-133">Se i timestamp sono diversi, WMI ricompila nuovamente il file MOF.</span><span class="sxs-lookup"><span data-stu-id="c6a98-133">If the timestamps differ, WMI re-compiles the MOF file.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a98-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6a98-134">Requirements</span></span>



| <span data-ttu-id="c6a98-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6a98-135">Requirement</span></span> | <span data-ttu-id="c6a98-136">Valore</span><span class="sxs-lookup"><span data-stu-id="c6a98-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a98-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6a98-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c6a98-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c6a98-138">Windows XP</span></span><br/>                                                              |
| <span data-ttu-id="c6a98-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6a98-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c6a98-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c6a98-140">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="c6a98-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c6a98-141">Namespace</span></span><br/>                | <span data-ttu-id="c6a98-142">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="c6a98-142">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="c6a98-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c6a98-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6a98-144"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6a98-144"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6a98-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6a98-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a98-146">Provider WDM</span><span class="sxs-lookup"><span data-stu-id="c6a98-146">WDM Provider</span></span>](wdm-provider.md)
</dt> </dl>

 


---
description: Contiene i metodi che ottengono il contenuto non elaborato della definizione del video di input dei dati di identificazione (VESA) Enhanced Extended Display Data (E-EDID) v. 1. x blocchi di dati standard a 128 byte.
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: Classe WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods
- WmiMonitorDescriptorMethods.Active
- WmiMonitorDescriptorMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 578c08c48ada4859b69e00655c5eea8c075515fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315740"
---
# <a name="wmimonitordescriptormethods-class"></a><span data-ttu-id="da9f8-103">Classe WmiMonitorDescriptorMethods</span><span class="sxs-lookup"><span data-stu-id="da9f8-103">WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="da9f8-104">La classe WMI **WmiMonitorDescriptorMethods** contiene i metodi che ottengono il contenuto non elaborato della definizione di input video di video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) v. 1. x blocchi di dati Standard a 128 byte.</span><span class="sxs-lookup"><span data-stu-id="da9f8-104">The **WmiMonitorDescriptorMethods** WMI class contains methods that obtain the raw content of Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) v.1.x standard 128-byte data blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="da9f8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da9f8-105">Syntax</span></span>

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="da9f8-106">Members</span><span class="sxs-lookup"><span data-stu-id="da9f8-106">Members</span></span>

<span data-ttu-id="da9f8-107">La classe **WmiMonitorDescriptorMethods** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="da9f8-107">The **WmiMonitorDescriptorMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="da9f8-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="da9f8-108">Methods</span></span>](#wmimonitordescriptormethods-class)
-   [<span data-ttu-id="da9f8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da9f8-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="da9f8-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="da9f8-110">Methods</span></span>

<span data-ttu-id="da9f8-111">La classe **WmiMonitorDescriptorMethods** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="da9f8-111">The **WmiMonitorDescriptorMethods** class has these methods.</span></span>



| <span data-ttu-id="da9f8-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="da9f8-112">Method</span></span>                                                                                           | <span data-ttu-id="da9f8-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da9f8-113">Description</span></span>                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="da9f8-114">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="da9f8-114">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | <span data-ttu-id="da9f8-115">Accede ai dati non elaborati per un blocco descrittore EDID v. 1. x specificato.</span><span class="sxs-lookup"><span data-stu-id="da9f8-115">Accesses the raw data for a specified EDID v.1.x descriptor block.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="da9f8-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da9f8-116">Properties</span></span>

<span data-ttu-id="da9f8-117">La classe **WmiMonitorDescriptorMethods** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="da9f8-117">The **WmiMonitorDescriptorMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da9f8-118">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="da9f8-118">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9f8-119">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="da9f8-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da9f8-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da9f8-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da9f8-121">Indica il monitoraggio attivo.</span><span class="sxs-lookup"><span data-stu-id="da9f8-121">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="da9f8-122">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="da9f8-122">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da9f8-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da9f8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da9f8-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da9f8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da9f8-125">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="da9f8-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="da9f8-126">Nome dell'istanza di monitoraggio specifica.</span><span class="sxs-lookup"><span data-stu-id="da9f8-126">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da9f8-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da9f8-127">Requirements</span></span>



| <span data-ttu-id="da9f8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="da9f8-128">Requirement</span></span> | <span data-ttu-id="da9f8-129">Valore</span><span class="sxs-lookup"><span data-stu-id="da9f8-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da9f8-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da9f8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="da9f8-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da9f8-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="da9f8-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da9f8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="da9f8-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da9f8-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="da9f8-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="da9f8-134">Namespace</span></span><br/>                | <span data-ttu-id="da9f8-135">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="da9f8-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="da9f8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="da9f8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da9f8-137"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da9f8-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="da9f8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="da9f8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da9f8-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da9f8-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da9f8-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da9f8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da9f8-141">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="da9f8-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 





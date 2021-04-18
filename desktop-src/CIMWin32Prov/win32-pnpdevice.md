---
description: La \_ classe WMI dell'associazione PnPDevice Win32 mette in correlazione un dispositivo (noto a Configuration Manager come PNPEntity) e la funzione che esegue.
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Classe Win32_PnPDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c17dc6d4169854469d630e2a622eacc85e8a587c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305272"
---
# <a name="win32_pnpdevice-class"></a><span data-ttu-id="032fe-103">Win32 \_ PnPDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="032fe-103">Win32\_PnPDevice class</span></span>

<span data-ttu-id="032fe-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ PnPDevice Win32** mette in correlazione un dispositivo (noto a Configuration Manager come PNPEntity) e la funzione che esegue.</span><span class="sxs-lookup"><span data-stu-id="032fe-104">The **Win32\_PnPDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a device (known to Configuration Manager as a PNPEntity) and the function it performs.</span></span> <span data-ttu-id="032fe-105">La relativa funzione è rappresentata da una sottoclasse del dispositivo logico che ne descrive l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="032fe-105">Its function is represented by a subclass of the logical device that describes its use.</span></span> <span data-ttu-id="032fe-106">Ad esempio, una [**\_ tastiera Win32**](win32-keyboard.md) o un'istanza [**Win32 \_ DiskDrive**](win32-diskdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="032fe-106">For example, a [**Win32\_Keyboard**](win32-keyboard.md) or [**Win32\_DiskDrive**](win32-diskdrive.md) instance.</span></span> <span data-ttu-id="032fe-107">Entrambi gli oggetti a cui si fa riferimento rappresentano lo stesso dispositivo di sistema sottostante. le modifiche apportate all'allocazione delle risorse sul lato PNPEntity comporteranno l'effetto del dispositivo associato.</span><span class="sxs-lookup"><span data-stu-id="032fe-107">Both referenced objects represent the same underlying system device; changes to resource allocation on the PNPEntity side will effect the associated device.</span></span>

<span data-ttu-id="032fe-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="032fe-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="032fe-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="032fe-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="032fe-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="032fe-110">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="032fe-111">Members</span><span class="sxs-lookup"><span data-stu-id="032fe-111">Members</span></span>

<span data-ttu-id="032fe-112">La classe **Win32 \_ PnPDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="032fe-112">The **Win32\_PnPDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="032fe-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="032fe-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="032fe-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="032fe-114">Properties</span></span>

<span data-ttu-id="032fe-115">La classe **Win32 \_ PnPDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="032fe-115">The **Win32\_PnPDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="032fe-116">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="032fe-116">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="032fe-117">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="032fe-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="032fe-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="032fe-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="032fe-119">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="032fe-119">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="032fe-120">Riferimento all'istanza [**CIM \_ LogicalDevice**](cim-logicaldevice.md) che rappresenta le proprietà logiche del dispositivo associate al dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="032fe-120">Reference to the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance representing the logical device properties associated with the Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="032fe-121">**SystemElement**</span><span class="sxs-lookup"><span data-stu-id="032fe-121">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="032fe-122">Tipo di dati: **Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="032fe-122">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="032fe-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="032fe-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="032fe-124">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PnPEntity")</span><span class="sxs-lookup"><span data-stu-id="032fe-124">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PnPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="032fe-125">Riferimento all'istanza [**Win32 \_ PnPEntity**](win32-pnpentity.md) che rappresenta il dispositivo Plug and Play associato al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="032fe-125">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance representing the Plug and Play device associated with the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="032fe-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="032fe-126">Requirements</span></span>



| <span data-ttu-id="032fe-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="032fe-127">Requirement</span></span> | <span data-ttu-id="032fe-128">Valore</span><span class="sxs-lookup"><span data-stu-id="032fe-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="032fe-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="032fe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="032fe-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="032fe-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="032fe-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="032fe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="032fe-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="032fe-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="032fe-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="032fe-133">Namespace</span></span><br/>                | <span data-ttu-id="032fe-134">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="032fe-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="032fe-135">MOF</span><span class="sxs-lookup"><span data-stu-id="032fe-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="032fe-136"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="032fe-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="032fe-137">DLL</span><span class="sxs-lookup"><span data-stu-id="032fe-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="032fe-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="032fe-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="032fe-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="032fe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="032fe-140">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="032fe-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

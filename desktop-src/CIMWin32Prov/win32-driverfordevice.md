---
description: La \_ classe WMI dell'associazione DriverForDevice Win32 mette in correlazione un'istanza di stampante a un'istanza di driver della stampante.
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Classe Win32_DriverForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5fb384eed80c6a614af448477c50be3204d3080
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305092"
---
# <a name="win32_driverfordevice-class"></a><span data-ttu-id="5c291-103">Win32 \_ DriverForDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="5c291-103">Win32\_DriverForDevice class</span></span>

<span data-ttu-id="5c291-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ DriverForDevice Win32** mette in correlazione un'istanza di stampante a un'istanza di driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="5c291-104">The **Win32\_DriverForDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a printer instance to a printer driver instance.</span></span>

<span data-ttu-id="5c291-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5c291-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5c291-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5c291-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c291-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c291-107">Syntax</span></span>

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5c291-108">Members</span><span class="sxs-lookup"><span data-stu-id="5c291-108">Members</span></span>

<span data-ttu-id="5c291-109">La classe **Win32 \_ DriverForDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5c291-109">The **Win32\_DriverForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="5c291-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c291-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c291-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c291-111">Properties</span></span>

<span data-ttu-id="5c291-112">La classe **Win32 \_ DriverForDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5c291-112">The **Win32\_DriverForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c291-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5c291-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c291-114">Tipo di dati **: \_ stampante Win32**</span><span class="sxs-lookup"><span data-stu-id="5c291-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="5c291-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5c291-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5c291-116">Riferimento all'istanza [**della \_ stampante Win32**](win32-printer.md) che rappresenta la stampante.</span><span class="sxs-lookup"><span data-stu-id="5c291-116">Reference to the [**Win32\_Printer**](win32-printer.md) instance that represents the printer.</span></span>

<span data-ttu-id="5c291-117">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5c291-117">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c291-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="5c291-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c291-119">Tipo di dati: **Win32 \_ PrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="5c291-119">Data type: **Win32\_PrinterDriver**</span></span>
</dt> <dt>

<span data-ttu-id="5c291-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c291-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c291-121">Riferimento all'istanza [**Win32 \_ PrinterDriver**](win32-printerdriver.md) che rappresenta il driver della stampante per la stampante.</span><span class="sxs-lookup"><span data-stu-id="5c291-121">Reference to the [**Win32\_PrinterDriver**](win32-printerdriver.md) instance that represents the printer driver for the printer.</span></span>

<span data-ttu-id="5c291-122">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5c291-122">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c291-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c291-123">Remarks</span></span>

<span data-ttu-id="5c291-124">La classe **Win32 \_ DriverForDevice** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5c291-124">The **Win32\_DriverForDevice** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c291-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c291-125">Requirements</span></span>



| <span data-ttu-id="5c291-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c291-126">Requirement</span></span> | <span data-ttu-id="5c291-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5c291-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c291-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c291-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5c291-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c291-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="5c291-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c291-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5c291-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c291-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="5c291-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5c291-132">Namespace</span></span><br/>                | <span data-ttu-id="5c291-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5c291-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="5c291-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5c291-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c291-135"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c291-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c291-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5c291-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c291-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c291-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="5c291-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c291-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c291-139">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="5c291-139">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 


---
description: La \_ classe WMI dell'associazione PrinterDriverDll Win32 mette in relazione una stampante locale e il relativo file del driver.
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Classe Win32_PrinterDriverDll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriverDll
- Win32_PrinterDriverDll.Antecedent
- Win32_PrinterDriverDll.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41484c39d9e1b59efd79d7aee08719b3a241de97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483693"
---
# <a name="win32_printerdriverdll-class"></a><span data-ttu-id="f3168-103">Win32 \_ PrinterDriverDll (classe)</span><span class="sxs-lookup"><span data-stu-id="f3168-103">Win32\_PrinterDriverDll class</span></span>

<span data-ttu-id="f3168-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ PrinterDriverDll Win32** mette in relazione una stampante locale e il relativo file del driver.</span><span class="sxs-lookup"><span data-stu-id="f3168-104">The **Win32\_PrinterDriverDll** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and its driver file.</span></span>

<span data-ttu-id="f3168-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f3168-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f3168-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f3168-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3168-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3168-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f3168-108">Members</span><span class="sxs-lookup"><span data-stu-id="f3168-108">Members</span></span>

<span data-ttu-id="f3168-109">La classe **Win32 \_ PrinterDriverDll** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f3168-109">The **Win32\_PrinterDriverDll** class has these types of members:</span></span>

-   [<span data-ttu-id="f3168-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f3168-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3168-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f3168-111">Properties</span></span>

<span data-ttu-id="f3168-112">La classe **Win32 \_ PrinterDriverDll** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f3168-112">The **Win32\_PrinterDriverDll** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3168-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f3168-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3168-114">Tipo di dati **: \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="f3168-114">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="f3168-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3168-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3168-116">Qualificatori: [ **chiave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f3168-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f3168-117">Riferimento all'istanza [**di \_ DataFile DataFile**](cim-datafile.md) che rappresenta il file del driver per la stampante basata su Windows.</span><span class="sxs-lookup"><span data-stu-id="f3168-117">Reference to the [**CIM\_DataFile**](cim-datafile.md) instance representing the driver file for this Windows-based printer.</span></span>

<span data-ttu-id="f3168-118">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="f3168-118">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3168-119">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="f3168-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3168-120">Tipo di dati **: \_ stampante Win32**</span><span class="sxs-lookup"><span data-stu-id="f3168-120">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="f3168-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f3168-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3168-122">Qualificatori: [ **chiave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f3168-122">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f3168-123">Riferimento all'istanza [**della \_ stampante Win32**](win32-printer.md) .</span><span class="sxs-lookup"><span data-stu-id="f3168-123">Reference to the [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="f3168-124">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="f3168-124">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3168-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3168-125">Remarks</span></span>

<span data-ttu-id="f3168-126">La classe **Win32 \_ PrinterDriverDll** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="f3168-126">The **Win32\_PrinterDriverDll** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3168-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3168-127">Requirements</span></span>



| <span data-ttu-id="f3168-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3168-128">Requirement</span></span> | <span data-ttu-id="f3168-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f3168-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3168-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3168-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f3168-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3168-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="f3168-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3168-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f3168-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3168-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="f3168-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f3168-134">Namespace</span></span><br/>                | <span data-ttu-id="f3168-135">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f3168-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="f3168-136">MOF</span><span class="sxs-lookup"><span data-stu-id="f3168-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3168-137"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3168-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3168-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f3168-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3168-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3168-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="f3168-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3168-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3168-141">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="f3168-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="f3168-142">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="f3168-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

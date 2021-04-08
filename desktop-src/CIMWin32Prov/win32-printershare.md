---
description: La \_ classe WMI dell'associazione PrinterShare Win32 mette in relazione una stampante locale e la condivisione che la rappresenta mentre viene visualizzata in una rete.
ms.assetid: 9ac99e52-5e8f-4329-960f-7bd1fd229e37
ms.tgt_platform: multiple
title: Classe Win32_PrinterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterShare
- Win32_PrinterShare.Antecedent
- Win32_PrinterShare.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57bc15fc5d3db78179335b039851d7d3b7cbf8a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878141"
---
# <a name="win32_printershare-class"></a><span data-ttu-id="d41bc-103">Win32 \_ PrinterShare (classe)</span><span class="sxs-lookup"><span data-stu-id="d41bc-103">Win32\_PrinterShare class</span></span>

<span data-ttu-id="d41bc-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ PrinterShare Win32** mette in relazione una stampante locale e la condivisione che la rappresenta mentre viene visualizzata in una rete.</span><span class="sxs-lookup"><span data-stu-id="d41bc-104">The **Win32\_PrinterShare** association [WMI class](../wmisdk/retrieving-a-class.md) relates a local printer and the share that represents it as it is viewed over a network.</span></span>

<span data-ttu-id="d41bc-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d41bc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d41bc-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d41bc-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d41bc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d41bc-107">Syntax</span></span>

``` syntax
class Win32_PrinterShare : CIM_Dependency
{
  Win32_Printer REF Antecedent;
  Win32_Share   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d41bc-108">Members</span><span class="sxs-lookup"><span data-stu-id="d41bc-108">Members</span></span>

<span data-ttu-id="d41bc-109">La classe **Win32 \_ PrinterShare** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d41bc-109">The **Win32\_PrinterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="d41bc-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d41bc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d41bc-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d41bc-111">Properties</span></span>

<span data-ttu-id="d41bc-112">La classe **Win32 \_ PrinterShare** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d41bc-112">The **Win32\_PrinterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d41bc-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="d41bc-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d41bc-114">Tipo di dati **: \_ stampante Win32**</span><span class="sxs-lookup"><span data-stu-id="d41bc-114">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="d41bc-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d41bc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d41bc-116">Qualificatori: [ **chiave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d41bc-116">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d41bc-117">Riferimento all'istanza di che rappresenta la stampante locale condivisa in questa associazione.</span><span class="sxs-lookup"><span data-stu-id="d41bc-117">Reference to the instance representing the local printer shared in this association.</span></span>

</dd> <dt>

<span data-ttu-id="d41bc-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="d41bc-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d41bc-119">Tipo di dati **: \_ condivisione Win32**</span><span class="sxs-lookup"><span data-stu-id="d41bc-119">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="d41bc-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d41bc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d41bc-121">Qualificatori: [ **chiave**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d41bc-121">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d41bc-122">Riferimento all'istanza di che rappresenta la condivisione della stampante in questa associazione.</span><span class="sxs-lookup"><span data-stu-id="d41bc-122">Reference to the instance representing the share of the printer in this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d41bc-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d41bc-123">Remarks</span></span>

<span data-ttu-id="d41bc-124">La classe **Win32 \_ PrinterShare** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d41bc-124">The **Win32\_PrinterShare** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d41bc-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d41bc-125">Requirements</span></span>



| <span data-ttu-id="d41bc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d41bc-126">Requirement</span></span> | <span data-ttu-id="d41bc-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d41bc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d41bc-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d41bc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d41bc-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d41bc-129">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="d41bc-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d41bc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d41bc-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d41bc-131">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="d41bc-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d41bc-132">Namespace</span></span><br/>                | <span data-ttu-id="d41bc-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d41bc-133">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="d41bc-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d41bc-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d41bc-135"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d41bc-135"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="d41bc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d41bc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d41bc-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d41bc-137"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="d41bc-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d41bc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d41bc-139">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d41bc-139">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 

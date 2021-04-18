---
description: Verifica se l'elemento fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico.
ms.assetid: 406aaa75-b48c-4377-adb5-e900676b6e36
ms.tgt_platform: multiple
title: Metodo di compatibilità della classe CIM_PhysicalPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1957b8d0c1929ff6f7b4ef8c69fa55ea4ccc83b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304757"
---
# <a name="iscompatible-method-of-the-cim_physicalpackage-class"></a><span data-ttu-id="8b0b0-103">Metodo di compatibilità della classe CIM \_ PhysicalPackage</span><span class="sxs-lookup"><span data-stu-id="8b0b0-103">IsCompatible method of the CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="8b0b0-104">Il **Metodo IsValid verifica se l'elemento** fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="8b0b0-104">The **IsCompatible** method verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="8b0b0-105">In una sottoclasse è possibile specificare il set di possibili codici restituiti utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="8b0b0-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="8b0b0-106">Le stringhe a cui viene convertito il contenuto **ValueMap** possono anche essere specificate nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="8b0b0-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b0b0-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="8b0b0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8b0b0-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8b0b0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8b0b0-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8b0b0-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8b0b0-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8b0b0-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b0b0-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b0b0-111">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="8b0b0-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b0b0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b0b0-113">*ElementToCheck* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b0b0-113">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b0b0-114">Riferimento all'elemento fisico su cui è in esecuzione il metodo di **compatibilità** .</span><span class="sxs-lookup"><span data-stu-id="8b0b0-114">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b0b0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b0b0-115">Return value</span></span>

<span data-ttu-id="8b0b0-116">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="8b0b0-116">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b0b0-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b0b0-117">Remarks</span></span>

<span data-ttu-id="8b0b0-118">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="8b0b0-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8b0b0-119">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="8b0b0-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8b0b0-120">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="8b0b0-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8b0b0-121">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="8b0b0-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b0b0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b0b0-122">Requirements</span></span>



| <span data-ttu-id="8b0b0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b0b0-123">Requirement</span></span> | <span data-ttu-id="8b0b0-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8b0b0-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b0b0-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b0b0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8b0b0-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b0b0-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b0b0-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b0b0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8b0b0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b0b0-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b0b0-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8b0b0-129">Namespace</span></span><br/>                | <span data-ttu-id="8b0b0-130">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8b0b0-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8b0b0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="8b0b0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b0b0-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b0b0-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b0b0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8b0b0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b0b0-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b0b0-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b0b0-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b0b0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b0b0-136">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="8b0b0-136">**CIM\_PhysicalPackage**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="8b0b0-137">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="8b0b0-137">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 


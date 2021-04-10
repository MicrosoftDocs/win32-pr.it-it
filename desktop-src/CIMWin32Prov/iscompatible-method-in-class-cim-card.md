---
description: Il metodo IsValid verifica se l'elemento fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico.
ms.assetid: 809a1871-dfa2-499b-9adf-118dec71586b
ms.tgt_platform: multiple
title: Metodo di compatibilità della classe CIM_Card
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Card.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0573cc9902826d2a283e549414cf31aae98cc331
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126456"
---
# <a name="iscompatible-method-of-the-cim_card-class"></a><span data-ttu-id="a223a-103">Metodo di compatibilità della classe CIM \_</span><span class="sxs-lookup"><span data-stu-id="a223a-103">IsCompatible method of the CIM\_Card class</span></span>

<span data-ttu-id="a223a-104">Il **Metodo IsValid verifica se l'elemento** fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="a223a-104">The **IsCompatible** method verifies whether the referenced physical element may be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="a223a-105">In una sottoclasse, il set di possibili codici restituiti può essere specificato utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="a223a-105">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="a223a-106">Le stringhe a cui viene convertito il contenuto **ValueMap** possono anche essere specificate nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="a223a-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="a223a-107">Questo metodo viene ereditato da [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="a223a-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a223a-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a223a-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a223a-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a223a-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a223a-110">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a223a-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a223a-111">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a223a-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a223a-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a223a-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="a223a-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="a223a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a223a-114">*ElementToCheck* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a223a-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a223a-115">Riferimento all'elemento fisico su cui è in esecuzione il metodo di **compatibilità** .</span><span class="sxs-lookup"><span data-stu-id="a223a-115">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a223a-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a223a-116">Return value</span></span>

<span data-ttu-id="a223a-117">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="a223a-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a223a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="a223a-118">Remarks</span></span>

<span data-ttu-id="a223a-119">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="a223a-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a223a-120">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="a223a-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a223a-121">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a223a-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a223a-122">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a223a-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a223a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a223a-123">Requirements</span></span>



| <span data-ttu-id="a223a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a223a-124">Requirement</span></span> | <span data-ttu-id="a223a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a223a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a223a-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a223a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a223a-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a223a-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a223a-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a223a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a223a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a223a-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a223a-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a223a-130">Namespace</span></span><br/>                | <span data-ttu-id="a223a-131">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a223a-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a223a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a223a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a223a-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a223a-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a223a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a223a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a223a-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a223a-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a223a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a223a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a223a-137">\_Scheda CIM</span><span class="sxs-lookup"><span data-stu-id="a223a-137">CIM\_Card</span></span>](iscompatible-method-in-class-cim-card.md)
</dt> <dt>

[<span data-ttu-id="a223a-138">**\_Scheda CIM**</span><span class="sxs-lookup"><span data-stu-id="a223a-138">**CIM\_Card**</span></span>](cim-card.md)
</dt> </dl>

 


---
description: Il metodo StartService inserisce il servizio in uno stato avviato.
ms.assetid: 0f2880ed-1643-4211-8684-12493711b1f8
ms.tgt_platform: multiple
title: Metodo StartService della classe CIM_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1592552595c06ec7111041cbb1c1b1d2628f8b6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748418"
---
# <a name="startservice-method-of-the-cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="59d8a-103">Metodo StartService della classe CIM_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="59d8a-103">StartService method of the CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="59d8a-104">Il metodo **StartService** inserisce il servizio in uno stato avviato.</span><span class="sxs-lookup"><span data-stu-id="59d8a-104">The **StartService** method puts the service in a started state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59d8a-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="59d8a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="59d8a-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="59d8a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="59d8a-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="59d8a-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="59d8a-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="59d8a-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="59d8a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59d8a-109">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="59d8a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="59d8a-110">Parameters</span></span>

<span data-ttu-id="59d8a-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="59d8a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59d8a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59d8a-112">Return value</span></span>

<span data-ttu-id="59d8a-113">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="59d8a-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="59d8a-114">In una sottoclasse è possibile specificare il set di possibili codici restituiti utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="59d8a-114">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="59d8a-115">Le stringhe a cui viene convertito il contenuto **ValueMap** possono anche essere specificate nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="59d8a-115">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="59d8a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="59d8a-116">Remarks</span></span>

<span data-ttu-id="59d8a-117">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="59d8a-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="59d8a-118">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="59d8a-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="59d8a-119">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="59d8a-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="59d8a-120">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="59d8a-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="59d8a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59d8a-121">Requirements</span></span>



| <span data-ttu-id="59d8a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="59d8a-122">Requirement</span></span> | <span data-ttu-id="59d8a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="59d8a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59d8a-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59d8a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="59d8a-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59d8a-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="59d8a-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59d8a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="59d8a-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59d8a-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59d8a-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="59d8a-128">Namespace</span></span><br/>                | <span data-ttu-id="59d8a-129">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="59d8a-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="59d8a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="59d8a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59d8a-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59d8a-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="59d8a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="59d8a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59d8a-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59d8a-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59d8a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59d8a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59d8a-135">\_Servizio CIM</span><span class="sxs-lookup"><span data-stu-id="59d8a-135">CIM\_Service</span></span>](startservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="59d8a-136">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="59d8a-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 


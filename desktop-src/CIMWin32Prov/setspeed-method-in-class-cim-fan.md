---
description: Il metodo sespeed richiede che la velocità della ventola venga impostata sul valore specificato nel parametro di input del metodo.
ms.assetid: 7dd1cd57-66c5-4b50-9a73-31caf0b824e6
ms.tgt_platform: multiple
title: Metodo sespeed della classe CIM_Fan
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan.SetSpeed
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16d90dbef3a9318ad144303e5720cea0abbde03e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878373"
---
# <a name="setspeed-method-of-the-cim_fan-class"></a><span data-ttu-id="8a8bd-103">Metodo di sevelocità della \_ classe di fan CIM</span><span class="sxs-lookup"><span data-stu-id="8a8bd-103">SetSpeed method of the CIM\_Fan class</span></span>

<span data-ttu-id="8a8bd-104">Il metodo **sespeed** richiede che la velocità della ventola venga impostata sul valore specificato nel parametro di input del metodo.</span><span class="sxs-lookup"><span data-stu-id="8a8bd-104">The **SetSpeed** method requests that the fan speed be set to the value specified in the method's input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a8bd-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="8a8bd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8a8bd-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8a8bd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8a8bd-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8a8bd-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8a8bd-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8a8bd-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a8bd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a8bd-109">Syntax</span></span>


```mof
uint32 SetSpeed(
  [in] uint64 DesiredSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="8a8bd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a8bd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a8bd-111">*DesiredSpeed* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a8bd-111">*DesiredSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8bd-112">Velocità della ventola richiesta, in rivoluzioni al minuto.</span><span class="sxs-lookup"><span data-stu-id="8a8bd-112">Requested fan speed, in revolutions per minute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a8bd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a8bd-113">Return value</span></span>

<span data-ttu-id="8a8bd-114">Restituisce un valore pari a 0 (zero) in caso di esito positivo, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="8a8bd-114">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a8bd-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a8bd-115">Remarks</span></span>

<span data-ttu-id="8a8bd-116">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="8a8bd-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8a8bd-117">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="8a8bd-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8a8bd-118">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="8a8bd-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8a8bd-119">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="8a8bd-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a8bd-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a8bd-120">Requirements</span></span>



| <span data-ttu-id="8a8bd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a8bd-121">Requirement</span></span> | <span data-ttu-id="8a8bd-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8a8bd-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8bd-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a8bd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8a8bd-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a8bd-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a8bd-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a8bd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8a8bd-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a8bd-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a8bd-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8a8bd-127">Namespace</span></span><br/>                | <span data-ttu-id="8a8bd-128">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8a8bd-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8a8bd-129">MOF</span><span class="sxs-lookup"><span data-stu-id="8a8bd-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a8bd-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a8bd-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a8bd-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8a8bd-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a8bd-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a8bd-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a8bd-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a8bd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a8bd-134">\_Ventola CIM</span><span class="sxs-lookup"><span data-stu-id="8a8bd-134">CIM\_Fan</span></span>](setspeed-method-in-class-cim-fan.md)
</dt> <dt>

[<span data-ttu-id="8a8bd-135">**\_Ventola CIM**</span><span class="sxs-lookup"><span data-stu-id="8a8bd-135">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> </dl>

 


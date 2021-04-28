---
description: 'Metodo StartService della classe CIM_Service (provider WMI CIMWin32): il metodo StartService inserisce il servizio in uno stato avviato.'
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
ms.openlocfilehash: 6027112323fc14abf4c4a8dc667b921025a5e652
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086169"
---
# <a name="startservice-method-of-the-cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="4e60e-103">Metodo StartService della classe CIM_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="4e60e-103">StartService method of the CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="4e60e-104">Il **metodo StartService** imposta lo stato avviato del servizio.</span><span class="sxs-lookup"><span data-stu-id="4e60e-104">The **StartService** method puts the service in a started state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e60e-105">Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4e60e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4e60e-106">WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4e60e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4e60e-107">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4e60e-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4e60e-108">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4e60e-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e60e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e60e-109">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="4e60e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e60e-110">Parameters</span></span>

<span data-ttu-id="4e60e-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4e60e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e60e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e60e-112">Return value</span></span>

<span data-ttu-id="4e60e-113">Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="4e60e-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="4e60e-114">In una sottoclasse è possibile specificare il set di possibili codici restituiti usando un **qualificatore ValueMap** nel metodo .</span><span class="sxs-lookup"><span data-stu-id="4e60e-114">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="4e60e-115">Le stringhe in cui vengono **convertiti i contenuti di ValueMap** possono essere specificate anche nella sottoclasse come qualificatore di matrice **Values.**</span><span class="sxs-lookup"><span data-stu-id="4e60e-115">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e60e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e60e-116">Remarks</span></span>

<span data-ttu-id="4e60e-117">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="4e60e-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4e60e-118">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="4e60e-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4e60e-119">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4e60e-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4e60e-120">Microsoft potrebbe aver apportato modifiche per correggere errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4e60e-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e60e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e60e-121">Requirements</span></span>



| <span data-ttu-id="4e60e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e60e-122">Requirement</span></span> | <span data-ttu-id="4e60e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4e60e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e60e-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e60e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4e60e-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e60e-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e60e-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e60e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4e60e-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e60e-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e60e-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4e60e-128">Namespace</span></span><br/>                | <span data-ttu-id="4e60e-129">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4e60e-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e60e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4e60e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e60e-131"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e60e-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e60e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4e60e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e60e-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e60e-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e60e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e60e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e60e-135">Servizio \_ CIM</span><span class="sxs-lookup"><span data-stu-id="4e60e-135">CIM\_Service</span></span>](startservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="4e60e-136">**Servizio \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="4e60e-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 


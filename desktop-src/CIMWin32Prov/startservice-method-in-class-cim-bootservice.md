---
description: Il metodo StartService inserisce il servizio in un &\# 0034; iniziare&\# 0034; stato.
ms.assetid: b2b38d64-b497-46f5-8638-a9a8ce50e888
ms.tgt_platform: multiple
title: Metodo StartService della classe CIM_BootService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7f7f56633319f9e009f58f7c06dde7a3baee8e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966365"
---
# <a name="startservice-method-of-the-cim_bootservice-class"></a><span data-ttu-id="d3021-103">Metodo StartService della classe CIM \_ Bootservice</span><span class="sxs-lookup"><span data-stu-id="d3021-103">StartService method of the CIM\_BootService class</span></span>

<span data-ttu-id="d3021-104">Il metodo **StartService** inserisce il servizio nello stato "Start".</span><span class="sxs-lookup"><span data-stu-id="d3021-104">The **StartService** method puts the service in a "start" state.</span></span> <span data-ttu-id="d3021-105">In una sottoclasse è possibile specificare il set di possibili codici restituiti utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="d3021-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="d3021-106">Le stringhe a cui viene convertito il contenuto **ValueMap** possono anche essere specificate nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="d3021-106">The strings to which the **ValueMap** contents are translated may also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="d3021-107">Questo metodo viene ereditato dal [**\_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="d3021-107">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3021-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="d3021-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d3021-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d3021-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d3021-110">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="d3021-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d3021-111">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d3021-111">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3021-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3021-112">Syntax</span></span>


```mof
Integer StartService();
```



## <a name="parameters"></a><span data-ttu-id="d3021-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3021-113">Parameters</span></span>

<span data-ttu-id="d3021-114">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d3021-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3021-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3021-115">Return value</span></span>

<span data-ttu-id="d3021-116">Restituisce un valore pari a 0 (zero) in caso di esito positivo, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="d3021-116">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3021-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3021-117">Remarks</span></span>

<span data-ttu-id="d3021-118">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="d3021-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d3021-119">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="d3021-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d3021-120">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="d3021-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d3021-121">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="d3021-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3021-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3021-122">Requirements</span></span>



| <span data-ttu-id="d3021-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3021-123">Requirement</span></span> | <span data-ttu-id="d3021-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d3021-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3021-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3021-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d3021-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3021-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3021-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3021-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d3021-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3021-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3021-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d3021-129">Namespace</span></span><br/>                | <span data-ttu-id="d3021-130">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d3021-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d3021-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d3021-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3021-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3021-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3021-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d3021-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3021-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3021-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3021-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3021-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3021-136">\_BOOTSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="d3021-136">CIM\_BootService</span></span>](startservice-method-in-class-cim-bootservice.md)
</dt> <dt>

[<span data-ttu-id="d3021-137">**\_BOOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="d3021-137">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> </dl>

 


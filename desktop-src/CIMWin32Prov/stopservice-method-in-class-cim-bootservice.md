---
description: Arresta il servizio rappresentato dall'oggetto derivato da CIM \_ BootService.
ms.assetid: 443a2afa-ed46-4378-a06f-5f9f94af51c9
ms.tgt_platform: multiple
title: Metodo StopService della classe CIM_BootService (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c054a9d05410ddbe7ee7d11c5bd4adba9e0ce83b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523690"
---
# <a name="stopservice-method-of-the-cim_bootservice-class"></a><span data-ttu-id="da1fd-103">Metodo StopService della classe CIM \_ Bootservice</span><span class="sxs-lookup"><span data-stu-id="da1fd-103">StopService method of the CIM\_BootService class</span></span>

<span data-ttu-id="da1fd-104">Il metodo **StopService** arresta il servizio rappresentato dall'oggetto derivato da [**CIM \_ BOOTSERVICE**](cim-bootservice.md).</span><span class="sxs-lookup"><span data-stu-id="da1fd-104">The **StopService** method stops the service represented by the object derived from [**CIM\_BootService**](cim-bootservice.md).</span></span> <span data-ttu-id="da1fd-105">Questo metodo viene ereditato dal [**\_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="da1fd-105">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da1fd-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="da1fd-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="da1fd-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="da1fd-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="da1fd-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="da1fd-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="da1fd-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="da1fd-109">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="da1fd-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da1fd-110">Syntax</span></span>


```mof
Integer StopService();
```



## <a name="parameters"></a><span data-ttu-id="da1fd-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="da1fd-111">Parameters</span></span>

<span data-ttu-id="da1fd-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="da1fd-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="da1fd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da1fd-113">Return value</span></span>

<span data-ttu-id="da1fd-114">Restituisce un valore pari a 0 (zero) in caso di esito positivo, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="da1fd-114">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="da1fd-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="da1fd-115">Remarks</span></span>

<span data-ttu-id="da1fd-116">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="da1fd-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="da1fd-117">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="da1fd-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="da1fd-118">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="da1fd-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="da1fd-119">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="da1fd-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="da1fd-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da1fd-120">Requirements</span></span>



| <span data-ttu-id="da1fd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="da1fd-121">Requirement</span></span> | <span data-ttu-id="da1fd-122">Valore</span><span class="sxs-lookup"><span data-stu-id="da1fd-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da1fd-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da1fd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="da1fd-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da1fd-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da1fd-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da1fd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="da1fd-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da1fd-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da1fd-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="da1fd-127">Namespace</span></span><br/>                | <span data-ttu-id="da1fd-128">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="da1fd-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="da1fd-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da1fd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="da1fd-130"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="da1fd-130"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="da1fd-131">MOF</span><span class="sxs-lookup"><span data-stu-id="da1fd-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da1fd-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da1fd-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="da1fd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="da1fd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da1fd-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da1fd-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da1fd-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da1fd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da1fd-136">\_BOOTSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="da1fd-136">CIM\_BootService</span></span>](stopservice-method-in-class-cim-bootservice.md)
</dt> <dt>

[<span data-ttu-id="da1fd-137">**\_BOOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="da1fd-137">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> </dl>

 


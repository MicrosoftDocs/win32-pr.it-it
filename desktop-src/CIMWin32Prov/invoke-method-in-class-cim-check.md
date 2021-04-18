---
description: Il metodo Invoke della classe CIM \_ Check valuta un particolare controllo.
ms.assetid: cf1adeb2-f8a2-4f84-978f-e801bce104ac
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_Check
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7774fcd1b3ef451fffb34ce9ad10d404e8ea95b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304678"
---
# <a name="invoke-method-of-the-cim_check-class"></a><span data-ttu-id="f9f54-103">Metodo Invoke della classe CIM \_ check</span><span class="sxs-lookup"><span data-stu-id="f9f54-103">Invoke method of the CIM\_Check class</span></span>

<span data-ttu-id="f9f54-104">Il metodo **Invoke** della classe [**CIM \_ Check**](cim-check.md) valuta un particolare controllo.</span><span class="sxs-lookup"><span data-stu-id="f9f54-104">The **Invoke** method of the [**CIM\_Check**](cim-check.md) class evaluates a particular check.</span></span>

<span data-ttu-id="f9f54-105">Per ulteriori informazioni sul modo in cui il metodo valuta un particolare controllo in un contesto CIM, vedere le sottoclassi [**di \_ controllo CIM**](cim-check.md) non astratte.</span><span class="sxs-lookup"><span data-stu-id="f9f54-105">For more information about how the method evaluates a particular check in a CIM context, see the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f9f54-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f9f54-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f9f54-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f9f54-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f9f54-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f9f54-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f9f54-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f9f54-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9f54-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9f54-110">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="f9f54-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9f54-111">Parameters</span></span>

<span data-ttu-id="f9f54-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f9f54-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9f54-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9f54-113">Return value</span></span>

<span data-ttu-id="f9f54-114">Restituisce un valore pari a 0 (zero) in caso di esito positivo, 1 (uno) se il metodo non è supportato e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="f9f54-114">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9f54-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9f54-115">Remarks</span></span>

<span data-ttu-id="f9f54-116">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="f9f54-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f9f54-117">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="f9f54-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f9f54-118">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f9f54-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f9f54-119">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f9f54-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9f54-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9f54-120">Requirements</span></span>



| <span data-ttu-id="f9f54-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9f54-121">Requirement</span></span> | <span data-ttu-id="f9f54-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f9f54-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f54-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9f54-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f9f54-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9f54-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9f54-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9f54-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f9f54-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9f54-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9f54-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f9f54-127">Namespace</span></span><br/>                | <span data-ttu-id="f9f54-128">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f9f54-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f9f54-129">MOF</span><span class="sxs-lookup"><span data-stu-id="f9f54-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9f54-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9f54-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9f54-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f9f54-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9f54-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9f54-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9f54-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9f54-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f54-134">**\_Controllo CIM**</span><span class="sxs-lookup"><span data-stu-id="f9f54-134">**CIM\_Check**</span></span>](invoke-method-in-class-cim-check.md)
</dt> <dt>

[<span data-ttu-id="f9f54-135">**\_Controllo CIM**</span><span class="sxs-lookup"><span data-stu-id="f9f54-135">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 


---
description: Il metodo Invoke della classe di \_ azione CIM esegue una determinata azione. I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione.
ms.assetid: 4f0be560-bd78-4c7f-b6e3-ca86837a84f9
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_Action
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Action.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e02e414fb05e0dd4ea97c3e3a4d87659fed4c963
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877585"
---
# <a name="invoke-method-of-the-cim_action-class"></a><span data-ttu-id="82ebe-104">Metodo Invoke della classe di \_ azione CIM</span><span class="sxs-lookup"><span data-stu-id="82ebe-104">Invoke method of the CIM\_Action class</span></span>

<span data-ttu-id="82ebe-105">Il metodo **Invoke** della classe [**di \_ azione CIM**](cim-action.md) esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="82ebe-105">The **Invoke** method of the [**CIM\_Action**](cim-action.md) class takes a particular action.</span></span> <span data-ttu-id="82ebe-106">I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="82ebe-106">The details of how the method performs the action is implementation-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82ebe-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="82ebe-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="82ebe-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="82ebe-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="82ebe-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="82ebe-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="82ebe-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="82ebe-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="82ebe-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82ebe-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="82ebe-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="82ebe-112">Parameters</span></span>

<span data-ttu-id="82ebe-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="82ebe-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="82ebe-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82ebe-114">Return value</span></span>

<span data-ttu-id="82ebe-115">Restituisce un valore pari a 0 (zero) in caso di esito positivo, 1 (uno) se il metodo non è supportato e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="82ebe-115">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="82ebe-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="82ebe-116">Remarks</span></span>

<span data-ttu-id="82ebe-117">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="82ebe-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="82ebe-118">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="82ebe-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="82ebe-119">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="82ebe-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="82ebe-120">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="82ebe-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="82ebe-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82ebe-121">Requirements</span></span>



| <span data-ttu-id="82ebe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="82ebe-122">Requirement</span></span> | <span data-ttu-id="82ebe-123">Valore</span><span class="sxs-lookup"><span data-stu-id="82ebe-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82ebe-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82ebe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="82ebe-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82ebe-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82ebe-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82ebe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="82ebe-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82ebe-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82ebe-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="82ebe-128">Namespace</span></span><br/>                | <span data-ttu-id="82ebe-129">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="82ebe-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="82ebe-130">MOF</span><span class="sxs-lookup"><span data-stu-id="82ebe-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82ebe-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82ebe-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="82ebe-132">DLL</span><span class="sxs-lookup"><span data-stu-id="82ebe-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82ebe-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82ebe-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82ebe-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82ebe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ebe-135">\_Azione CIM</span><span class="sxs-lookup"><span data-stu-id="82ebe-135">CIM\_Action</span></span>](invoke-method-in-class-cim-action.md)
</dt> <dt>

[<span data-ttu-id="82ebe-136">**\_Azione CIM**</span><span class="sxs-lookup"><span data-stu-id="82ebe-136">**CIM\_Action**</span></span>](cim-action.md)
</dt> <dt>

[<span data-ttu-id="82ebe-137">Classi CIM</span><span class="sxs-lookup"><span data-stu-id="82ebe-137">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 


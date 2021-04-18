---
description: Il metodo Invoke della classe CIM \_ DirectorySpecification valuta un particolare controllo.
ms.assetid: 63289f94-f134-4159-898c-404cdd8f2a5c
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_DirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecification.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48e5cb315f7dba6be187280ee6a16d7c4711752f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304677"
---
# <a name="invoke-method-of-the-cim_directoryspecification-class"></a><span data-ttu-id="94523-103">Metodo Invoke della classe CIM \_ DirectorySpecification</span><span class="sxs-lookup"><span data-stu-id="94523-103">Invoke method of the CIM\_DirectorySpecification class</span></span>

<span data-ttu-id="94523-104">Il metodo **Invoke** della classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) valuta un particolare controllo.</span><span class="sxs-lookup"><span data-stu-id="94523-104">The **Invoke** method of the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class evaluates a particular check.</span></span> <span data-ttu-id="94523-105">Informazioni dettagliate sul modo in cui il metodo valuta un particolare controllo in un contesto CIM sono descritte dalle sottoclassi [**di \_ controllo CIM**](cim-check.md) non astratte.</span><span class="sxs-lookup"><span data-stu-id="94523-105">Details about how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="94523-106">Questo metodo viene ereditato dal **\_ controllo CIM**.</span><span class="sxs-lookup"><span data-stu-id="94523-106">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94523-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="94523-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="94523-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="94523-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="94523-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="94523-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="94523-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="94523-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="94523-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94523-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="94523-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="94523-112">Parameters</span></span>

<span data-ttu-id="94523-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="94523-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="94523-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94523-114">Return value</span></span>

<span data-ttu-id="94523-115">Restituisce 0 se ha esito positivo, 1 se il metodo non è supportato e qualsiasi altro valore indica un errore.</span><span class="sxs-lookup"><span data-stu-id="94523-115">Returns a 0 if successful, a 1 if the method is not supported, and any other value indicates an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="94523-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="94523-116">Remarks</span></span>

<span data-ttu-id="94523-117">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="94523-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="94523-118">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="94523-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="94523-119">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="94523-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="94523-120">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="94523-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="94523-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94523-121">Requirements</span></span>



| <span data-ttu-id="94523-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="94523-122">Requirement</span></span> | <span data-ttu-id="94523-123">Valore</span><span class="sxs-lookup"><span data-stu-id="94523-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94523-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94523-124">Minimum supported client</span></span><br/> | <span data-ttu-id="94523-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94523-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94523-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94523-126">Minimum supported server</span></span><br/> | <span data-ttu-id="94523-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94523-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94523-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="94523-128">Namespace</span></span><br/>                | <span data-ttu-id="94523-129">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="94523-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94523-130">MOF</span><span class="sxs-lookup"><span data-stu-id="94523-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94523-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94523-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94523-132">DLL</span><span class="sxs-lookup"><span data-stu-id="94523-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94523-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94523-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94523-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94523-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94523-135">\_DIRECTORYSPECIFICATION CIM</span><span class="sxs-lookup"><span data-stu-id="94523-135">CIM\_DirectorySpecification</span></span>](invoke-method-in-class-cim-directoryspecification.md)
</dt> <dt>

[<span data-ttu-id="94523-136">**\_DIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="94523-136">**CIM\_DirectorySpecification**</span></span>](cim-directoryspecification.md)
</dt> </dl>

 


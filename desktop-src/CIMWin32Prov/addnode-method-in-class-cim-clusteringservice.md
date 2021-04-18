---
description: Porta un nuovo sistema di computer in un cluster.
ms.assetid: 26d9428e-99de-4dcb-96ed-d773f28e015a
ms.tgt_platform: multiple
title: Metodo AddNode della classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.AddNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1769ebb876fd2ae99c800a61b80d339a850ab232
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304787"
---
# <a name="addnode-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="94535-103">Metodo AddNode della classe CIM \_ ClusteringService</span><span class="sxs-lookup"><span data-stu-id="94535-103">AddNode method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="94535-104">Il metodo **AddNode** porta un nuovo sistema di computer in un cluster.</span><span class="sxs-lookup"><span data-stu-id="94535-104">The **AddNode** method brings a new computer system into a cluster.</span></span> <span data-ttu-id="94535-105">Il nodo da aggiungere viene specificato come parametro per il metodo.</span><span class="sxs-lookup"><span data-stu-id="94535-105">The node to be added is specified as a parameter to the method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94535-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="94535-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="94535-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="94535-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="94535-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="94535-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="94535-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="94535-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="94535-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94535-110">Syntax</span></span>


```mof
uint32 AddNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a><span data-ttu-id="94535-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="94535-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94535-112">*CS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94535-112">*CS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94535-113">Riferimento al sistema del computer da aggiungere al cluster.</span><span class="sxs-lookup"><span data-stu-id="94535-113">Reference to the computer system to add to the cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94535-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94535-114">Return value</span></span>

<span data-ttu-id="94535-115">Restituisce un valore pari a 0 (zero) in caso di esito positivo, 1 (uno) se l'operazione non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="94535-115">Returns a value of 0 (zero) on success, 1 (one) if the operation is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="94535-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="94535-116">Remarks</span></span>

<span data-ttu-id="94535-117">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="94535-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="94535-118">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="94535-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="94535-119">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="94535-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="94535-120">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="94535-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="94535-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94535-121">Requirements</span></span>



| <span data-ttu-id="94535-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="94535-122">Requirement</span></span> | <span data-ttu-id="94535-123">Valore</span><span class="sxs-lookup"><span data-stu-id="94535-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94535-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94535-124">Minimum supported client</span></span><br/> | <span data-ttu-id="94535-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94535-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94535-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94535-126">Minimum supported server</span></span><br/> | <span data-ttu-id="94535-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94535-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94535-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="94535-128">Namespace</span></span><br/>                | <span data-ttu-id="94535-129">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="94535-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94535-130">MOF</span><span class="sxs-lookup"><span data-stu-id="94535-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94535-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94535-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94535-132">DLL</span><span class="sxs-lookup"><span data-stu-id="94535-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94535-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94535-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94535-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94535-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94535-135">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="94535-135">**CIM\_ClusteringService**</span></span>](addnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="94535-136">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="94535-136">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 


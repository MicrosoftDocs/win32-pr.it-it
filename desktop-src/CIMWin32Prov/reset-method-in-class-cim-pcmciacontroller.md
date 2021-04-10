---
description: Il metodo Reset della classe CIM \_ PCMCIAController richiede la reimpostazione del dispositivo logico.
ms.assetid: c58e3265-2849-4154-a03e-2e1cfa9e3d30
ms.tgt_platform: multiple
title: Reimposta il metodo della classe CIM_PCMCIAController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8576bc5c1ce291c355d2907761e5b342ea6f3bc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225664"
---
# <a name="reset-method-of-the-cim_pcmciacontroller-class"></a><span data-ttu-id="15756-103">Metodo Reset della classe CIM \_ PCMCIAController</span><span class="sxs-lookup"><span data-stu-id="15756-103">Reset method of the CIM\_PCMCIAController class</span></span>

<span data-ttu-id="15756-104">Il metodo **Reset** della classe CIM \_ PCMCIAController richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="15756-104">The **Reset** method of the CIM\_PCMCIAController class requests a reset of the logical device.</span></span> <span data-ttu-id="15756-105">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15756-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15756-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="15756-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="15756-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="15756-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="15756-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15756-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="15756-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="15756-109">Parameters</span></span>

<span data-ttu-id="15756-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="15756-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15756-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15756-111">Return value</span></span>

<span data-ttu-id="15756-112">Restituisce 0 (zero) se la richiesta è stata eseguita correttamente, 1 (uno) se la richiesta non è supportata e un altro valore se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="15756-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="15756-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="15756-113">Remarks</span></span>

<span data-ttu-id="15756-114">Questo metodo non è implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="15756-114">This method is not implemented by WMI.</span></span> <span data-ttu-id="15756-115">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="15756-115">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="15756-116">Per le classi WMI derivate da [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md), vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="15756-116">For WMI classes derived from [**CIM\_PCMCIAController**](cim-pcmciacontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="15756-117">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="15756-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="15756-118">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="15756-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="15756-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15756-119">Requirements</span></span>



| <span data-ttu-id="15756-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="15756-120">Requirement</span></span> | <span data-ttu-id="15756-121">Valore</span><span class="sxs-lookup"><span data-stu-id="15756-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15756-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15756-122">Minimum supported client</span></span><br/> | <span data-ttu-id="15756-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15756-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15756-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15756-124">Minimum supported server</span></span><br/> | <span data-ttu-id="15756-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15756-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15756-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="15756-126">Namespace</span></span><br/>                | <span data-ttu-id="15756-127">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="15756-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15756-128">MOF</span><span class="sxs-lookup"><span data-stu-id="15756-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15756-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15756-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15756-130">DLL</span><span class="sxs-lookup"><span data-stu-id="15756-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15756-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15756-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15756-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15756-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15756-133">\_PCMCIACONTROLLER CIM</span><span class="sxs-lookup"><span data-stu-id="15756-133">CIM\_PCMCIAController</span></span>](reset-method-in-class-cim-pcmciacontroller.md)
</dt> <dt>

[<span data-ttu-id="15756-134">**\_PCMCIACONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="15756-134">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> </dl>

 

 





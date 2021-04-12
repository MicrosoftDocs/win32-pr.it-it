---
description: Richiede la reimpostazione del LogicalDevice.
ms.assetid: f7655825-3de5-421f-a3e9-97d2f605affd
title: Metodo Reset della classe CIM_LogicalDevice (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 851332103143e84863762d8cc1183ec3ad841ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347796"
---
# <a name="reset-method-of-the-cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="ae886-103">Metodo Reset della classe CIM_LogicalDevice (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="ae886-103">Reset method of the CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="ae886-104">Richiede la reimpostazione del LogicalDevice.</span><span class="sxs-lookup"><span data-stu-id="ae886-104">Requests a reset of the LogicalDevice.</span></span> <span data-ttu-id="ae886-105">In una sottoclasse è possibile specificare il set di possibili codici restituiti utilizzando un qualificatore ValueMap nel metodo.</span><span class="sxs-lookup"><span data-stu-id="ae886-105">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="ae886-106">Le stringhe a cui è stato convertito il contenuto ValueMap possono anche essere specificate nella sottoclasse come qualificatore della matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="ae886-106">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae886-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae886-107">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="ae886-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae886-108">Parameters</span></span>

<span data-ttu-id="ae886-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ae886-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae886-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae886-110">Return value</span></span>

<span data-ttu-id="ae886-111">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ae886-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae886-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae886-112">Requirements</span></span>



| <span data-ttu-id="ae886-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae886-113">Requirement</span></span> | <span data-ttu-id="ae886-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ae886-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae886-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae886-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ae886-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ae886-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ae886-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae886-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ae886-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ae886-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ae886-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ae886-119">Namespace</span></span><br/>                | <span data-ttu-id="ae886-120">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ae886-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ae886-121">MOF</span><span class="sxs-lookup"><span data-stu-id="ae886-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae886-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae886-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae886-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ae886-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae886-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae886-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ae886-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae886-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae886-126">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ae886-126">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 





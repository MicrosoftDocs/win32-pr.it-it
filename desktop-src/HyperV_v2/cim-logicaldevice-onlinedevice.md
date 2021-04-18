---
description: Il metodo OnlineDevice è stato deprecato al posto del metodo RequestStateChange più generale che si sovrappone direttamente alla funzionalità fornita da questo metodo.
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: Metodo OnlineDevice della classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56e5fae557198a713aec338f92ad8f2865b2c351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317217"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="efc0a-103">Metodo OnlineDevice della classe CIM \_ LogicalDevice</span><span class="sxs-lookup"><span data-stu-id="efc0a-103">OnlineDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="efc0a-104">Il metodo **OnlineDevice** è stato deprecato al posto del metodo **RequestStateChange** più generale che si sovrappone direttamente alla funzionalità fornita da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="efc0a-104">The **OnlineDevice** method has been deprecated in lieu of the more general **RequestStateChange** method that directly overlaps with the functionality provided by this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="efc0a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efc0a-105">Syntax</span></span>


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a><span data-ttu-id="efc0a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="efc0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efc0a-107">In *linea* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efc0a-107">*Online* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efc0a-108">Se **true**, portare il dispositivo online, se **false**, portare il dispositivo offline.</span><span class="sxs-lookup"><span data-stu-id="efc0a-108">If **TRUE**, take the device online, if **FALSE**, take the device offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efc0a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efc0a-109">Return value</span></span>

<span data-ttu-id="efc0a-110">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="efc0a-110">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="efc0a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efc0a-111">Requirements</span></span>



| <span data-ttu-id="efc0a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="efc0a-112">Requirement</span></span> | <span data-ttu-id="efc0a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="efc0a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efc0a-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efc0a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="efc0a-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="efc0a-115">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="efc0a-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efc0a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="efc0a-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="efc0a-117">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="efc0a-118">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="efc0a-118">Namespace</span></span><br/>                | <span data-ttu-id="efc0a-119">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="efc0a-119">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="efc0a-120">MOF</span><span class="sxs-lookup"><span data-stu-id="efc0a-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efc0a-121"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efc0a-121"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="efc0a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="efc0a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efc0a-123"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="efc0a-123"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="efc0a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efc0a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc0a-125">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="efc0a-125">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 





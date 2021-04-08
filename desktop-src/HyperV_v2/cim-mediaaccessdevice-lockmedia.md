---
description: Blocca e sblocca il supporto in un dispositivo di accesso rimovibile.
ms.assetid: 357ee552-82d0-4201-bcc2-0acf208e16a0
title: Metodo LockMedia della classe CIM_MediaAccessDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 12c4aa6c6ba9e57a2ab88e58624b246fb98065f3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104058423"
---
# <a name="lockmedia-method-of-the-cim_mediaaccessdevice-class"></a><span data-ttu-id="c0735-103">Metodo LockMedia della classe CIM \_ MediaAccessDevice</span><span class="sxs-lookup"><span data-stu-id="c0735-103">LockMedia method of the CIM\_MediaAccessDevice class</span></span>

<span data-ttu-id="c0735-104">Blocca e sblocca il supporto in un dispositivo di accesso rimovibile.</span><span class="sxs-lookup"><span data-stu-id="c0735-104">Locks and unlocks the media in a removeable access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0735-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0735-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="c0735-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0735-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0735-107">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0735-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0735-108">Se **true**, blocca il supporto.</span><span class="sxs-lookup"><span data-stu-id="c0735-108">If **TRUE**, locks the media.</span></span> <span data-ttu-id="c0735-109">Se **false**, rilascia il supporto.</span><span class="sxs-lookup"><span data-stu-id="c0735-109">If **FALSE**, releases the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0735-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0735-110">Return value</span></span>

<span data-ttu-id="c0735-111">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="c0735-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0735-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0735-112">Requirements</span></span>



| <span data-ttu-id="c0735-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0735-113">Requirement</span></span> | <span data-ttu-id="c0735-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c0735-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0735-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0735-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c0735-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c0735-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c0735-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0735-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c0735-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c0735-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c0735-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c0735-119">Namespace</span></span><br/>                | <span data-ttu-id="c0735-120">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c0735-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c0735-121">MOF</span><span class="sxs-lookup"><span data-stu-id="c0735-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0735-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0735-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0735-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c0735-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0735-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c0735-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c0735-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0735-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0735-126">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c0735-126">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

 





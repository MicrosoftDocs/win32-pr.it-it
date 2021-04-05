---
description: Blocca o rilascia i supporti.
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: Metodo LockMedia della classe Msvm_DisketteDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4f9bce4e9e46d76c3426271af16c28026c242fa9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103885994"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="ec691-103">Metodo LockMedia della classe MSVM \_ DisketteDrive</span><span class="sxs-lookup"><span data-stu-id="ec691-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="ec691-104">Blocca o rilascia i supporti.</span><span class="sxs-lookup"><span data-stu-id="ec691-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec691-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec691-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="ec691-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec691-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec691-107">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ec691-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec691-108">**true** per bloccare i supporti; **false** per rilasciare il supporto.</span><span class="sxs-lookup"><span data-stu-id="ec691-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec691-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec691-109">Return value</span></span>

<span data-ttu-id="ec691-110">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ec691-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ec691-111">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ec691-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ec691-112">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ec691-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ec691-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec691-113">Requirements</span></span>



| <span data-ttu-id="ec691-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec691-114">Requirement</span></span> | <span data-ttu-id="ec691-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ec691-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec691-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec691-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ec691-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ec691-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ec691-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec691-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ec691-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ec691-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ec691-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ec691-120">Namespace</span></span><br/>                | <span data-ttu-id="ec691-121">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ec691-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ec691-122">MOF</span><span class="sxs-lookup"><span data-stu-id="ec691-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec691-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec691-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec691-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ec691-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec691-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ec691-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ec691-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec691-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec691-127">**\_DisketteDrive MSVM**</span><span class="sxs-lookup"><span data-stu-id="ec691-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 





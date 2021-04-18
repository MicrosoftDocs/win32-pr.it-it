---
description: Blocca o Sblocca il supporto.
ms.assetid: 805efb2d-71a7-4c74-821f-942644928ff9
title: Metodo LockMedia della classe Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7ddc082ca6ceb7141eaa42bdfddf7a97897a9240
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320721"
---
# <a name="lockmedia-method-of-the-msvm_diskdrive-class"></a><span data-ttu-id="f5c9e-103">Metodo LockMedia della classe MSVM \_ DiskDrive</span><span class="sxs-lookup"><span data-stu-id="f5c9e-103">LockMedia method of the Msvm\_DiskDrive class</span></span>

<span data-ttu-id="f5c9e-104">Blocca o Sblocca il supporto.</span><span class="sxs-lookup"><span data-stu-id="f5c9e-104">Locks or unlocks the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c9e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5c9e-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="f5c9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5c9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5c9e-107">*Blocca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5c9e-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c9e-108">**true** per bloccare i supporti; **false** per rilasciare il supporto.</span><span class="sxs-lookup"><span data-stu-id="f5c9e-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5c9e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5c9e-109">Return value</span></span>

<span data-ttu-id="f5c9e-110">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5c9e-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="f5c9e-111">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="f5c9e-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f5c9e-112">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="f5c9e-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f5c9e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5c9e-113">Requirements</span></span>



| <span data-ttu-id="f5c9e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5c9e-114">Requirement</span></span> | <span data-ttu-id="f5c9e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f5c9e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c9e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5c9e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c9e-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f5c9e-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f5c9e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5c9e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c9e-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f5c9e-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f5c9e-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f5c9e-120">Namespace</span></span><br/>                | <span data-ttu-id="f5c9e-121">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f5c9e-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f5c9e-122">MOF</span><span class="sxs-lookup"><span data-stu-id="f5c9e-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5c9e-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5c9e-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5c9e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f5c9e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5c9e-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f5c9e-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f5c9e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5c9e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c9e-127">**\_DiskDrive MSVM**</span><span class="sxs-lookup"><span data-stu-id="f5c9e-127">**Msvm\_DiskDrive**</span></span>](msvm-diskdrive.md)
</dt> </dl>

 

 





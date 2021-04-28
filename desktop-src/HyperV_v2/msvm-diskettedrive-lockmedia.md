---
description: 'Metodo LockMedia della classe Msvm_DisketteDrive : blocca o rilascia il supporto.'
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
ms.openlocfilehash: 5f5f87354aa7c39534e8b32c8985c5d18b55caa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111978"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="255ca-103">Metodo LockMedia della classe Msvm \_ DisketteDrive</span><span class="sxs-lookup"><span data-stu-id="255ca-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="255ca-104">Blocca o rilascia il supporto.</span><span class="sxs-lookup"><span data-stu-id="255ca-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="255ca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="255ca-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="255ca-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="255ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="255ca-107">*Blocco* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="255ca-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="255ca-108">**true** per bloccare il supporto; **false** per rilasciare il supporto.</span><span class="sxs-lookup"><span data-stu-id="255ca-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="255ca-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="255ca-109">Return value</span></span>

<span data-ttu-id="255ca-110">Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="255ca-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="255ca-111">**Completata senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="255ca-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="255ca-112">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="255ca-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="255ca-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="255ca-113">Requirements</span></span>



| <span data-ttu-id="255ca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="255ca-114">Requirement</span></span> | <span data-ttu-id="255ca-115">Valore</span><span class="sxs-lookup"><span data-stu-id="255ca-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="255ca-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="255ca-116">Minimum supported client</span></span><br/> | <span data-ttu-id="255ca-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="255ca-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="255ca-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="255ca-118">Minimum supported server</span></span><br/> | <span data-ttu-id="255ca-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="255ca-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="255ca-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="255ca-120">Namespace</span></span><br/>                | <span data-ttu-id="255ca-121">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="255ca-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="255ca-122">MOF</span><span class="sxs-lookup"><span data-stu-id="255ca-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="255ca-123"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="255ca-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="255ca-124">DLL</span><span class="sxs-lookup"><span data-stu-id="255ca-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="255ca-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="255ca-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="255ca-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="255ca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="255ca-127">**Msvm \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="255ca-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 





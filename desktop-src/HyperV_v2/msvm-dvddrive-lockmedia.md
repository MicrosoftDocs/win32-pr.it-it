---
description: 'Metodo LockMedia della classe Msvm_DVDDrive: blocca o rilascia il supporto.'
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Metodo LockMedia della classe Msvm_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e00780fbeeeec60563b31008c8e5979a09f9d173
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119149"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a><span data-ttu-id="1851d-103">Metodo LockMedia della classe MSvm \_ DVDDrive</span><span class="sxs-lookup"><span data-stu-id="1851d-103">LockMedia method of the Msvm\_DVDDrive class</span></span>

<span data-ttu-id="1851d-104">Blocca o rilascia i supporti.</span><span class="sxs-lookup"><span data-stu-id="1851d-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="1851d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1851d-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="1851d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1851d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1851d-107">*Blocco* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1851d-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1851d-108">**true** per bloccare il supporto; **false** per rilasciare il supporto.</span><span class="sxs-lookup"><span data-stu-id="1851d-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1851d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1851d-109">Return value</span></span>

<span data-ttu-id="1851d-110">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1851d-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="1851d-111">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="1851d-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1851d-112">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="1851d-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1851d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1851d-113">Requirements</span></span>



| <span data-ttu-id="1851d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1851d-114">Requirement</span></span> | <span data-ttu-id="1851d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1851d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1851d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1851d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1851d-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1851d-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1851d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1851d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1851d-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1851d-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1851d-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1851d-120">Namespace</span></span><br/>                | <span data-ttu-id="1851d-121">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1851d-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1851d-122">MOF</span><span class="sxs-lookup"><span data-stu-id="1851d-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1851d-123"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="1851d-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1851d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1851d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1851d-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1851d-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1851d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1851d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1851d-127">**Msvm \_ DVDDrive**</span><span class="sxs-lookup"><span data-stu-id="1851d-127">**Msvm\_DVDDrive**</span></span>](msvm-dvddrive.md)
</dt> </dl>

 

 





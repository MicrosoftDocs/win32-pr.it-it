---
description: Arresta il servizio Guest.
ms.assetid: 67FFA46C-0B61-4845-A617-BA10F4D42CBC
title: 'Metodo Msvm_GuestService:: StopService'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6c396078e2bd623a768f391a645091679694f453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879006"
---
# <a name="msvm_guestservicestopservice-method"></a><span data-ttu-id="19c51-103">\_Metodo MSVM GuestService:: StopService</span><span class="sxs-lookup"><span data-stu-id="19c51-103">Msvm\_GuestService::StopService method</span></span>

<span data-ttu-id="19c51-104">Arresta il servizio Guest.</span><span class="sxs-lookup"><span data-stu-id="19c51-104">Stops the guest service.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c51-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19c51-105">Syntax</span></span>


```C++
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="19c51-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="19c51-106">Parameters</span></span>

<span data-ttu-id="19c51-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="19c51-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="19c51-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19c51-108">Return value</span></span>

<span data-ttu-id="19c51-109">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="19c51-109">This method returns one of the following values.</span></span>



| <span data-ttu-id="19c51-110">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="19c51-110">Return code/value</span></span>                                                                                                                                             | <span data-ttu-id="19c51-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19c51-111">Description</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="19c51-112"><dt>**Completato senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="19c51-112"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="19c51-113">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="19c51-113">Success.</span></span><br/> |
| <dl> <span data-ttu-id="19c51-114"><dt>**Non supportato**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="19c51-114"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>           |                     |



 

## <a name="requirements"></a><span data-ttu-id="19c51-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19c51-115">Requirements</span></span>



| <span data-ttu-id="19c51-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="19c51-116">Requirement</span></span> | <span data-ttu-id="19c51-117">Valore</span><span class="sxs-lookup"><span data-stu-id="19c51-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19c51-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19c51-118">Minimum supported client</span></span><br/> | <span data-ttu-id="19c51-119">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="19c51-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="19c51-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19c51-120">Minimum supported server</span></span><br/> | <span data-ttu-id="19c51-121">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="19c51-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="19c51-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="19c51-122">Namespace</span></span><br/>                | <span data-ttu-id="19c51-123">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="19c51-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="19c51-124">MOF</span><span class="sxs-lookup"><span data-stu-id="19c51-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19c51-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19c51-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="19c51-126">DLL</span><span class="sxs-lookup"><span data-stu-id="19c51-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19c51-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="19c51-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="19c51-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19c51-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c51-129">**\_GuestService MSVM**</span><span class="sxs-lookup"><span data-stu-id="19c51-129">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 





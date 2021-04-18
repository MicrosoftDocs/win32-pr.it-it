---
description: Reimposta la tastiera virtuale.
ms.assetid: 6D4A9F02-53BD-47C2-9C09-F22C3630312F
title: Reimposta il metodo della classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4fe46657177789e49b49ec2c36f0e7a9dc95394f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318345"
---
# <a name="reset-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="98270-103">Metodo Reset della classe della \_ tastiera MSVM</span><span class="sxs-lookup"><span data-stu-id="98270-103">Reset method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="98270-104">Reimposta la tastiera virtuale.</span><span class="sxs-lookup"><span data-stu-id="98270-104">Resets the virtual keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="98270-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98270-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="98270-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="98270-106">Parameters</span></span>

<span data-ttu-id="98270-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="98270-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98270-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98270-108">Return value</span></span>

<span data-ttu-id="98270-109">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="98270-109">A return value of zero indicates success.</span></span> <span data-ttu-id="98270-110">Un valore restituito di uno indica un errore perché il metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="98270-110">A return value of one indicates a failure because the method is not supported.</span></span>

<dl> <dt>

<span data-ttu-id="98270-111">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="98270-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="98270-112">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="98270-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="98270-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98270-113">Requirements</span></span>



| <span data-ttu-id="98270-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="98270-114">Requirement</span></span> | <span data-ttu-id="98270-115">Valore</span><span class="sxs-lookup"><span data-stu-id="98270-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98270-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98270-116">Minimum supported client</span></span><br/> | <span data-ttu-id="98270-117">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98270-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="98270-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98270-118">Minimum supported server</span></span><br/> | <span data-ttu-id="98270-119">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="98270-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="98270-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="98270-120">Namespace</span></span><br/>                | <span data-ttu-id="98270-121">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="98270-121">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="98270-122">MOF</span><span class="sxs-lookup"><span data-stu-id="98270-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98270-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98270-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="98270-124">DLL</span><span class="sxs-lookup"><span data-stu-id="98270-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98270-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="98270-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="98270-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98270-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98270-127">**\_Tastiera MSVM**</span><span class="sxs-lookup"><span data-stu-id="98270-127">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 





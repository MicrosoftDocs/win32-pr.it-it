---
description: Reimposta la tastiera virtuale.
ms.assetid: 2a943dd8-3b94-4b20-8786-7f9d8b0aeaa6
title: Reimposta il metodo della classe Msvm_SyntheticKeyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 05c5b8dbfba04eca6e0b118ae20f2ad172d324e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225912"
---
# <a name="reset-method-of-the-msvm_synthetickeyboard-class"></a><span data-ttu-id="84d25-103">Metodo Reset della \_ classe SyntheticKeyboard di MSVM</span><span class="sxs-lookup"><span data-stu-id="84d25-103">Reset method of the Msvm\_SyntheticKeyboard class</span></span>

<span data-ttu-id="84d25-104">Reimposta la tastiera virtuale.</span><span class="sxs-lookup"><span data-stu-id="84d25-104">Resets the virtual keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="84d25-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84d25-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="84d25-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="84d25-106">Parameters</span></span>

<span data-ttu-id="84d25-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="84d25-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="84d25-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84d25-108">Return value</span></span>

<span data-ttu-id="84d25-109">In caso di esito positivo, restituisce 0; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="84d25-109">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="84d25-110">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="84d25-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84d25-111">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="84d25-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="84d25-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84d25-112">Requirements</span></span>



| <span data-ttu-id="84d25-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="84d25-113">Requirement</span></span> | <span data-ttu-id="84d25-114">Valore</span><span class="sxs-lookup"><span data-stu-id="84d25-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84d25-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84d25-115">Minimum supported client</span></span><br/> | <span data-ttu-id="84d25-116">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="84d25-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="84d25-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84d25-117">Minimum supported server</span></span><br/> | <span data-ttu-id="84d25-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="84d25-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="84d25-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="84d25-119">Namespace</span></span><br/>                | <span data-ttu-id="84d25-120">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="84d25-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="84d25-121">MOF</span><span class="sxs-lookup"><span data-stu-id="84d25-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84d25-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84d25-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84d25-123">DLL</span><span class="sxs-lookup"><span data-stu-id="84d25-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84d25-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84d25-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84d25-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84d25-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84d25-126">**\_SyntheticKeyboard MSVM**</span><span class="sxs-lookup"><span data-stu-id="84d25-126">**Msvm\_SyntheticKeyboard**</span></span>](msvm-synthetickeyboard.md)
</dt> </dl>

 

 





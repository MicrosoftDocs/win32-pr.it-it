---
title: Metodo ChangeProductKeyMethod della classe MDM_WindowsLicensing
description: Questo metodo installa un codice Product Key per i dispositivi Windows 10 desktop. Il punto non viene riavviato. Vedere anche ChangeProductKey.
ms.assetid: 1d9e3243-2ca4-427b-bda2-d33e1e70c80d
keywords:
- Metodo ChangeProductKeyMethod
- Metodo ChangeProductKeyMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, metodo ChangeProductKeyMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.ChangeProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e00345fb0e23655b457e0540c70289a169c54ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478046"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="db8b1-108">Metodo ChangeProductKeyMethod della classe MDM \_ WindowsLicensing</span><span class="sxs-lookup"><span data-stu-id="db8b1-108">ChangeProductKeyMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="db8b1-109">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="db8b1-109">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="db8b1-110">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="db8b1-110">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="db8b1-111">Questo metodo installa un codice Product Key per i dispositivi Windows 10 desktop.</span><span class="sxs-lookup"><span data-stu-id="db8b1-111">This method installs a product key for Windows 10 desktop devices.</span></span> <span data-ttu-id="db8b1-112">Il punto non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="db8b1-112">Dot not reboot.</span></span> <span data-ttu-id="db8b1-113">Vedere anche [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)</span><span class="sxs-lookup"><span data-stu-id="db8b1-113">See also [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)</span></span>

## <a name="syntax"></a><span data-ttu-id="db8b1-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db8b1-114">Syntax</span></span>


```mof
uint32 ChangeProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="db8b1-115">Parametri</span><span class="sxs-lookup"><span data-stu-id="db8b1-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db8b1-116">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db8b1-116">*param* \[in\]</span></span>
<span data-ttu-id="db8b1-117"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="db8b1-117"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="db8b1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db8b1-118">Requirements</span></span>



| <span data-ttu-id="db8b1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="db8b1-119">Requirement</span></span> | <span data-ttu-id="db8b1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="db8b1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db8b1-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db8b1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="db8b1-122">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="db8b1-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db8b1-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db8b1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="db8b1-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="db8b1-124">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="db8b1-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="db8b1-125">Namespace</span></span><br/>                | <span data-ttu-id="db8b1-126">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="db8b1-126">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="db8b1-127">MOF</span><span class="sxs-lookup"><span data-stu-id="db8b1-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db8b1-128"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db8b1-128"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="db8b1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="db8b1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db8b1-130"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db8b1-130"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db8b1-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db8b1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db8b1-132">**\_WINDOWSLICENSING MDM**</span><span class="sxs-lookup"><span data-stu-id="db8b1-132">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> </dl>

 


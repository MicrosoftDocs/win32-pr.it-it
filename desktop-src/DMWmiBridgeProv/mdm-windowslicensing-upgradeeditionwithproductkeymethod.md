---
title: Metodo UpgradeEditionWithProductKeyMethod della classe MDM_WindowsLicensing
description: Immette un codice Product Key per un aggiornamento dell'edizione dei dispositivi desktop Windows 10. Vedere anche UpgradeEditionWithProductKey.
ms.assetid: 6576fb5c-210c-4979-8c01-ed8f78e72c2c
keywords:
- Metodo UpgradeEditionWithProductKeyMethod
- Metodo UpgradeEditionWithProductKeyMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, metodo UpgradeEditionWithProductKeyMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85824fc6fac9e5a15bf2bc890215afcbd0958680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478041"
---
# <a name="upgradeeditionwithproductkeymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="0d3d4-107">Metodo UpgradeEditionWithProductKeyMethod della classe MDM \_ WindowsLicensing</span><span class="sxs-lookup"><span data-stu-id="0d3d4-107">UpgradeEditionWithProductKeyMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="0d3d4-108">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="0d3d4-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0d3d4-109">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="0d3d4-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0d3d4-110">Immette un codice Product Key per un aggiornamento dell'edizione dei dispositivi desktop Windows 10.</span><span class="sxs-lookup"><span data-stu-id="0d3d4-110">Enters a product key for an edition upgrade of Windows 10 desktop devices.</span></span> <span data-ttu-id="0d3d4-111">Vedere anche [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="0d3d4-111">See also, [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d3d4-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d3d4-112">Syntax</span></span>


```mof
uint32 UpgradeEditionWithProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="0d3d4-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d3d4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d3d4-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d3d4-114">*param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3d4-115">Codice Product Key.</span><span class="sxs-lookup"><span data-stu-id="0d3d4-115">The product key.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d3d4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d3d4-116">Requirements</span></span>



| <span data-ttu-id="0d3d4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d3d4-117">Requirement</span></span> | <span data-ttu-id="0d3d4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0d3d4-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d3d4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d3d4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0d3d4-120">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0d3d4-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d3d4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d3d4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0d3d4-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0d3d4-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0d3d4-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0d3d4-123">Namespace</span></span><br/>                | <span data-ttu-id="0d3d4-124">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="0d3d4-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0d3d4-125">MOF</span><span class="sxs-lookup"><span data-stu-id="0d3d4-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d3d4-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d3d4-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d3d4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0d3d4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d3d4-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d3d4-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d3d4-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d3d4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3d4-130">**\_WINDOWSLICENSING MDM**</span><span class="sxs-lookup"><span data-stu-id="0d3d4-130">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="0d3d4-131">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="0d3d4-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


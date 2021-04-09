---
title: Metodo CheckApplicabilityMethod della classe MDM_WindowsLicensing
description: Verifica se il codice Product Key immesso può essere usato per l'aggiornamento di un'edizione, l'attivazione o la modifica di un codice Product Key di Windows 10 per i dispositivi desktop. Vedere anche CheckApplicability.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- Metodo CheckApplicabilityMethod
- Metodo CheckApplicabilityMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, metodo CheckApplicabilityMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae08c4a13d036a7d1185a3d53dee846ea460e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120611"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="3e402-107">Metodo CheckApplicabilityMethod della classe MDM \_ WindowsLicensing</span><span class="sxs-lookup"><span data-stu-id="3e402-107">CheckApplicabilityMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="3e402-108">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="3e402-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3e402-109">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="3e402-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3e402-110">Verifica se il codice Product Key immesso può essere usato per l'aggiornamento di un'edizione, l'attivazione o la modifica di un codice Product Key di Windows 10 per i dispositivi desktop.</span><span class="sxs-lookup"><span data-stu-id="3e402-110">Checks if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span> <span data-ttu-id="3e402-111">Vedere anche [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="3e402-111">See also, [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e402-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e402-112">Syntax</span></span>


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="3e402-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e402-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e402-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e402-114">*param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e402-115">Codice Product Key.</span><span class="sxs-lookup"><span data-stu-id="3e402-115">The product key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e402-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e402-116">Return value</span></span>

<span data-ttu-id="3e402-117">TRUE o FALSE</span><span class="sxs-lookup"><span data-stu-id="3e402-117">TRUE or FALSE</span></span>

## <a name="requirements"></a><span data-ttu-id="3e402-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e402-118">Requirements</span></span>



| <span data-ttu-id="3e402-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e402-119">Requirement</span></span> | <span data-ttu-id="3e402-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3e402-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e402-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e402-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3e402-122">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3e402-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e402-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e402-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3e402-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3e402-124">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3e402-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3e402-125">Namespace</span></span><br/>                | <span data-ttu-id="3e402-126">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="3e402-126">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3e402-127">MOF</span><span class="sxs-lookup"><span data-stu-id="3e402-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e402-128"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e402-128"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e402-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3e402-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e402-130"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e402-130"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e402-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e402-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e402-132">**\_WINDOWSLICENSING MDM**</span><span class="sxs-lookup"><span data-stu-id="3e402-132">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="3e402-133">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="3e402-133">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


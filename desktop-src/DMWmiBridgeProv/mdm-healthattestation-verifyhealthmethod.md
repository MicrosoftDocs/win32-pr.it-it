---
title: Metodo VerifyHealthMethod della classe MDM_HealthAttestation
description: Metodo per notificare al dispositivo di preparare una richiesta di verifica del certificato di integrità. Vedere anche VerifyHealth.
ms.assetid: f5b11081-c664-4525-8f36-5f17c21e7f22
keywords:
- Metodo VerifyHealthMethod
- Metodo VerifyHealthMethod, classe MDM_HealthAttestation
- Classe MDM_HealthAttestation, metodo VerifyHealthMethod
topic_type:
- apiref
api_name:
- MDM_HealthAttestation.VerifyHealthMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d71d3758059706d4ea598e7012433220feb27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301390"
---
# <a name="verifyhealthmethod-method-of-the-mdm_healthattestation-class"></a><span data-ttu-id="d94df-107">Metodo VerifyHealthMethod della classe MDM \_ HealthAttestation</span><span class="sxs-lookup"><span data-stu-id="d94df-107">VerifyHealthMethod method of the MDM\_HealthAttestation class</span></span>

<span data-ttu-id="d94df-108">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="d94df-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d94df-109">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="d94df-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d94df-110">Metodo per notificare al dispositivo di preparare una richiesta di verifica del certificato di integrità.</span><span class="sxs-lookup"><span data-stu-id="d94df-110">Method to notify the device to prepare a health certificate verification request.</span></span> <span data-ttu-id="d94df-111">Vedere anche [VerifyHealth](/windows/client-management/mdm/healthattestation-csp).</span><span class="sxs-lookup"><span data-stu-id="d94df-111">See also, [VerifyHealth](/windows/client-management/mdm/healthattestation-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="d94df-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d94df-112">Syntax</span></span>


```mof
uint32 VerifyHealthMethod();
```



## <a name="parameters"></a><span data-ttu-id="d94df-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="d94df-113">Parameters</span></span>

<span data-ttu-id="d94df-114">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d94df-114">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="d94df-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d94df-115">Requirements</span></span>



| <span data-ttu-id="d94df-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d94df-116">Requirement</span></span> | <span data-ttu-id="d94df-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d94df-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d94df-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d94df-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d94df-119">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d94df-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d94df-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d94df-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d94df-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d94df-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d94df-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d94df-122">Namespace</span></span><br/>                | <span data-ttu-id="d94df-123">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="d94df-123">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d94df-124">MOF</span><span class="sxs-lookup"><span data-stu-id="d94df-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d94df-125"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d94df-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d94df-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d94df-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d94df-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d94df-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d94df-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d94df-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d94df-129">**\_HEALTHATTESTATION MDM**</span><span class="sxs-lookup"><span data-stu-id="d94df-129">**MDM\_HealthAttestation**</span></span>](mdm-healthattestation.md)
</dt> <dt>

[<span data-ttu-id="d94df-130">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="d94df-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


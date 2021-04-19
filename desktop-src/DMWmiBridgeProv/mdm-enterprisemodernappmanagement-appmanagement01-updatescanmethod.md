---
title: Metodo UpdateScanMethod della classe MDM_EnterpriseModernAppManagement_AppManagement01
description: Metodo per avviare l'analisi del Windows Update. Vedere anche UpdateScan.
ms.assetid: 61d17072-0fe5-4d5b-8e9e-fed536883ac9
keywords:
- Metodo UpdateScanMethod
- Metodo UpdateScanMethod, classe MDM_EnterpriseModernAppManagement_AppManagement01
- Classe MDM_EnterpriseModernAppManagement_AppManagement01, metodo UpdateScanMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01.UpdateScanMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af6cb5b744243b78f737ea44fbc27ef40708c6f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302113"
---
# <a name="updatescanmethod-method-of-the-mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="b7e69-107">Metodo UpdateScanMethod della classe MDM \_ EnterpriseModernAppManagement \_ AppManagement01</span><span class="sxs-lookup"><span data-stu-id="b7e69-107">UpdateScanMethod method of the MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="b7e69-108">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b7e69-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b7e69-109">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b7e69-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b7e69-110">Metodo per avviare l'analisi del Windows Update.</span><span class="sxs-lookup"><span data-stu-id="b7e69-110">Method for starting the Windows Update scan.</span></span> <span data-ttu-id="b7e69-111">Vedere anche [UpdateScan](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="b7e69-111">See also, [UpdateScan](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e69-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7e69-112">Syntax</span></span>


```mof
uint32 UpdateScanMethod();
```



## <a name="parameters"></a><span data-ttu-id="b7e69-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7e69-113">Parameters</span></span>

<span data-ttu-id="b7e69-114">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b7e69-114">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e69-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7e69-115">Requirements</span></span>



| <span data-ttu-id="b7e69-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7e69-116">Requirement</span></span> | <span data-ttu-id="b7e69-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b7e69-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e69-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7e69-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e69-119">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b7e69-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7e69-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7e69-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e69-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b7e69-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b7e69-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b7e69-122">Namespace</span></span><br/>                | <span data-ttu-id="b7e69-123">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="b7e69-123">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b7e69-124">MOF</span><span class="sxs-lookup"><span data-stu-id="b7e69-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7e69-125"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7e69-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7e69-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b7e69-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7e69-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7e69-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7e69-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7e69-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e69-129">**\_AppManagement01 ENTERPRISEMODERNAPPMANAGEMENT \_ MDM**</span><span class="sxs-lookup"><span data-stu-id="b7e69-129">**MDM\_EnterpriseModernAppManagement\_AppManagement01**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01.md)
</dt> <dt>

[<span data-ttu-id="b7e69-130">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="b7e69-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


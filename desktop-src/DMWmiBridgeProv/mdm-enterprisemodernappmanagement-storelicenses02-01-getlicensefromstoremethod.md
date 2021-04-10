---
title: Metodo GetLicenseFromStoreMethod della classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
description: Metodo per ottenere una licenza dallo Store. Vedere anche GetLicenseFromStore.
ms.assetid: 4cf8a979-60c1-4ec1-968e-5a90cc671ebf
keywords:
- Metodo GetLicenseFromStoreMethod
- Metodo GetLicenseFromStoreMethod, classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01, metodo GetLicenseFromStoreMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.GetLicenseFromStoreMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8751546bfb57e5c9bf34db97ee6b59dd7e1f580
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120634"
---
# <a name="getlicensefromstoremethod-method-of-the-mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="e6cd1-107">Metodo GetLicenseFromStoreMethod della classe MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="e6cd1-107">GetLicenseFromStoreMethod method of the MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="e6cd1-108">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="e6cd1-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e6cd1-109">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="e6cd1-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e6cd1-110">Metodo per ottenere una licenza dallo Store.</span><span class="sxs-lookup"><span data-stu-id="e6cd1-110">Method for getting a license from the store.</span></span> <span data-ttu-id="e6cd1-111">Vedere anche [GetLicenseFromStore](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="e6cd1-111">See also, [GetLicenseFromStore](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="e6cd1-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6cd1-112">Syntax</span></span>


```mof
uint32 GetLicenseFromStoreMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="e6cd1-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6cd1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6cd1-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6cd1-114">*param* \[in\]</span></span>
<span data-ttu-id="e6cd1-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e6cd1-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e6cd1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6cd1-116">Requirements</span></span>



| <span data-ttu-id="e6cd1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6cd1-117">Requirement</span></span> | <span data-ttu-id="e6cd1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e6cd1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6cd1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6cd1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e6cd1-120">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e6cd1-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6cd1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6cd1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e6cd1-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e6cd1-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e6cd1-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e6cd1-123">Namespace</span></span><br/>                | <span data-ttu-id="e6cd1-124">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="e6cd1-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e6cd1-125">MOF</span><span class="sxs-lookup"><span data-stu-id="e6cd1-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6cd1-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6cd1-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6cd1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e6cd1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6cd1-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6cd1-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6cd1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6cd1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6cd1-130">**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="e6cd1-130">**MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01.md)
</dt> <dt>

[<span data-ttu-id="e6cd1-131">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="e6cd1-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


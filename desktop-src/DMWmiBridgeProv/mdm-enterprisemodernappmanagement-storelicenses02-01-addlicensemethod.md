---
title: Metodo AddLicenseMethod della classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
description: Metodo per l'aggiunta della licenza. Vedere anche AddLicense.
ms.assetid: 325d284d-10ac-4786-8b04-8184ac43b53f
keywords:
- Metodo AddLicenseMethod
- Metodo AddLicenseMethod, classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01, metodo AddLicenseMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.AddLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f104f4e74d0200cc9d00b9f116232aa5308738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302112"
---
# <a name="addlicensemethod-method-of-the-mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="2cb0e-107">Metodo AddLicenseMethod della classe MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="2cb0e-107">AddLicenseMethod method of the MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="2cb0e-108">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="2cb0e-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2cb0e-109">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="2cb0e-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2cb0e-110">Metodo per l'aggiunta della licenza.</span><span class="sxs-lookup"><span data-stu-id="2cb0e-110">Method for adding license.</span></span> <span data-ttu-id="2cb0e-111">Vedere anche [AddLicense](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="2cb0e-111">See also, [AddLicense](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb0e-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cb0e-112">Syntax</span></span>


```mof
uint32 AddLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="2cb0e-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="2cb0e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cb0e-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2cb0e-114">*param* \[in\]</span></span>
<span data-ttu-id="2cb0e-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2cb0e-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2cb0e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cb0e-116">Requirements</span></span>



| <span data-ttu-id="2cb0e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cb0e-117">Requirement</span></span> | <span data-ttu-id="2cb0e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2cb0e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb0e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cb0e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2cb0e-120">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2cb0e-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2cb0e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cb0e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2cb0e-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2cb0e-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2cb0e-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2cb0e-123">Namespace</span></span><br/>                | <span data-ttu-id="2cb0e-124">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="2cb0e-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2cb0e-125">MOF</span><span class="sxs-lookup"><span data-stu-id="2cb0e-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2cb0e-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2cb0e-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2cb0e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2cb0e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cb0e-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cb0e-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cb0e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cb0e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb0e-130">**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="2cb0e-130">**MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01.md)
</dt> <dt>

[<span data-ttu-id="2cb0e-131">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="2cb0e-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


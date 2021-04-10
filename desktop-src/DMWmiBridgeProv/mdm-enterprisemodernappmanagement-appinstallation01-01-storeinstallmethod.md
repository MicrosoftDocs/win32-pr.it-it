---
title: Metodo StoreInstallMethod della classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Metodo per eseguire un'installazione di un'app e una licenza da Windows Store. Vedere anche StoreInstall.
ms.assetid: 4f8aff47-ad16-4fe5-85be-7ddb55ddff24
keywords:
- Metodo StoreInstallMethod
- Metodo StoreInstallMethod, classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01, metodo StoreInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.StoreInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4ae34e8502b7d408a7fb4d96fb9c2c4fadb509
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964617"
---
# <a name="storeinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="5ac6d-107">Metodo StoreInstallMethod della classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="5ac6d-107">StoreInstallMethod method of the MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="5ac6d-108">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="5ac6d-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5ac6d-109">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="5ac6d-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5ac6d-110">Metodo per eseguire un'installazione di un'app e una licenza da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="5ac6d-110">Method to perform an install of an app and a license from the Windows Store.</span></span> <span data-ttu-id="5ac6d-111">Vedere anche [StoreInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="5ac6d-111">See also, [StoreInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ac6d-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ac6d-112">Syntax</span></span>


```mof
uint32 StoreInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="5ac6d-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ac6d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac6d-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ac6d-114">*param* \[in\]</span></span>
<span data-ttu-id="5ac6d-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5ac6d-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5ac6d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ac6d-116">Requirements</span></span>



| <span data-ttu-id="5ac6d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ac6d-117">Requirement</span></span> | <span data-ttu-id="5ac6d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5ac6d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac6d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ac6d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac6d-120">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5ac6d-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5ac6d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ac6d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac6d-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5ac6d-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5ac6d-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5ac6d-123">Namespace</span></span><br/>                | <span data-ttu-id="5ac6d-124">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="5ac6d-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5ac6d-125">MOF</span><span class="sxs-lookup"><span data-stu-id="5ac6d-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ac6d-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ac6d-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ac6d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5ac6d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ac6d-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ac6d-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac6d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ac6d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac6d-130">**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="5ac6d-130">**MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[<span data-ttu-id="5ac6d-131">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="5ac6d-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


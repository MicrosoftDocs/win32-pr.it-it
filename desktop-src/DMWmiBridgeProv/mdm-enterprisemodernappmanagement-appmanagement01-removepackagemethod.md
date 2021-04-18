---
title: Metodo RemovePackageMethod della classe MDM_EnterpriseModernAppManagement_AppManagement01
description: Metodo per la rimozione di pacchetti. Vedere anche RemovePackage.
ms.assetid: 0f48fd9c-5a3f-48e5-a954-e937e79af049
keywords:
- Metodo RemovePackageMethod
- Metodo RemovePackageMethod, classe MDM_EnterpriseModernAppManagement_AppManagement01
- Classe MDM_EnterpriseModernAppManagement_AppManagement01, metodo RemovePackageMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01.RemovePackageMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2cdeb2c1a8dfaebdde73e52b2910da180b638c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302114"
---
# <a name="removepackagemethod-method-of-the-mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="10ac1-107">Metodo RemovePackageMethod della classe MDM \_ EnterpriseModernAppManagement \_ AppManagement01</span><span class="sxs-lookup"><span data-stu-id="10ac1-107">RemovePackageMethod method of the MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="10ac1-108">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="10ac1-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="10ac1-109">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="10ac1-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="10ac1-110">Metodo per la rimozione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="10ac1-110">Method for removing packages.</span></span> <span data-ttu-id="10ac1-111">Vedere anche [RemovePackage](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="10ac1-111">See also [RemovePackage](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="10ac1-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10ac1-112">Syntax</span></span>


```mof
uint32 RemovePackageMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="10ac1-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="10ac1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10ac1-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10ac1-114">*param* \[in\]</span></span>
<span data-ttu-id="10ac1-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="10ac1-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="10ac1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10ac1-116">Requirements</span></span>



| <span data-ttu-id="10ac1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="10ac1-117">Requirement</span></span> | <span data-ttu-id="10ac1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="10ac1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10ac1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10ac1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="10ac1-120">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="10ac1-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="10ac1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10ac1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="10ac1-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="10ac1-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="10ac1-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="10ac1-123">Namespace</span></span><br/>                | <span data-ttu-id="10ac1-124">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="10ac1-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="10ac1-125">MOF</span><span class="sxs-lookup"><span data-stu-id="10ac1-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10ac1-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10ac1-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="10ac1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="10ac1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10ac1-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10ac1-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10ac1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10ac1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ac1-130">**\_AppManagement01 ENTERPRISEMODERNAPPMANAGEMENT \_ MDM**</span><span class="sxs-lookup"><span data-stu-id="10ac1-130">**MDM\_EnterpriseModernAppManagement\_AppManagement01**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01.md)
</dt> </dl>

 


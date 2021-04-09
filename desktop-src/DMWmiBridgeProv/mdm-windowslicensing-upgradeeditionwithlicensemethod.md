---
title: Metodo UpgradeEditionWithLicenseMethod della classe MDM_WindowsLicensing
description: Metodo per fornire una licenza per l'aggiornamento di un'edizione di dispositivi Windows 10 Mobile. Vedere anche UpgradeEditionWithLicense.
ms.assetid: 1a57fb71-eea6-41bf-bc44-6d3a816096a4
keywords:
- Metodo UpgradeEditionWithLicenseMethod
- Metodo UpgradeEditionWithLicenseMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, metodo UpgradeEditionWithLicenseMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b336ee4128aa520ecd463c3607254526c7c3dc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964607"
---
# <a name="upgradeeditionwithlicensemethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="4c8c1-107">Metodo UpgradeEditionWithLicenseMethod della classe MDM \_ WindowsLicensing</span><span class="sxs-lookup"><span data-stu-id="4c8c1-107">UpgradeEditionWithLicenseMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="4c8c1-108">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="4c8c1-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4c8c1-109">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="4c8c1-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4c8c1-110">Metodo per fornire una licenza per l'aggiornamento di un'edizione di dispositivi Windows 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="4c8c1-110">Method for providing a license for an edition upgrade of Windows 10 mobile devices.</span></span> <span data-ttu-id="4c8c1-111">Vedere anche [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="4c8c1-111">See also, [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="4c8c1-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c8c1-112">Syntax</span></span>


```mof
uint32 UpgradeEditionWithLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="4c8c1-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c8c1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c8c1-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c8c1-114">*param* \[in\]</span></span>
<span data-ttu-id="4c8c1-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4c8c1-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="4c8c1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c8c1-116">Requirements</span></span>



| <span data-ttu-id="4c8c1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c8c1-117">Requirement</span></span> | <span data-ttu-id="4c8c1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4c8c1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c8c1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c8c1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4c8c1-120">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4c8c1-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c8c1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c8c1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4c8c1-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4c8c1-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4c8c1-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4c8c1-123">Namespace</span></span><br/>                | <span data-ttu-id="4c8c1-124">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="4c8c1-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="4c8c1-125">MOF</span><span class="sxs-lookup"><span data-stu-id="4c8c1-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c8c1-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c8c1-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c8c1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4c8c1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c8c1-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c8c1-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c8c1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c8c1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c8c1-130">**\_WINDOWSLICENSING MDM**</span><span class="sxs-lookup"><span data-stu-id="4c8c1-130">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="4c8c1-131">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="4c8c1-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


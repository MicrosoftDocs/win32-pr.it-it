---
title: Metodo HostedInstallMethod della classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Metodo per eseguire un'installazione di un pacchetto dell'app da un percorso ospitato, ad esempio un'unità locale, un'origine dati UNC o HTTPS. Vedere anche HostedInstall.
ms.assetid: 1ec16315-75ce-4613-804e-6b587c4071d6
keywords:
- Metodo HostedInstallMethod
- Metodo HostedInstallMethod, classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01, metodo HostedInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.HostedInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597f748a2b5695fd2703f187cfe50db7ad0aa85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302117"
---
# <a name="hostedinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="25b22-107">Metodo HostedInstallMethod della classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="25b22-107">HostedInstallMethod method of the MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="25b22-108">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="25b22-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="25b22-109">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="25b22-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="25b22-110">Metodo per eseguire un'installazione di un pacchetto dell'app da un percorso ospitato, ad esempio un'unità locale, un'origine dati UNC o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="25b22-110">Method to perform an install of an app package from a hosted location, such as a local drive, a UNC, or HTTPS data source.</span></span> <span data-ttu-id="25b22-111">Vedere anche [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="25b22-111">See also, [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="25b22-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25b22-112">Syntax</span></span>


```mof
uint32 HostedInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="25b22-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="25b22-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25b22-114">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25b22-114">*param* \[in\]</span></span>
<span data-ttu-id="25b22-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="25b22-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="25b22-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25b22-116">Requirements</span></span>



| <span data-ttu-id="25b22-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="25b22-117">Requirement</span></span> | <span data-ttu-id="25b22-118">Valore</span><span class="sxs-lookup"><span data-stu-id="25b22-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25b22-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25b22-119">Minimum supported client</span></span><br/> | <span data-ttu-id="25b22-120">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="25b22-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="25b22-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25b22-121">Minimum supported server</span></span><br/> | <span data-ttu-id="25b22-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="25b22-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="25b22-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="25b22-123">Namespace</span></span><br/>                | <span data-ttu-id="25b22-124">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="25b22-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="25b22-125">MOF</span><span class="sxs-lookup"><span data-stu-id="25b22-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25b22-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25b22-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="25b22-127">DLL</span><span class="sxs-lookup"><span data-stu-id="25b22-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25b22-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25b22-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25b22-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25b22-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b22-130">**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="25b22-130">**MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[<span data-ttu-id="25b22-131">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="25b22-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


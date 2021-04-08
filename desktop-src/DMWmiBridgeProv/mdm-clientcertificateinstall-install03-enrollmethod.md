---
title: Metodo EnrollMethod della classe MDM_ClientCertificateInstall_Install03
description: Attiva il dispositivo per avviare la registrazione del certificato.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Metodo EnrollMethod
- Metodo EnrollMethod, classe MDM_ClientCertificateInstall_Install03
- Classe MDM_ClientCertificateInstall_Install03, metodo EnrollMethod
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7903407d5a97f056835e529eb21408bdcbe800ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742639"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="72fa2-106">Metodo EnrollMethod della classe MDM \_ ClientCertificateInstall \_ Install03</span><span class="sxs-lookup"><span data-stu-id="72fa2-106">EnrollMethod method of the MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="72fa2-107">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="72fa2-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="72fa2-108">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="72fa2-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="72fa2-109">Attiva il dispositivo per avviare la registrazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="72fa2-109">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="72fa2-110">Al termine della registrazione del certificato, il dispositivo non invierà una notifica al server MDM.</span><span class="sxs-lookup"><span data-stu-id="72fa2-110">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="72fa2-111">Il server MDM potrebbe successivamente eseguire una query sul dispositivo per verificare se è stato aggiunto un nuovo certificato.</span><span class="sxs-lookup"><span data-stu-id="72fa2-111">The MDM server could later query the device to find out whether new certificate is added.</span></span> <span data-ttu-id="72fa2-112">Vedere anche [**registrazione**](/windows/client-management/mdm/clientcertificateinstall-csp).</span><span class="sxs-lookup"><span data-stu-id="72fa2-112">See also, [**Enroll**](/windows/client-management/mdm/clientcertificateinstall-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="72fa2-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72fa2-113">Syntax</span></span>


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a><span data-ttu-id="72fa2-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="72fa2-114">Parameters</span></span>

<span data-ttu-id="72fa2-115">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="72fa2-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72fa2-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72fa2-116">Return value</span></span>

<span data-ttu-id="72fa2-117">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="72fa2-117">Required.</span></span> <span data-ttu-id="72fa2-118">Attiva il dispositivo per avviare la registrazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="72fa2-118">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="72fa2-119">Al termine della registrazione del certificato, il dispositivo non invierà una notifica al server MDM.</span><span class="sxs-lookup"><span data-stu-id="72fa2-119">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="72fa2-120">Il server MDM potrebbe successivamente eseguire una query sul dispositivo per verificare se è stato aggiunto un nuovo certificato.</span><span class="sxs-lookup"><span data-stu-id="72fa2-120">The MDM server could later query the device to find out whether new certificate is added.</span></span>

## <a name="requirements"></a><span data-ttu-id="72fa2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72fa2-121">Requirements</span></span>



| <span data-ttu-id="72fa2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="72fa2-122">Requirement</span></span> | <span data-ttu-id="72fa2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="72fa2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72fa2-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72fa2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="72fa2-125">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="72fa2-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72fa2-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72fa2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="72fa2-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="72fa2-127">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="72fa2-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="72fa2-128">Namespace</span></span><br/>                | <span data-ttu-id="72fa2-129">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="72fa2-129">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="72fa2-130">MOF</span><span class="sxs-lookup"><span data-stu-id="72fa2-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72fa2-131"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72fa2-131"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="72fa2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="72fa2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72fa2-133"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72fa2-133"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72fa2-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72fa2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72fa2-135">**\_Install03 CLIENTCERTIFICATEINSTALL \_ MDM**</span><span class="sxs-lookup"><span data-stu-id="72fa2-135">**MDM\_ClientCertificateInstall\_Install03**</span></span>](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[<span data-ttu-id="72fa2-136">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="72fa2-136">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


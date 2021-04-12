---
title: Metodo doWipeMethod della classe MDM_RemoteWipe
description: Attiva il dispositivo per avviare la cancellazione remota.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- Metodo doWipeMethod
- Metodo doWipeMethod, classe MDM_RemoteWipe
- Classe MDM_RemoteWipe, metodo doWipeMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f31dcc9dde2fe51ca0d8677df8b27637edd06c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475286"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a><span data-ttu-id="50e52-106">Metodo doWipeMethod della classe MDM \_ RemoteWipe</span><span class="sxs-lookup"><span data-stu-id="50e52-106">doWipeMethod method of the MDM\_RemoteWipe class</span></span>

<span data-ttu-id="50e52-107">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="50e52-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="50e52-108">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="50e52-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="50e52-109">Attiva il dispositivo per avviare la cancellazione remota.</span><span class="sxs-lookup"><span data-stu-id="50e52-109">Triggers the device to start the remote wipe.</span></span> <span data-ttu-id="50e52-110">Vedere anche [contrassegno dowipe](/windows/client-management/mdm/remotewipe-csp).</span><span class="sxs-lookup"><span data-stu-id="50e52-110">See also, [doWipe](/windows/client-management/mdm/remotewipe-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="50e52-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50e52-111">Syntax</span></span>


```mof
uint32 doWipeMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="50e52-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="50e52-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50e52-113">*param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50e52-113">*param* \[in\]</span></span>
<span data-ttu-id="50e52-114"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="50e52-114"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="50e52-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50e52-115">Requirements</span></span>



| <span data-ttu-id="50e52-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="50e52-116">Requirement</span></span> | <span data-ttu-id="50e52-117">Valore</span><span class="sxs-lookup"><span data-stu-id="50e52-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50e52-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50e52-118">Minimum supported client</span></span><br/> | <span data-ttu-id="50e52-119">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="50e52-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="50e52-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50e52-120">Minimum supported server</span></span><br/> | <span data-ttu-id="50e52-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="50e52-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="50e52-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="50e52-122">Namespace</span></span><br/>                | <span data-ttu-id="50e52-123">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="50e52-123">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="50e52-124">MOF</span><span class="sxs-lookup"><span data-stu-id="50e52-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50e52-125"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50e52-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="50e52-126">DLL</span><span class="sxs-lookup"><span data-stu-id="50e52-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50e52-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50e52-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50e52-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50e52-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e52-129">**\_REMOTEWIPE MDM**</span><span class="sxs-lookup"><span data-stu-id="50e52-129">**MDM\_RemoteWipe**</span></span>](mdm-remotewipe.md)
</dt> <dt>

[<span data-ttu-id="50e52-130">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="50e52-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


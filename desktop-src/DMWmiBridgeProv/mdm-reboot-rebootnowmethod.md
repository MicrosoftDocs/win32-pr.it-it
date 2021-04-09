---
title: Metodo RebootNowMethod della classe MDM_Reboot
description: Questo metodo esegue un riavvio del dispositivo.
ms.assetid: b1bacad8-06db-4e56-9f3d-46c9a0036729
keywords:
- Metodo RebootNowMethod
- Metodo RebootNowMethod, classe MDM_Reboot
- Classe MDM_Reboot, metodo RebootNowMethod
topic_type:
- apiref
api_name:
- MDM_Reboot.RebootNowMethod
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d35d297858588ade6655ea84876c6e75abd719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119067"
---
# <a name="rebootnowmethod-method-of-the-mdm_reboot-class"></a><span data-ttu-id="a3e7b-106">Metodo RebootNowMethod della classe di \_ riavvio MDM</span><span class="sxs-lookup"><span data-stu-id="a3e7b-106">RebootNowMethod method of the MDM\_Reboot class</span></span>

<span data-ttu-id="a3e7b-107">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="a3e7b-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a3e7b-108">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="a3e7b-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a3e7b-109">Questo metodo esegue un riavvio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3e7b-109">This method executes a reboot of the device.</span></span> <span data-ttu-id="a3e7b-110">Vedere anche [RebootNow](/windows/client-management/mdm/reboot-csp).</span><span class="sxs-lookup"><span data-stu-id="a3e7b-110">See also, [RebootNow](/windows/client-management/mdm/reboot-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e7b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3e7b-111">Syntax</span></span>


```mof
uint32 RebootNowMethod();
```



## <a name="parameters"></a><span data-ttu-id="a3e7b-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3e7b-112">Parameters</span></span>

<span data-ttu-id="a3e7b-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a3e7b-113">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e7b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3e7b-114">Requirements</span></span>



| <span data-ttu-id="a3e7b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3e7b-115">Requirement</span></span> | <span data-ttu-id="a3e7b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a3e7b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e7b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3e7b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e7b-118">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a3e7b-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a3e7b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3e7b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e7b-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a3e7b-120">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="a3e7b-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a3e7b-121">Namespace</span></span><br/>                | <span data-ttu-id="a3e7b-122">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="a3e7b-122">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="a3e7b-123">MOF</span><span class="sxs-lookup"><span data-stu-id="a3e7b-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3e7b-124"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3e7b-124"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="a3e7b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a3e7b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3e7b-126"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a3e7b-126"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3e7b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3e7b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e7b-128">**\_Riavvio MDM**</span><span class="sxs-lookup"><span data-stu-id="a3e7b-128">**MDM\_Reboot**</span></span>](mdm-reboot.md)
</dt> </dl>

 


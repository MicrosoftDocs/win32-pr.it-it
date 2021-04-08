---
description: Confrontare l'argomento con la configurazione attiva dell'agente di raccolta.
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Metodo IsConfigurationEqual della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: fb471f144a39519f1f724db458b57b624db2846d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747786"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a><span data-ttu-id="f0033-103">Metodo IsConfigurationEqual della classe Control</span><span class="sxs-lookup"><span data-stu-id="f0033-103">IsConfigurationEqual method of the Control class</span></span>

<span data-ttu-id="f0033-104">Confrontare l'argomento con la configurazione attiva dell'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="f0033-104">Compare the argument with the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0033-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0033-105">Syntax</span></span>


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a><span data-ttu-id="f0033-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0033-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0033-107">*Configurazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f0033-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0033-108">Configurazione da confrontare con la configurazione attiva.</span><span class="sxs-lookup"><span data-stu-id="f0033-108">The configuration to compare to the active configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0033-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0033-109">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="f0033-110">0</span><span class="sxs-lookup"><span data-stu-id="f0033-110">0</span></span>

<span data-ttu-id="f0033-111">Errore</span><span class="sxs-lookup"><span data-stu-id="f0033-111">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f0033-112">1</span><span class="sxs-lookup"><span data-stu-id="f0033-112">1</span></span>

<span data-ttu-id="f0033-113">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="f0033-113">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0033-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0033-114">Requirements</span></span>



| <span data-ttu-id="f0033-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0033-115">Requirement</span></span> | <span data-ttu-id="f0033-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f0033-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0033-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0033-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f0033-118">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f0033-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f0033-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0033-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f0033-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f0033-120">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="f0033-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f0033-121">Namespace</span></span><br/>                | <span data-ttu-id="f0033-122">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="f0033-122">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="f0033-123">MOF</span><span class="sxs-lookup"><span data-stu-id="f0033-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0033-124"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0033-124"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0033-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f0033-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0033-126"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0033-126"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f0033-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0033-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0033-128">**Control**</span><span class="sxs-lookup"><span data-stu-id="f0033-128">**Control**</span></span>](control.md)
</dt> </dl>

 

 





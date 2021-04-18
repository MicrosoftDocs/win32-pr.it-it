---
title: Metodo SetLoadBalancingState della classe Win32_TSSessionDirectory
description: Imposta il valore per indicare se il server parteciperà al bilanciamento del carico di Connessione Desktop remoto broker (gestore connessione Desktop remoto).
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetLoadBalancingState
- Metodo SetLoadBalancingState Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo SetLoadBalancingState
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88142f5a9c87b4af2688e06d2766ac38d7e234c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301293"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="45d48-106">Metodo SetLoadBalancingState della \_ classe TSSessionDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="45d48-106">SetLoadBalancingState method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="45d48-107">Imposta il valore per indicare se il server parteciperà al bilanciamento del carico di Connessione Desktop remoto broker (gestore connessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="45d48-107">Sets the value to indicate whether the server will participate in Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="45d48-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45d48-108">Syntax</span></span>


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a><span data-ttu-id="45d48-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="45d48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45d48-110">*StateValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45d48-110">*StateValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45d48-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45d48-111">Type: **uint32**</span></span>

<span data-ttu-id="45d48-112">Indica se il server parteciperà al bilanciamento del carico di gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="45d48-112">Indicates whether the server will participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="45d48-113">0</span><span class="sxs-lookup"><span data-stu-id="45d48-113">0</span></span>
</dt> <dd>

<span data-ttu-id="45d48-114">Il server non parteciperà al bilanciamento del carico di gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="45d48-114">The server will not participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="45d48-115">1</span><span class="sxs-lookup"><span data-stu-id="45d48-115">1</span></span>
</dt> <dd>

<span data-ttu-id="45d48-116">Il server parteciperà al bilanciamento del carico di gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="45d48-116">The server will participate in RD Connection Broker load balancing.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45d48-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="45d48-117">Remarks</span></span>

<span data-ttu-id="45d48-118">Il server deve essere aggiunto a una farm in Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="45d48-118">The server must be joined to a farm in RD Connection Broker.</span></span>

<span data-ttu-id="45d48-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="45d48-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="45d48-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="45d48-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="45d48-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="45d48-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="45d48-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="45d48-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="45d48-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45d48-123">Requirements</span></span>



| <span data-ttu-id="45d48-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="45d48-124">Requirement</span></span> | <span data-ttu-id="45d48-125">Valore</span><span class="sxs-lookup"><span data-stu-id="45d48-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45d48-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45d48-126">Minimum supported client</span></span><br/> | <span data-ttu-id="45d48-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="45d48-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="45d48-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45d48-128">Minimum supported server</span></span><br/> | <span data-ttu-id="45d48-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45d48-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45d48-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="45d48-130">Namespace</span></span><br/>                | <span data-ttu-id="45d48-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="45d48-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="45d48-132">MOF</span><span class="sxs-lookup"><span data-stu-id="45d48-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45d48-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45d48-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="45d48-134">DLL</span><span class="sxs-lookup"><span data-stu-id="45d48-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45d48-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45d48-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45d48-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45d48-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d48-137">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="45d48-137">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 


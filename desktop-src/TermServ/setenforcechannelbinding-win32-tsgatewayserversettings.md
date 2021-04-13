---
title: Metodo SetEnforceChannelBinding della classe Win32_TSGatewayServerSettings
description: Imposta la proprietà EnforceChannelBinding.
ms.assetid: 8bd64fe7-bad5-44e6-a309-10802d9a8bd4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetEnforceChannelBinding
- Metodo SetEnforceChannelBinding Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo SetEnforceChannelBinding
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetEnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b236341f0fdac31f80f7e7d77aa12a4b22eb9731
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518027"
---
# <a name="setenforcechannelbinding-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="0f5f7-106">Metodo SetEnforceChannelBinding della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="0f5f7-106">SetEnforceChannelBinding method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="0f5f7-107">Imposta la proprietà **EnforceChannelBinding** .</span><span class="sxs-lookup"><span data-stu-id="0f5f7-107">Sets the **EnforceChannelBinding** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f5f7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f5f7-108">Syntax</span></span>


```mof
uint32 SetEnforceChannelBinding(
  [in] boolean EnforceChannelBinding
);
```



## <a name="parameters"></a><span data-ttu-id="0f5f7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f5f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f5f7-110">*EnforceChannelBinding* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f5f7-110">*EnforceChannelBinding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f5f7-111">Specifica il nuovo valore della proprietà **EnforceChannelBinding** .</span><span class="sxs-lookup"><span data-stu-id="0f5f7-111">Specifies the new **EnforceChannelBinding** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f5f7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f5f7-112">Return value</span></span>

<span data-ttu-id="0f5f7-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="0f5f7-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0f5f7-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="0f5f7-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0f5f7-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0f5f7-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f5f7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f5f7-116">Requirements</span></span>



| <span data-ttu-id="0f5f7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f5f7-117">Requirement</span></span> | <span data-ttu-id="0f5f7-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0f5f7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f5f7-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f5f7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0f5f7-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0f5f7-120">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0f5f7-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f5f7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0f5f7-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f5f7-122">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="0f5f7-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0f5f7-123">Namespace</span></span><br/>                | <span data-ttu-id="0f5f7-124">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0f5f7-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0f5f7-125">MOF</span><span class="sxs-lookup"><span data-stu-id="0f5f7-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f5f7-126"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f5f7-126"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f5f7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0f5f7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f5f7-128"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f5f7-128"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0f5f7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f5f7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f5f7-130">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="0f5f7-130">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 






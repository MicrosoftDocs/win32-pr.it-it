---
title: Metodo IsTransportEnabled della classe Win32_TSGatewayServerSettings
description: Determina se il trasporto specificato è abilitato.
ms.assetid: 3f08a206-5800-4088-a113-bb3f0cc826f2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsTransportEnabled
- Metodo IsTransportEnabled Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo IsTransportEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsTransportEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da152499138f6c1aba1ff6477c719aa0e787deee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119627"
---
# <a name="istransportenabled-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="dae2f-106">Metodo IsTransportEnabled della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="dae2f-106">IsTransportEnabled method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="dae2f-107">Determina se il trasporto specificato è abilitato.</span><span class="sxs-lookup"><span data-stu-id="dae2f-107">Determines whether the specified transport is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="dae2f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dae2f-108">Syntax</span></span>


```mof
uint32 IsTransportEnabled(
  [in]  uint16  TransportType,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="dae2f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="dae2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dae2f-110">*TransportType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dae2f-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dae2f-111">Specifica il tipo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="dae2f-111">Specifies the transport type.</span></span> <span data-ttu-id="dae2f-112">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="dae2f-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="dae2f-113">0</span><span class="sxs-lookup"><span data-stu-id="dae2f-113">0</span></span>
</dt> <dd>

<span data-ttu-id="dae2f-114">RPC sul trasporto HTTP.</span><span class="sxs-lookup"><span data-stu-id="dae2f-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="dae2f-115">1</span><span class="sxs-lookup"><span data-stu-id="dae2f-115">1</span></span>
</dt> <dd>

<span data-ttu-id="dae2f-116">Trasporto HTTP.</span><span class="sxs-lookup"><span data-stu-id="dae2f-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="dae2f-117">2</span><span class="sxs-lookup"><span data-stu-id="dae2f-117">2</span></span>
</dt> <dd>

<span data-ttu-id="dae2f-118">Trasporto UDP.</span><span class="sxs-lookup"><span data-stu-id="dae2f-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="dae2f-119">*Abilitato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dae2f-119">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dae2f-120">Valore **booleano** che indica se il trasporto è abilitato.</span><span class="sxs-lookup"><span data-stu-id="dae2f-120">A **boolean** value that indicates whether the transport is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dae2f-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dae2f-121">Return value</span></span>

<span data-ttu-id="dae2f-122">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="dae2f-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="dae2f-123">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="dae2f-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="dae2f-124">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="dae2f-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dae2f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dae2f-125">Requirements</span></span>



| <span data-ttu-id="dae2f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae2f-126">Requirement</span></span> | <span data-ttu-id="dae2f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="dae2f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae2f-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dae2f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dae2f-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dae2f-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="dae2f-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dae2f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dae2f-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dae2f-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="dae2f-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dae2f-132">Namespace</span></span><br/>                | <span data-ttu-id="dae2f-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="dae2f-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="dae2f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="dae2f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dae2f-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dae2f-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="dae2f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dae2f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dae2f-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dae2f-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="dae2f-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dae2f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae2f-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="dae2f-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 






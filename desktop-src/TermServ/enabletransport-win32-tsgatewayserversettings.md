---
title: Metodo EnableTransport della classe Win32_TSGatewayServerSettings
description: Abilita o Disabilita il trasporto specificato.
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo EnableTransport
- Metodo EnableTransport Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo EnableTransport
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableTransport
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a14e7ee94eb02e1358d66b9965ecc2323d5b773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302747"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="f94a9-106">Metodo EnableTransport della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="f94a9-106">EnableTransport method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="f94a9-107">Abilita o Disabilita il trasporto specificato.</span><span class="sxs-lookup"><span data-stu-id="f94a9-107">Enables or disables the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="f94a9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f94a9-108">Syntax</span></span>


```mof
uint32 EnableTransport(
  [in] uint16  TransportType,
  [in] boolean Enable
);
```



## <a name="parameters"></a><span data-ttu-id="f94a9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f94a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f94a9-110">*TransportType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f94a9-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f94a9-111">Specifica il tipo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="f94a9-111">Specifies the transport type.</span></span> <span data-ttu-id="f94a9-112">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f94a9-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="f94a9-113">0</span><span class="sxs-lookup"><span data-stu-id="f94a9-113">0</span></span>
</dt> <dd>

<span data-ttu-id="f94a9-114">RPC sul trasporto HTTP.</span><span class="sxs-lookup"><span data-stu-id="f94a9-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="f94a9-115">1</span><span class="sxs-lookup"><span data-stu-id="f94a9-115">1</span></span>
</dt> <dd>

<span data-ttu-id="f94a9-116">Trasporto HTTP.</span><span class="sxs-lookup"><span data-stu-id="f94a9-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="f94a9-117">2</span><span class="sxs-lookup"><span data-stu-id="f94a9-117">2</span></span>
</dt> <dd>

<span data-ttu-id="f94a9-118">Trasporto UDP.</span><span class="sxs-lookup"><span data-stu-id="f94a9-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f94a9-119">*Abilita* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f94a9-119">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f94a9-120">Specifica se il trasporto è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="f94a9-120">Specifies if the transport is enabled or disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f94a9-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f94a9-121">Return value</span></span>

<span data-ttu-id="f94a9-122">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="f94a9-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f94a9-123">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f94a9-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f94a9-124">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f94a9-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f94a9-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f94a9-125">Requirements</span></span>



| <span data-ttu-id="f94a9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f94a9-126">Requirement</span></span> | <span data-ttu-id="f94a9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f94a9-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f94a9-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f94a9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f94a9-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f94a9-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f94a9-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f94a9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f94a9-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f94a9-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="f94a9-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f94a9-132">Namespace</span></span><br/>                | <span data-ttu-id="f94a9-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f94a9-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f94a9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f94a9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f94a9-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f94a9-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f94a9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f94a9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f94a9-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f94a9-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f94a9-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f94a9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f94a9-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="f94a9-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 






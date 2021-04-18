---
title: Metodo SetIPAndPort della classe Win32_TSGatewayServerSettings
description: Imposta l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetIPAndPort
- Metodo SetIPAndPort Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo SetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88870cce628a94ca34b38ccf315edc87a1a734b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517686"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="7b6c1-106">Metodo SetIPAndPort della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="7b6c1-106">SetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="7b6c1-107">Imposta l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-107">Sets the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b6c1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b6c1-108">Syntax</span></span>


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
);
```



## <a name="parameters"></a><span data-ttu-id="7b6c1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b6c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b6c1-110">*TransportType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b6c1-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b6c1-111">Specifica il tipo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-111">Specifies the transport type.</span></span> <span data-ttu-id="7b6c1-112">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="7b6c1-113">0</span><span class="sxs-lookup"><span data-stu-id="7b6c1-113">0</span></span>
</dt> <dd>

<span data-ttu-id="7b6c1-114">RPC sul trasporto HTTP.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="7b6c1-115">1</span><span class="sxs-lookup"><span data-stu-id="7b6c1-115">1</span></span>
</dt> <dd>

<span data-ttu-id="7b6c1-116">Trasporto HTTP.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="7b6c1-117">2</span><span class="sxs-lookup"><span data-stu-id="7b6c1-117">2</span></span>
</dt> <dd>

<span data-ttu-id="7b6c1-118">Trasporto UDP.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7b6c1-119">*Indirizzo IP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b6c1-119">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b6c1-120">Specifica l'indirizzo IP di ascolto, in formato ottetto (ad esempio, "192.168.1.1").</span><span class="sxs-lookup"><span data-stu-id="7b6c1-120">Specifies the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="7b6c1-121">*Porta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b6c1-121">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b6c1-122">Specifica il numero della porta di attesa.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-122">Specifies the listening port number.</span></span>

</dd> <dt>

<span data-ttu-id="7b6c1-123">*OverrideExisting* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b6c1-123">*OverrideExisting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b6c1-124">Indica se eseguire l'override dell'associazione IP/porta esistente per HTTP.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-124">Indicates whether to override the existing IP/Port binding for HTTP.</span></span> <span data-ttu-id="7b6c1-125">Questo parametro viene usato solo se il parametro *TransportType* contiene 0 (RPC su http) o 1 (http).</span><span class="sxs-lookup"><span data-stu-id="7b6c1-125">This parameter is only used if the *TransportType* parameter contains 0 (RPC over HTTP) or 1 (HTTP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b6c1-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b6c1-126">Return value</span></span>

<span data-ttu-id="7b6c1-127">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-127">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7b6c1-128">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-128">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7b6c1-129">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7b6c1-129">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b6c1-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b6c1-130">Requirements</span></span>



| <span data-ttu-id="7b6c1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b6c1-131">Requirement</span></span> | <span data-ttu-id="7b6c1-132">Valore</span><span class="sxs-lookup"><span data-stu-id="7b6c1-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b6c1-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b6c1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7b6c1-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7b6c1-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7b6c1-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b6c1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7b6c1-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b6c1-136">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="7b6c1-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7b6c1-137">Namespace</span></span><br/>                | <span data-ttu-id="7b6c1-138">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7b6c1-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7b6c1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7b6c1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b6c1-140"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b6c1-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b6c1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7b6c1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b6c1-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b6c1-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7b6c1-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b6c1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b6c1-144">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="7b6c1-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 






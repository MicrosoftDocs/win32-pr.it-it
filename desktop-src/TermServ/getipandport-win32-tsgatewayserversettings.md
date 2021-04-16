---
title: Metodo GetIPAndPort della classe Win32_TSGatewayServerSettings
description: Ottiene l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetIPAndPort
- Metodo GetIPAndPort Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo GetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260cc45961720ae8d175d4df3e84edc7a0c15c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340462"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="e42f5-106">Metodo GetIPAndPort della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="e42f5-106">GetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="e42f5-107">Ottiene l'indirizzo IP di ascolto e il numero di porta per il trasporto specificato.</span><span class="sxs-lookup"><span data-stu-id="e42f5-107">Obtains the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="e42f5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e42f5-108">Syntax</span></span>


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
);
```



## <a name="parameters"></a><span data-ttu-id="e42f5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e42f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e42f5-110">*TransportType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e42f5-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e42f5-111">Specifica il tipo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="e42f5-111">Specifies the transport type.</span></span> <span data-ttu-id="e42f5-112">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e42f5-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="e42f5-113">0</span><span class="sxs-lookup"><span data-stu-id="e42f5-113">0</span></span>
</dt> <dd>

<span data-ttu-id="e42f5-114">RPC sul trasporto HTTP.</span><span class="sxs-lookup"><span data-stu-id="e42f5-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="e42f5-115">1</span><span class="sxs-lookup"><span data-stu-id="e42f5-115">1</span></span>
</dt> <dd>

<span data-ttu-id="e42f5-116">Trasporto HTTP.</span><span class="sxs-lookup"><span data-stu-id="e42f5-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="e42f5-117">2</span><span class="sxs-lookup"><span data-stu-id="e42f5-117">2</span></span>
</dt> <dd>

<span data-ttu-id="e42f5-118">Trasporto UDP.</span><span class="sxs-lookup"><span data-stu-id="e42f5-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e42f5-119">*Indirizzo IP* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e42f5-119">*IPAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e42f5-120">Stringa che riceve l'indirizzo IP di ascolto, in formato ottetto (ad esempio, "192.168.1.1").</span><span class="sxs-lookup"><span data-stu-id="e42f5-120">A string that receives the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="e42f5-121">*Porta* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e42f5-121">*Port* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e42f5-122">Specifica il numero della porta di attesa.</span><span class="sxs-lookup"><span data-stu-id="e42f5-122">Specifies the listening port number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e42f5-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e42f5-123">Return value</span></span>

<span data-ttu-id="e42f5-124">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="e42f5-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e42f5-125">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e42f5-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e42f5-126">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e42f5-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e42f5-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e42f5-127">Requirements</span></span>



| <span data-ttu-id="e42f5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e42f5-128">Requirement</span></span> | <span data-ttu-id="e42f5-129">Valore</span><span class="sxs-lookup"><span data-stu-id="e42f5-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e42f5-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e42f5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e42f5-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e42f5-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e42f5-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e42f5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e42f5-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e42f5-133">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="e42f5-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e42f5-134">Namespace</span></span><br/>                | <span data-ttu-id="e42f5-135">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e42f5-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e42f5-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e42f5-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e42f5-137"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e42f5-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e42f5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e42f5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e42f5-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e42f5-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e42f5-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e42f5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e42f5-141">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="e42f5-141">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 






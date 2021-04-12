---
title: Metodo getprotocolname della classe Win32_TSGatewayServerSettings
description: Restituisce il nome del protocollo per l'indice di protocollo specificato.
ms.assetid: 6778cede-cc61-4e5d-9a29-ba88197fa8c6
ms.tgt_platform: multiple
keywords:
- Metodo getprotocolname Servizi Desktop remoto
- Metodo getprotocolname Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo getprotocolname
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetProtocolName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81064581b209f047ac492faee6d442b082d038cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120206"
---
# <a name="getprotocolname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="cf742-106">Metodo getprotocolname della \_ classe TSGatewayServerSettings di Win32</span><span class="sxs-lookup"><span data-stu-id="cf742-106">GetProtocolName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="cf742-107">Restituisce il nome del protocollo per l'indice di protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="cf742-107">Returns the protocol name for the specified protocol index.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf742-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf742-108">Syntax</span></span>


```mof
uint32 GetProtocolName(
  [in]  uint32 ProtocolId,
  [out] string ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="cf742-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf742-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf742-110">*ProtocolId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf742-110">*ProtocolId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf742-111">Indice dell'identificatore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="cf742-111">Index of the protocol identifier.</span></span> <span data-ttu-id="cf742-112">Il valore deve essere compreso tra zero e il valore della proprietà **MaxProtocols** .</span><span class="sxs-lookup"><span data-stu-id="cf742-112">The value must be between zero and the value of the **MaxProtocols** property.</span></span>

</dd> <dt>

<span data-ttu-id="cf742-113">*ProtocolName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf742-113">*ProtocolName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf742-114">Restituisce il nome del protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="cf742-114">Returns the name of the specified protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf742-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf742-115">Return value</span></span>

<span data-ttu-id="cf742-116">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="cf742-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="cf742-117">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="cf742-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="cf742-118">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cf742-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf742-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf742-119">Remarks</span></span>

<span data-ttu-id="cf742-120">È supportato un protocollo.</span><span class="sxs-lookup"><span data-stu-id="cf742-120">One protocol is supported.</span></span>

<span data-ttu-id="cf742-121">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="cf742-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="cf742-122">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="cf742-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cf742-123">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="cf742-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cf742-124">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="cf742-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cf742-125">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cf742-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf742-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf742-126">Requirements</span></span>



| <span data-ttu-id="cf742-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf742-127">Requirement</span></span> | <span data-ttu-id="cf742-128">Valore</span><span class="sxs-lookup"><span data-stu-id="cf742-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf742-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf742-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cf742-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cf742-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="cf742-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf742-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cf742-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf742-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="cf742-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cf742-133">Namespace</span></span><br/>                | <span data-ttu-id="cf742-134">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cf742-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="cf742-135">MOF</span><span class="sxs-lookup"><span data-stu-id="cf742-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf742-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf742-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf742-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cf742-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf742-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf742-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="cf742-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf742-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf742-140">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="cf742-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


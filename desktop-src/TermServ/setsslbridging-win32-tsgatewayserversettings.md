---
title: Metodo SetSslBridging della classe Win32_TSGatewayServerSettings
description: Imposta il tipo di bridging SSL che verrà utilizzato dal server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSslBridging
- Metodo SetSslBridging Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo SetSslBridging
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetSslBridging
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77181fb8d8661ec7ea7dc0ce70532281fb9c1bde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400728"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="3145c-106">Metodo SetSslBridging della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="3145c-106">SetSslBridging method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="3145c-107">Imposta il tipo di bridging SSL che verrà utilizzato dal server Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="3145c-107">Sets the type of SSL bridging to be used by the Remote Desktop Gateway (RD Gateway) server.</span></span> <span data-ttu-id="3145c-108">Questo valore viene archiviato nella proprietà **SslBridging** .</span><span class="sxs-lookup"><span data-stu-id="3145c-108">This value is stored in the **SslBridging** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3145c-109">Quando il tipo di bridging SSL viene modificato con questo metodo, il servizio Gateway Desktop remoto deve essere riavviato per rendere effettiva la modifica.</span><span class="sxs-lookup"><span data-stu-id="3145c-109">When the SSL bridging type is changed with this method, the RD Gateway service must be restarted to make this change take effect.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3145c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3145c-110">Syntax</span></span>


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a><span data-ttu-id="3145c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="3145c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3145c-112">*SslBridging* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3145c-112">*SslBridging* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3145c-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3145c-113">Type: **uint32**</span></span>

<span data-ttu-id="3145c-114">Specifica il nuovo valore di bridging SSL.</span><span class="sxs-lookup"><span data-stu-id="3145c-114">Specifies the new SSL bridging value.</span></span> <span data-ttu-id="3145c-115">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3145c-115">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="3145c-116">0</span><span class="sxs-lookup"><span data-stu-id="3145c-116">0</span></span>
</dt> <dd>

<span data-ttu-id="3145c-117">Nessun bridging SSL.</span><span class="sxs-lookup"><span data-stu-id="3145c-117">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="3145c-118">1</span><span class="sxs-lookup"><span data-stu-id="3145c-118">1</span></span>
</dt> <dd>

<span data-ttu-id="3145c-119">Bridging da HTTPS a HTTP.</span><span class="sxs-lookup"><span data-stu-id="3145c-119">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="3145c-120">2</span><span class="sxs-lookup"><span data-stu-id="3145c-120">2</span></span>
</dt> <dd>

<span data-ttu-id="3145c-121">Bridging da HTTPS a HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3145c-121">HTTPS to HTTPS bridging.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3145c-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3145c-122">Return value</span></span>

<span data-ttu-id="3145c-123">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3145c-123">Type: **uint32**</span></span>

<span data-ttu-id="3145c-124">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="3145c-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3145c-125">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="3145c-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3145c-126">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3145c-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3145c-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="3145c-127">Remarks</span></span>

<span data-ttu-id="3145c-128">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="3145c-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3145c-129">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3145c-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3145c-130">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="3145c-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3145c-131">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="3145c-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3145c-132">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3145c-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3145c-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3145c-133">Requirements</span></span>



| <span data-ttu-id="3145c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3145c-134">Requirement</span></span> | <span data-ttu-id="3145c-135">Valore</span><span class="sxs-lookup"><span data-stu-id="3145c-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3145c-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3145c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3145c-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3145c-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3145c-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3145c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3145c-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3145c-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="3145c-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3145c-140">Namespace</span></span><br/>                | <span data-ttu-id="3145c-141">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3145c-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3145c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3145c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3145c-143"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3145c-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3145c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3145c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3145c-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3145c-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3145c-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3145c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3145c-147">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="3145c-147">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


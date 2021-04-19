---
title: Metodo SetMaxConnections della classe Win32_TSGatewayServerSettings
description: Imposta le proprietà MaxConnections e UnlimitedConnections, che controllano il numero massimo di connessioni consentite al server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: cfdbacb7-4969-4ec5-8301-e8020f3af0cd
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetMaxConnections
- Metodo SetMaxConnections Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo SetMaxConnections
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetMaxConnections
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e8a2fa18491232a058913fd338bb871b0a98aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301975"
---
# <a name="setmaxconnections-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="3f806-106">Metodo SetMaxConnections della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="3f806-106">SetMaxConnections method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="3f806-107">Imposta le proprietà **MaxConnections** e **UnlimitedConnections** , che controllano il numero massimo di connessioni consentite al server Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="3f806-107">Sets the **MaxConnections** and **UnlimitedConnections** properties, which control the maximum number of allowed connections to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f806-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f806-108">Syntax</span></span>


```mof
uint32 SetMaxConnections(
  [in] uint32  Connections,
  [in] boolean IsUnlimited
);
```



## <a name="parameters"></a><span data-ttu-id="3f806-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f806-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f806-110">*Connessioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3f806-110">*Connections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f806-111">Numero di connessioni accettate dal server.</span><span class="sxs-lookup"><span data-stu-id="3f806-111">Number of connections that this server should accept.</span></span> <span data-ttu-id="3f806-112">Per un numero illimitato di connessioni, impostare il parametro *Unlimited* su **true**.</span><span class="sxs-lookup"><span data-stu-id="3f806-112">For an unlimited number of connections, set the *IsUnlimited* parameter to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="3f806-113">*Senza limiti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f806-113">*IsUnlimited* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f806-114">Se **true**, le connessioni al servizio non sono limitate a un numero specifico.</span><span class="sxs-lookup"><span data-stu-id="3f806-114">If **True**, connections to the service are not limited to a specific number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f806-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f806-115">Return value</span></span>

<span data-ttu-id="3f806-116">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="3f806-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3f806-117">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="3f806-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3f806-118">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3f806-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f806-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f806-119">Remarks</span></span>

<span data-ttu-id="3f806-120">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="3f806-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3f806-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3f806-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3f806-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="3f806-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3f806-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="3f806-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3f806-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3f806-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f806-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f806-125">Requirements</span></span>



| <span data-ttu-id="3f806-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f806-126">Requirement</span></span> | <span data-ttu-id="3f806-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3f806-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f806-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f806-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3f806-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3f806-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3f806-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f806-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3f806-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f806-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3f806-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3f806-132">Namespace</span></span><br/>                | <span data-ttu-id="3f806-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3f806-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3f806-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3f806-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f806-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f806-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f806-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3f806-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f806-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f806-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3f806-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f806-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f806-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="3f806-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


---
title: Metodo EnableCentralCAP della classe Win32_TSGatewayServerSettings
description: Controlla la proprietà CentralCAPEnabled, che controlla i criteri di autorizzazione della connessione Servizi Desktop remoto (RD \ 160; CAPs) per il server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: 43e476df-714d-43bd-b40f-33511b7757a4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo EnableCentralCAP
- Metodo EnableCentralCAP Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo EnableCentralCAP
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableCentralCAP
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 933e91a89f9a5afdcd2ae85fa6cb097ef0c29cd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400941"
---
# <a name="enablecentralcap-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="35a29-106">Metodo EnableCentralCAP della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="35a29-106">EnableCentralCAP method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="35a29-107">Controlla la proprietà **CentralCAPEnabled** , che controlla i criteri di autorizzazione della connessione Servizi Desktop remoto (Rd) per il server gateway di desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="35a29-107">Controls the **CentralCAPEnabled** property, which controls the Remote Desktop Services connection authorization policies (RD CAPs) for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a29-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35a29-108">Syntax</span></span>


```mof
uint32 EnableCentralCAP(
  [in] boolean CentralCAPEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="35a29-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="35a29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a29-110">*CentralCAPEnabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35a29-110">*CentralCAPEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a29-111">Se è impostato su **true**, verranno utilizzati i criteri di autorizzazione connessioni Desktop remoto dai server terminal centrali.</span><span class="sxs-lookup"><span data-stu-id="35a29-111">If set to **True**, RD CAPs from central RD CAP servers will be used.</span></span> <span data-ttu-id="35a29-112">Se impostato su **false**, verranno utilizzati solo i criteri del server locale.</span><span class="sxs-lookup"><span data-stu-id="35a29-112">If set to **False**, only policies from the local server will be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a29-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35a29-113">Return value</span></span>

<span data-ttu-id="35a29-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="35a29-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="35a29-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="35a29-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="35a29-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="35a29-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="35a29-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="35a29-117">Remarks</span></span>

<span data-ttu-id="35a29-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="35a29-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="35a29-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="35a29-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="35a29-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="35a29-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="35a29-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="35a29-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="35a29-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="35a29-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="35a29-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35a29-123">Requirements</span></span>



| <span data-ttu-id="35a29-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="35a29-124">Requirement</span></span> | <span data-ttu-id="35a29-125">Valore</span><span class="sxs-lookup"><span data-stu-id="35a29-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35a29-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35a29-126">Minimum supported client</span></span><br/> | <span data-ttu-id="35a29-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="35a29-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="35a29-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35a29-128">Minimum supported server</span></span><br/> | <span data-ttu-id="35a29-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35a29-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="35a29-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="35a29-130">Namespace</span></span><br/>                | <span data-ttu-id="35a29-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="35a29-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="35a29-132">MOF</span><span class="sxs-lookup"><span data-stu-id="35a29-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35a29-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35a29-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="35a29-134">DLL</span><span class="sxs-lookup"><span data-stu-id="35a29-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35a29-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35a29-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="35a29-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35a29-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a29-137">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="35a29-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


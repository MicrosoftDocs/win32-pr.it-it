---
title: Metodo SetCertificateACL della classe Win32_TSGatewayServerSettings
description: Imposta il certificato necessario per accedere al server gateway di Desktop remoto (Gateway Desktop remoto).
ms.assetid: 274c24bf-4e44-42ea-a109-99d0249c2f78
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetCertificateACL
- Metodo SetCertificateACL Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo SetCertificateACL
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificateACL
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7a43e737b39b9bea18ee3925b5c3f55440d2a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048727"
---
# <a name="setcertificateacl-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="3d20b-106">Metodo SetCertificateACL della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="3d20b-106">SetCertificateACL method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="3d20b-107">Imposta il certificato necessario per accedere al server gateway di Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="3d20b-107">Sets the certificate that is required to access the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d20b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d20b-108">Syntax</span></span>


```mof
uint32 SetCertificateACL(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="3d20b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d20b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d20b-110">*Certhash* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d20b-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d20b-111">Hash del certificato utilizzato dal server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="3d20b-111">Hash of the certificate that is used by the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d20b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d20b-112">Return value</span></span>

<span data-ttu-id="3d20b-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="3d20b-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3d20b-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="3d20b-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3d20b-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3d20b-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3d20b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d20b-116">Remarks</span></span>

<span data-ttu-id="3d20b-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="3d20b-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3d20b-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3d20b-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3d20b-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="3d20b-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3d20b-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="3d20b-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3d20b-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3d20b-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d20b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d20b-122">Requirements</span></span>



| <span data-ttu-id="3d20b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d20b-123">Requirement</span></span> | <span data-ttu-id="3d20b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3d20b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d20b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d20b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3d20b-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3d20b-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3d20b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d20b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3d20b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d20b-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3d20b-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3d20b-129">Namespace</span></span><br/>                | <span data-ttu-id="3d20b-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3d20b-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3d20b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3d20b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d20b-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d20b-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d20b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3d20b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d20b-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d20b-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3d20b-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d20b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d20b-136">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="3d20b-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


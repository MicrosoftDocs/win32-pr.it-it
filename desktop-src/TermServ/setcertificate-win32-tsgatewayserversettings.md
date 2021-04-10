---
title: Metodo secertificate della classe Win32_TSGatewayServerSettings
description: Imposta l'hash del certificato per il binding HTTPS sulla porta 443 in IIS.
ms.assetid: b5f794bc-17b1-401a-92d8-c9bbe5d0d05f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto metodo secertificate
- Servizi Desktop remoto metodo secertificate, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo secertificate
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1da7e3abcca671b0c8bf70461c77d56e68cf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121215"
---
# <a name="setcertificate-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="3247d-106">Metodo secertificate della \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="3247d-106">SetCertificate method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="3247d-107">Imposta l'hash del certificato per il binding HTTPS sulla porta 443 in IIS.</span><span class="sxs-lookup"><span data-stu-id="3247d-107">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="3247d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3247d-108">Syntax</span></span>


```mof
uint32 SetCertificate(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="3247d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3247d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3247d-110">*Certhash* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3247d-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3247d-111">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="3247d-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="3247d-112">Nuovo hash del certificato.</span><span class="sxs-lookup"><span data-stu-id="3247d-112">The new certificate hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3247d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3247d-113">Return value</span></span>

<span data-ttu-id="3247d-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3247d-114">Type: **uint32**</span></span>

<span data-ttu-id="3247d-115">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="3247d-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3247d-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="3247d-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3247d-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3247d-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3247d-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="3247d-118">Remarks</span></span>

<span data-ttu-id="3247d-119">Dopo aver impostato l'hash del certificato con questo metodo, è necessario chiamare il metodo [**Configure**](configure-win32-tsgatewayserversettings.md) per completare il processo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="3247d-119">After the certificate hash has been set with this method, you must call the [**Configure**](configure-win32-tsgatewayserversettings.md) method to complete the configuration process.</span></span>

<span data-ttu-id="3247d-120">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="3247d-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3247d-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3247d-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3247d-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="3247d-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3247d-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="3247d-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3247d-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3247d-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3247d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3247d-125">Requirements</span></span>



| <span data-ttu-id="3247d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3247d-126">Requirement</span></span> | <span data-ttu-id="3247d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3247d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3247d-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3247d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3247d-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3247d-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3247d-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3247d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3247d-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3247d-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="3247d-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3247d-132">Namespace</span></span><br/>                | <span data-ttu-id="3247d-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3247d-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3247d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3247d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3247d-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3247d-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3247d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3247d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3247d-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3247d-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3247d-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3247d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3247d-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="3247d-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


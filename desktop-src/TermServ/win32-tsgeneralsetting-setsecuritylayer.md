---
title: Metodo SetSecurityLayer della classe Win32_TSGeneralSetting
description: Il metodo SetSecurityLayer imposta il livello di sicurezza.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSecurityLayer
- Metodo SetSecurityLayer Servizi Desktop remoto, classe Win32_TSGeneralSetting
- Classe Win32_TSGeneralSetting Servizi Desktop remoto, metodo SetSecurityLayer
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e04c3f7e5a58ec8de345d570e36b35c7eb1e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964319"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="a1109-106">Metodo SetSecurityLayer della \_ classe TSGeneralSetting Win32</span><span class="sxs-lookup"><span data-stu-id="a1109-106">SetSecurityLayer method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="a1109-107">Il metodo **SetSecurityLayer** imposta il livello di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a1109-107">The **SetSecurityLayer** method sets the security layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1109-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1109-108">Syntax</span></span>


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a><span data-ttu-id="a1109-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1109-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1109-110">*SecurityLayer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1109-110">*SecurityLayer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1109-111">Livello di sicurezza da impostare.</span><span class="sxs-lookup"><span data-stu-id="a1109-111">The security layer to set.</span></span> <span data-ttu-id="a1109-112">Se il livello di crittografia corrente è 1, il valore 2 per *SecurityLayer* non è valido.</span><span class="sxs-lookup"><span data-stu-id="a1109-112">If the current Encryption Level is 1, then a value of 2 for *SecurityLayer* is not valid.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="a1109-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Livello di protezione RDP** (0)</span><span class="sxs-lookup"><span data-stu-id="a1109-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a1109-114">La comunicazione tra il server e il client utilizzerà la crittografia RDP nativa.</span><span class="sxs-lookup"><span data-stu-id="a1109-114">Communication between the server and the client will use native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="a1109-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (1)</span><span class="sxs-lookup"><span data-stu-id="a1109-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a1109-116">Verrà utilizzato il livello più sicuro supportato dal client.</span><span class="sxs-lookup"><span data-stu-id="a1109-116">The most secure layer that is supported by the client will be used.</span></span> <span data-ttu-id="a1109-117">Se supportato, viene usato SSL (TLS 1,0).</span><span class="sxs-lookup"><span data-stu-id="a1109-117">If supported, SSL (TLS 1.0) will be used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="a1109-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2)</span><span class="sxs-lookup"><span data-stu-id="a1109-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a1109-119">SSL (TLS 1,0) verrà usato per l'autenticazione del server, nonché per la crittografia di tutti i dati trasferiti tra il server e il client.</span><span class="sxs-lookup"><span data-stu-id="a1109-119">SSL (TLS 1.0) will be used for server authentication as well as for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="a1109-120">Per questa impostazione è necessario che il server disponga di un certificato compatibile con SSL.</span><span class="sxs-lookup"><span data-stu-id="a1109-120">This setting requires the server to have an SSL compatible certificate.</span></span> <span data-ttu-id="a1109-121">Questa impostazione non è compatibile con un valore **MinEncryptionLevel** pari a 1.</span><span class="sxs-lookup"><span data-stu-id="a1109-121">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1109-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1109-122">Return value</span></span>

<span data-ttu-id="a1109-123">Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="a1109-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a1109-124">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a1109-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1109-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1109-125">Remarks</span></span>

<span data-ttu-id="a1109-126">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a1109-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a1109-127">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="a1109-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a1109-128">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="a1109-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a1109-129">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a1109-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1109-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1109-130">Requirements</span></span>



| <span data-ttu-id="a1109-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1109-131">Requirement</span></span> | <span data-ttu-id="a1109-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a1109-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1109-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1109-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a1109-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1109-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a1109-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1109-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a1109-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1109-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a1109-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a1109-137">Namespace</span></span><br/>                | <span data-ttu-id="a1109-138">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a1109-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a1109-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a1109-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1109-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1109-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1109-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a1109-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1109-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1109-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1109-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1109-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1109-144">**\_TSGeneralSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a1109-144">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> <dt>

[<span data-ttu-id="a1109-145">**SetEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="a1109-145">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 


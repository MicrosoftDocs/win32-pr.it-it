---
title: Metodo SetEncryptionLevel della classe Win32_TSGeneralSetting
description: Il metodo SetEncryptionLevel imposta il livello di crittografia.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetEncryptionLevel
- Metodo SetEncryptionLevel Servizi Desktop remoto, classe Win32_TSGeneralSetting
- Classe Win32_TSGeneralSetting Servizi Desktop remoto, metodo SetEncryptionLevel
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetEncryptionLevel
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1fbe727c75851bb13252d196e1fe7d599f881c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120382"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="9eea0-106">Metodo SetEncryptionLevel della \_ classe TSGeneralSetting Win32</span><span class="sxs-lookup"><span data-stu-id="9eea0-106">SetEncryptionLevel method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="9eea0-107">Il metodo **SetEncryptionLevel** imposta il livello di crittografia.</span><span class="sxs-lookup"><span data-stu-id="9eea0-107">The **SetEncryptionLevel** method sets the encryption level.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eea0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9eea0-108">Syntax</span></span>


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a><span data-ttu-id="9eea0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9eea0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eea0-110">*MinEncryptionLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9eea0-110">*MinEncryptionLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eea0-111">Livello di crittografia minimo da impostare.</span><span class="sxs-lookup"><span data-stu-id="9eea0-111">The minimum encryption level to set.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="9eea0-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="9eea0-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="9eea0-113">Basso livello di crittografia.</span><span class="sxs-lookup"><span data-stu-id="9eea0-113">Low level of encryption.</span></span> <span data-ttu-id="9eea0-114">Solo i dati inviati dal client al server vengono crittografati con la crittografia a 56 bit.</span><span class="sxs-lookup"><span data-stu-id="9eea0-114">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="9eea0-115">Si noti che i dati inviati dal server al client non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="9eea0-115">Note that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="9eea0-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="9eea0-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="9eea0-117">Livello di crittografia compatibile con il client.</span><span class="sxs-lookup"><span data-stu-id="9eea0-117">Client-compatible level of encryption.</span></span> <span data-ttu-id="9eea0-118">Tutti i dati inviati da client a server e da server a client vengono crittografati al livello di attendibilità massima supportato dal client.</span><span class="sxs-lookup"><span data-stu-id="9eea0-118">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="9eea0-119"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="9eea0-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="9eea0-120">Livello elevato di crittografia.</span><span class="sxs-lookup"><span data-stu-id="9eea0-120">High level of encryption.</span></span> <span data-ttu-id="9eea0-121">Tutti i dati inviati da client a server e da server a client vengono crittografati con la crittografia a 128 bit avanzata.</span><span class="sxs-lookup"><span data-stu-id="9eea0-121">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="9eea0-122">I client che non supportano questo livello di crittografia non possono connettersi.</span><span class="sxs-lookup"><span data-stu-id="9eea0-122">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="9eea0-123"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="9eea0-123"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="9eea0-124">Crittografia conforme a FIPS.</span><span class="sxs-lookup"><span data-stu-id="9eea0-124">FIPS-compliant encryption.</span></span> <span data-ttu-id="9eea0-125">Tutti i dati inviati da client a server e da server a client vengono crittografati e decrittografati con gli algoritmi di crittografia Federal Information Processing Standard (FIPS) usando i moduli di crittografia Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9eea0-125">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="9eea0-126">FIPS è uno standard denominato "requisiti di sicurezza per i moduli di crittografia".</span><span class="sxs-lookup"><span data-stu-id="9eea0-126">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="9eea0-127">FIPS 140-1 (1994) e FIPS 140-2 (2001) descrivono i requisiti governativi per i moduli di crittografia hardware e software utilizzati all'interno del governo degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="9eea0-127">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eea0-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9eea0-128">Return value</span></span>

<span data-ttu-id="9eea0-129">Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="9eea0-129">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9eea0-130">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="9eea0-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eea0-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="9eea0-131">Remarks</span></span>

<span data-ttu-id="9eea0-132">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9eea0-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9eea0-133">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="9eea0-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9eea0-134">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="9eea0-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9eea0-135">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9eea0-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9eea0-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9eea0-136">Requirements</span></span>



| <span data-ttu-id="9eea0-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eea0-137">Requirement</span></span> | <span data-ttu-id="9eea0-138">Valore</span><span class="sxs-lookup"><span data-stu-id="9eea0-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9eea0-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eea0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9eea0-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9eea0-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9eea0-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eea0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9eea0-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9eea0-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9eea0-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9eea0-143">Namespace</span></span><br/>                | <span data-ttu-id="9eea0-144">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9eea0-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9eea0-145">MOF</span><span class="sxs-lookup"><span data-stu-id="9eea0-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9eea0-146"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9eea0-146"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9eea0-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9eea0-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eea0-148"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eea0-148"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eea0-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9eea0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eea0-150">**\_TSGeneralSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="9eea0-150">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 


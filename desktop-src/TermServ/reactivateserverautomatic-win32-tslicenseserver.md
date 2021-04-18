---
title: Metodo ReactivateServerAutomatic della classe Win32_TSLicenseServer
description: Riattiva il server licenze Desktop remoto usando una connessione automatica a Internet.
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ReactivateServerAutomatic
- Metodo ReactivateServerAutomatic Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo ReactivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b9df7314abc3dccf6458322911c50d6120ad10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302450"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="1e32b-106">Metodo ReactivateServerAutomatic della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="1e32b-106">ReactivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="1e32b-107">Riattiva il server licenze Desktop remoto usando una connessione automatica a Internet.</span><span class="sxs-lookup"><span data-stu-id="1e32b-107">Reactivates the Remote Desktop license server by using an automatic connection to the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e32b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e32b-108">Syntax</span></span>


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="1e32b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e32b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e32b-110">*Motivo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e32b-110">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e32b-111">Motivo dell'attivazione.</span><span class="sxs-lookup"><span data-stu-id="1e32b-111">Reason for the activation.</span></span> <span data-ttu-id="1e32b-112">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1e32b-112">It can be one of the following values.</span></span>

<dt>

<span data-ttu-id="1e32b-113">0</span><span class="sxs-lookup"><span data-stu-id="1e32b-113">0</span></span>
</dt> <dd>

<span data-ttu-id="1e32b-114">Il server è stato ridistribuito.</span><span class="sxs-lookup"><span data-stu-id="1e32b-114">The server was redeployed.</span></span>

</dd> <dt>

<span data-ttu-id="1e32b-115">1</span><span class="sxs-lookup"><span data-stu-id="1e32b-115">1</span></span>
</dt> <dd>

<span data-ttu-id="1e32b-116">Il certificato è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="1e32b-116">The certificate was corrupt.</span></span>

</dd> <dt>

<span data-ttu-id="1e32b-117">2</span><span class="sxs-lookup"><span data-stu-id="1e32b-117">2</span></span>
</dt> <dd>

<span data-ttu-id="1e32b-118">La chiave privata è stata compromessa.</span><span class="sxs-lookup"><span data-stu-id="1e32b-118">The private key was compromised.</span></span>

</dd> <dt>

<span data-ttu-id="1e32b-119">3</span><span class="sxs-lookup"><span data-stu-id="1e32b-119">3</span></span>
</dt> <dd>

<span data-ttu-id="1e32b-120">Il codice di attivazione è scaduto.</span><span class="sxs-lookup"><span data-stu-id="1e32b-120">The activation key expired.</span></span>

</dd> <dt>

<span data-ttu-id="1e32b-121">4</span><span class="sxs-lookup"><span data-stu-id="1e32b-121">4</span></span>
</dt> <dd>

<span data-ttu-id="1e32b-122">Il server è stato aggiornato.</span><span class="sxs-lookup"><span data-stu-id="1e32b-122">The server was upgraded.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1e32b-123">*ActivationStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1e32b-123">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e32b-124">Lo stato di attivazione restituito può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1e32b-124">The activation status returned can be one of the following values.</span></span>

<dt>

<span data-ttu-id="1e32b-125">0</span><span class="sxs-lookup"><span data-stu-id="1e32b-125">0</span></span>
</dt> <dd>

<span data-ttu-id="1e32b-126">Il server licenze Desktop remoto viene attivato.</span><span class="sxs-lookup"><span data-stu-id="1e32b-126">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="1e32b-127">1</span><span class="sxs-lookup"><span data-stu-id="1e32b-127">1</span></span>
</dt> <dd>

<span data-ttu-id="1e32b-128">Il server licenze Desktop remoto non è attivato.</span><span class="sxs-lookup"><span data-stu-id="1e32b-128">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="1e32b-129">2</span><span class="sxs-lookup"><span data-stu-id="1e32b-129">2</span></span>
</dt> <dd>

<span data-ttu-id="1e32b-130">Si è verificato un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="1e32b-130">An unknown error occurred.</span></span> <span data-ttu-id="1e32b-131">Non è noto se il server licenze Desktop remoto è attivato.</span><span class="sxs-lookup"><span data-stu-id="1e32b-131">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e32b-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e32b-132">Return value</span></span>

<span data-ttu-id="1e32b-133">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="1e32b-133">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1e32b-134">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="1e32b-134">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1e32b-135">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1e32b-135">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1e32b-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e32b-136">Remarks</span></span>

<span data-ttu-id="1e32b-137">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="1e32b-137">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1e32b-138">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1e32b-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1e32b-139">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="1e32b-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1e32b-140">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="1e32b-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1e32b-141">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1e32b-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e32b-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e32b-142">Requirements</span></span>



| <span data-ttu-id="1e32b-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e32b-143">Requirement</span></span> | <span data-ttu-id="1e32b-144">Valore</span><span class="sxs-lookup"><span data-stu-id="1e32b-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e32b-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e32b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1e32b-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1e32b-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="1e32b-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e32b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1e32b-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e32b-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="1e32b-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1e32b-149">Namespace</span></span><br/>                | <span data-ttu-id="1e32b-150">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1e32b-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="1e32b-151">MOF</span><span class="sxs-lookup"><span data-stu-id="1e32b-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e32b-152"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e32b-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e32b-153">DLL</span><span class="sxs-lookup"><span data-stu-id="1e32b-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e32b-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e32b-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e32b-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e32b-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e32b-156">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="1e32b-156">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


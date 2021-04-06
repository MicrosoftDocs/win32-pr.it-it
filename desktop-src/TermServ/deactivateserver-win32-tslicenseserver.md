---
title: Metodo DeactivateServer della classe Win32_TSLicenseServer
description: Disattiva il server licenze Desktop remoto utilizzando un codice di conferma ricevuto tramite telefono.
ms.assetid: 84e069b7-9a4f-4843-b656-839f936ac727
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DeactivateServer
- Metodo DeactivateServer Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo DeactivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b851a8d8049c9194bce163afc4b7bad5d4aa15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963851"
---
# <a name="deactivateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="1a88e-106">Metodo DeactivateServer della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="1a88e-106">DeactivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="1a88e-107">Disattiva il server licenze Desktop remoto utilizzando un codice di conferma ricevuto tramite telefono.</span><span class="sxs-lookup"><span data-stu-id="1a88e-107">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a88e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a88e-108">Syntax</span></span>


```mof
uint32 DeactivateServer(
  [in]  string sConfirmCode,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="1a88e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a88e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a88e-110">*sConfirmCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a88e-110">*sConfirmCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a88e-111">Codice di conferma.</span><span class="sxs-lookup"><span data-stu-id="1a88e-111">Confirmation code.</span></span>

</dd> <dt>

<span data-ttu-id="1a88e-112">*ActivationStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1a88e-112">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a88e-113">Lo stato di attivazione restituito può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="1a88e-113">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="1a88e-114">0</span><span class="sxs-lookup"><span data-stu-id="1a88e-114">0</span></span>
</dt> <dd>

<span data-ttu-id="1a88e-115">Il server licenze Desktop remoto viene attivato.</span><span class="sxs-lookup"><span data-stu-id="1a88e-115">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="1a88e-116">1</span><span class="sxs-lookup"><span data-stu-id="1a88e-116">1</span></span>
</dt> <dd>

<span data-ttu-id="1a88e-117">Il server licenze Desktop remoto non è attivato.</span><span class="sxs-lookup"><span data-stu-id="1a88e-117">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="1a88e-118">2</span><span class="sxs-lookup"><span data-stu-id="1a88e-118">2</span></span>
</dt> <dd>

<span data-ttu-id="1a88e-119">Si è verificato un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="1a88e-119">An unknown error occurred.</span></span> <span data-ttu-id="1a88e-120">Non è noto se il server licenze Servizi Desktop remoto è attivato.</span><span class="sxs-lookup"><span data-stu-id="1a88e-120">It is not known whether the Remote Desktop Services license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a88e-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a88e-121">Return value</span></span>

<span data-ttu-id="1a88e-122">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="1a88e-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1a88e-123">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="1a88e-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1a88e-124">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1a88e-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1a88e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a88e-125">Remarks</span></span>

<span data-ttu-id="1a88e-126">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="1a88e-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1a88e-127">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1a88e-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1a88e-128">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="1a88e-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1a88e-129">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="1a88e-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1a88e-130">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1a88e-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a88e-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a88e-131">Requirements</span></span>



| <span data-ttu-id="1a88e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a88e-132">Requirement</span></span> | <span data-ttu-id="1a88e-133">Valore</span><span class="sxs-lookup"><span data-stu-id="1a88e-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a88e-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a88e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1a88e-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1a88e-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="1a88e-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a88e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1a88e-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a88e-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="1a88e-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1a88e-138">Namespace</span></span><br/>                | <span data-ttu-id="1a88e-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1a88e-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="1a88e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1a88e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a88e-141"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a88e-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a88e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1a88e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a88e-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a88e-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a88e-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a88e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a88e-145">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="1a88e-145">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


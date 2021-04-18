---
description: Recupera l'identificatore di sicurezza e i flag utilizzati per proteggere una chiave.
ms.assetid: 5EF97F44-78FF-4FBF-9142-F2DD0A849057
title: Metodo GetKeyProtectorAdSidInformation della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 57e72488a9e53f49383d179b0bcb1a8b9ff1f706
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334004"
---
# <a name="getkeyprotectoradsidinformation-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="bb72c-103">Metodo GetKeyProtectorAdSidInformation della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="bb72c-103">GetKeyProtectorAdSidInformation method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="bb72c-104">Il metodo **GetKeyProtectorAdSidInformation** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) recupera l'identificatore di sicurezza e i flag utilizzati per proteggere una chiave.</span><span class="sxs-lookup"><span data-stu-id="bb72c-104">The **GetKeyProtectorAdSidInformation** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the security identifier and flags used to protect a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb72c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb72c-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] string SidString,
  [out] uint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="bb72c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb72c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb72c-107">*VolumeKeyProtectorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb72c-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb72c-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="bb72c-108">Type: **string**</span></span>

<span data-ttu-id="bb72c-109">Identificatore di stringa che può essere usato per gestire una protezione con chiave del volume crittografata.</span><span class="sxs-lookup"><span data-stu-id="bb72c-109">A string identifier that can be used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="bb72c-110">*SidString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bb72c-110">*SidString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb72c-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="bb72c-111">Type: **string**</span></span>

<span data-ttu-id="bb72c-112">Stringa che contiene l'ID di sicurezza (SID).</span><span class="sxs-lookup"><span data-stu-id="bb72c-112">A string that contains the security identifier (SID).</span></span>

</dd> <dt>

<span data-ttu-id="bb72c-113">*Flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bb72c-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb72c-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb72c-114">Type: **uint32**</span></span>

<span data-ttu-id="bb72c-115">Flag che modificano il comportamento della funzione.</span><span class="sxs-lookup"><span data-stu-id="bb72c-115">Flags that change the function behavior.</span></span> <span data-ttu-id="bb72c-116">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bb72c-116">This can be one of the following values.</span></span>



| <span data-ttu-id="bb72c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bb72c-117">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="bb72c-118">Significato</span><span class="sxs-lookup"><span data-stu-id="bb72c-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="bb72c-119"><dt>**FVE \_ \_Flag ng \_ DPAPI \_ None**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="bb72c-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="bb72c-120">Nessun effetto.</span><span class="sxs-lookup"><span data-stu-id="bb72c-120">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="bb72c-121"><dt>**FVE \_ Lo \_ sblocco del flag ng DPAPI \_ \_ \_ come \_ \_ account del servizio**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="bb72c-121"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="bb72c-122">Specifica che la protezione basata su SID è stata protetta per un account del servizio.</span><span class="sxs-lookup"><span data-stu-id="bb72c-122">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="bb72c-123">Se questo flag è specificato, il chiamante deve verificare che sia in esecuzione come account del servizio appropriato prima di chiamare [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (eliminando temporaneamente la rappresentazione, ad esempio).</span><span class="sxs-lookup"><span data-stu-id="bb72c-123">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb72c-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb72c-124">Return value</span></span>

<span data-ttu-id="bb72c-125">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb72c-125">Type: **uint32**</span></span>

<span data-ttu-id="bb72c-126">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="bb72c-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="bb72c-127">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb72c-127">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="bb72c-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb72c-128">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="bb72c-129"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bb72c-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="bb72c-130">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="bb72c-130">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bb72c-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb72c-131">Remarks</span></span>

<span data-ttu-id="bb72c-132">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bb72c-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bb72c-133">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="bb72c-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="bb72c-134">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="bb72c-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bb72c-135">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="bb72c-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb72c-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb72c-136">Requirements</span></span>



| <span data-ttu-id="bb72c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb72c-137">Requirement</span></span> | <span data-ttu-id="bb72c-138">Valore</span><span class="sxs-lookup"><span data-stu-id="bb72c-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb72c-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb72c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="bb72c-140">Windows 8 Enterprise, \[ solo app desktop Windows 8 Pro\]</span><span class="sxs-lookup"><span data-stu-id="bb72c-140">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bb72c-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb72c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="bb72c-142">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bb72c-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb72c-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bb72c-143">Namespace</span></span><br/>                | <span data-ttu-id="bb72c-144">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="bb72c-144">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="bb72c-145">MOF</span><span class="sxs-lookup"><span data-stu-id="bb72c-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb72c-146"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb72c-146"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb72c-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb72c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb72c-148">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="bb72c-148">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

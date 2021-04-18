---
description: Protegge la chiave di crittografia del volume utilizzando un ID di sicurezza Active Directory (SID).
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Metodo ProtectKeyWithAdSid della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0279a6edc8aaa275fdf75a855452d987de802d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315339"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ceaea-103">Metodo ProtectKeyWithAdSid della \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="ceaea-103">ProtectKeyWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ceaea-104">Il metodo **ProtectKeyWithAdSid** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) protegge la chiave di crittografia del volume utilizzando un ID di sicurezza Active Directory (SID).</span><span class="sxs-lookup"><span data-stu-id="ceaea-104">The **ProtectKeyWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using a Active Directory security identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="ceaea-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ceaea-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithAdSid(
  [in, optional] string FriendlyName,
  [in]           string SidString,
  [in]           uint32 Flags,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="ceaea-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ceaea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceaea-107">*FriendlyName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ceaea-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ceaea-108">Stringa che specifica un identificatore assegnato dall'utente per la protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="ceaea-108">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="ceaea-109">Se questo parametro non è specificato, viene utilizzato un valore blank.</span><span class="sxs-lookup"><span data-stu-id="ceaea-109">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="ceaea-110">*SidString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ceaea-110">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceaea-111">Stringa che contiene il SID Active Directory usato per proteggere la chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="ceaea-111">String that contains the Active Directory SID used to protect the encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="ceaea-112">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ceaea-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceaea-113">Flag che modificano il comportamento della funzione.</span><span class="sxs-lookup"><span data-stu-id="ceaea-113">Flags that change the function behavior.</span></span> <span data-ttu-id="ceaea-114">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ceaea-114">This can be one of the following values.</span></span>



| <span data-ttu-id="ceaea-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ceaea-115">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="ceaea-116">Significato</span><span class="sxs-lookup"><span data-stu-id="ceaea-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="ceaea-117"><dt>**FVE \_ \_Flag ng \_ DPAPI \_ None**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="ceaea-117"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="ceaea-118">Nessun effetto.</span><span class="sxs-lookup"><span data-stu-id="ceaea-118">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="ceaea-119"><dt>**FVE \_ Lo \_ sblocco del flag ng DPAPI \_ \_ \_ come \_ \_ account del servizio**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="ceaea-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="ceaea-120">Specifica che la protezione basata su SID è stata protetta per un account del servizio.</span><span class="sxs-lookup"><span data-stu-id="ceaea-120">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="ceaea-121">Se questo flag è specificato, il chiamante deve verificare che sia in esecuzione come account del servizio appropriato prima di chiamare [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (eliminando temporaneamente la rappresentazione, ad esempio).</span><span class="sxs-lookup"><span data-stu-id="ceaea-121">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ceaea-122">*VolumeKeyProtectorID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ceaea-122">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ceaea-123">Identificatore univoco associato alla protezione creata.</span><span class="sxs-lookup"><span data-stu-id="ceaea-123">A unique identifier associated with the created protector.</span></span> <span data-ttu-id="ceaea-124">È possibile usare questa stringa per gestire la protezione con chiave.</span><span class="sxs-lookup"><span data-stu-id="ceaea-124">You can use this string to manage the key protector.</span></span>

<span data-ttu-id="ceaea-125">Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID è impostata su "BitLocker" e la protezione con chiave viene scritta in base ai metadati della banda.</span><span class="sxs-lookup"><span data-stu-id="ceaea-125">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceaea-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ceaea-126">Return value</span></span>

<span data-ttu-id="ceaea-127">Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ceaea-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ceaea-128">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="ceaea-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="ceaea-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ceaea-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ceaea-130"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ceaea-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ceaea-131">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="ceaea-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ceaea-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="ceaea-132">Remarks</span></span>

<span data-ttu-id="ceaea-133">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ceaea-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ceaea-134">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ceaea-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ceaea-135">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="ceaea-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ceaea-136">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md)</span><span class="sxs-lookup"><span data-stu-id="ceaea-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md)</span></span>

<span data-ttu-id="ceaea-137">Per impostazione predefinita, non è possibile aggiungere un account Active Directory o un gruppo di protezione in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="ceaea-137">By default, you cannot add an Active Directory account or group protector remotely.</span></span> <span data-ttu-id="ceaea-138">È necessario abilitare la delega vincolata sul controller di dominio e sul computer di origine.</span><span class="sxs-lookup"><span data-stu-id="ceaea-138">You must enable constrained delegation on the domain controller and source computer.</span></span> <span data-ttu-id="ceaea-139">Nel controller di dominio seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="ceaea-139">On the domain controller, perform the following steps:</span></span>

1.  <span data-ttu-id="ceaea-140">Avviare Server Manager</span><span class="sxs-lookup"><span data-stu-id="ceaea-140">Open Server Manager</span></span>
2.  <span data-ttu-id="ceaea-141">Selezione dei computer nei ruoli Active Directory</span><span class="sxs-lookup"><span data-stu-id="ceaea-141">Select Computers in Active Directory roles</span></span>
3.  <span data-ttu-id="ceaea-142">Selezionare il computer client di destinazione e fare clic con il pulsante destro</span><span class="sxs-lookup"><span data-stu-id="ceaea-142">Select the target client computer and right click</span></span>
4.  <span data-ttu-id="ceaea-143">Selezionare la scheda delega</span><span class="sxs-lookup"><span data-stu-id="ceaea-143">Select the Delegation tab</span></span>
5.  <span data-ttu-id="ceaea-144">Selezionare il pulsante di opzione "considera attendibile il computer per la delega solo ai servizi specificati"</span><span class="sxs-lookup"><span data-stu-id="ceaea-144">Select the "Trust this computer for delegation to specified services only" radio button</span></span>
6.  <span data-ttu-id="ceaea-145">Selezionare il pulsante di opzione "USA solo Kerberos"</span><span class="sxs-lookup"><span data-stu-id="ceaea-145">Select the "Use Kerberos only" radio button</span></span>
7.  <span data-ttu-id="ceaea-146">Fare clic su Aggiungi.</span><span class="sxs-lookup"><span data-stu-id="ceaea-146">Click Add</span></span>
8.  <span data-ttu-id="ceaea-147">Selezionare "utenti o computer"</span><span class="sxs-lookup"><span data-stu-id="ceaea-147">Select "Users or Computers"</span></span>
9.  <span data-ttu-id="ceaea-148">Selezionare host/come nome dell'entità servizio</span><span class="sxs-lookup"><span data-stu-id="ceaea-148">Select host/ as the Service Principal Name</span></span>

<span data-ttu-id="ceaea-149">Eseguire i passaggi da 3 a 9 nel computer di origine.</span><span class="sxs-lookup"><span data-stu-id="ceaea-149">Perform steps 3 through 9 on the source computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceaea-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ceaea-150">Requirements</span></span>



| <span data-ttu-id="ceaea-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceaea-151">Requirement</span></span> | <span data-ttu-id="ceaea-152">Valore</span><span class="sxs-lookup"><span data-stu-id="ceaea-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceaea-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ceaea-153">Minimum supported client</span></span><br/> | <span data-ttu-id="ceaea-154">Windows 8 Enterprise, \[ solo app desktop Windows 8 Pro\]</span><span class="sxs-lookup"><span data-stu-id="ceaea-154">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ceaea-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ceaea-155">Minimum supported server</span></span><br/> | <span data-ttu-id="ceaea-156">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ceaea-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ceaea-157">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ceaea-157">Namespace</span></span><br/>                | <span data-ttu-id="ceaea-158">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="ceaea-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ceaea-159">MOF</span><span class="sxs-lookup"><span data-stu-id="ceaea-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ceaea-160"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ceaea-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceaea-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ceaea-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceaea-162">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="ceaea-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

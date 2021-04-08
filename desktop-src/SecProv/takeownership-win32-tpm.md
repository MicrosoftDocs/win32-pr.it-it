---
description: Installa un proprietario per il TPM.
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: Metodo TakeOwnership della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.TakeOwnership
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: acb0cb03f5e422695623bf6e183d1fd89f63ab60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058180"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a><span data-ttu-id="98f45-103">Metodo TakeOwnership della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="98f45-103">TakeOwnership method of the Win32\_Tpm class</span></span>

<span data-ttu-id="98f45-104">Il metodo **TakeOwnership** della classe [**\_ TPM Win32**](win32-tpm.md) installa un proprietario per il TPM.</span><span class="sxs-lookup"><span data-stu-id="98f45-104">The **TakeOwnership** method of the [**Win32\_Tpm**](win32-tpm.md) class installs an owner for the TPM.</span></span> <span data-ttu-id="98f45-105">Il proprietario del TPM può avvalersi completamente delle funzionalità TPM.</span><span class="sxs-lookup"><span data-stu-id="98f45-105">The owner of the TPM can make full use of TPM capabilities.</span></span> <span data-ttu-id="98f45-106">Dopo aver impostato un proprietario, nessun altro utente o software può richiedere la proprietà del TPM.</span><span class="sxs-lookup"><span data-stu-id="98f45-106">After an owner is set, no other user or software can claim ownership of the TPM.</span></span>

<span data-ttu-id="98f45-107">I metodi [**IsEnabled**](isenabled-win32-tpm.md), IsEnabled [**e**](isactivated-win32-tpm.md) [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) devono essere tutti true prima che il metodo **TakeOwnership** possa avere esito positivo.</span><span class="sxs-lookup"><span data-stu-id="98f45-107">The [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) methods must all be true before the **TakeOwnership** method can succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="98f45-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98f45-108">Syntax</span></span>


```mof
uint32 TakeOwnership(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="98f45-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="98f45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98f45-110">*OwnerAuth* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="98f45-110">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="98f45-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="98f45-111">Type: **string**</span></span>

<span data-ttu-id="98f45-112">Stringa che identifica il proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="98f45-112">A string that identifies the TPM owner.</span></span> <span data-ttu-id="98f45-113">Questa stringa deve essere una stringa con codifica Base64 con terminazione null che contiene esattamente 20 byte di dati binari.</span><span class="sxs-lookup"><span data-stu-id="98f45-113">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="98f45-114">Usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per tradurre una passphrase nel formato previsto.</span><span class="sxs-lookup"><span data-stu-id="98f45-114">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="98f45-115">Il parametro *OwnerAuth* viene letto dal registro di sistema se non ne viene specificato alcuno.</span><span class="sxs-lookup"><span data-stu-id="98f45-115">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98f45-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98f45-116">Return value</span></span>

<span data-ttu-id="98f45-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98f45-117">Type: **uint32**</span></span>

<span data-ttu-id="98f45-118">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="98f45-118">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="98f45-119">Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="98f45-119">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="98f45-120">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="98f45-120">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="98f45-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98f45-121">Description</span></span>                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="98f45-122"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="98f45-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="98f45-123">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="98f45-123">The method was successful.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="98f45-124"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="98f45-124"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="98f45-125">Il parametro *OwnerAuth* non è valido.</span><span class="sxs-lookup"><span data-stu-id="98f45-125">The *OwnerAuth* parameter is not valid.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="98f45-126"><dt>**TPM \_ E \_ owner \_ set**</dt> <dt>2150105108 (0x80280014)</dt></span><span class="sxs-lookup"><span data-stu-id="98f45-126"><dt>**TPM\_E\_OWNER\_SET**</dt> <dt>2150105108 (0x80280014)</dt></span></span> </dl>            | <span data-ttu-id="98f45-127">Un proprietario esiste già nel TPM.</span><span class="sxs-lookup"><span data-stu-id="98f45-127">An owner already exists on the TPM.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="98f45-128"><dt>**TPM \_ E \_ Nessuna \_**</dt> verifica dell'autenticità <dt>2150105123 (0x80280023)</dt></span><span class="sxs-lookup"><span data-stu-id="98f45-128"><dt>**TPM\_E\_NO\_ENDORSEMENT**</dt> <dt>2150105123 (0x80280023)</dt></span></span> </dl>       | <span data-ttu-id="98f45-129">Non è possibile trovare la chiave di verifica dell'autenticità nel TPM.</span><span class="sxs-lookup"><span data-stu-id="98f45-129">No endorsement key can be found on the TPM.</span></span><br/> <span data-ttu-id="98f45-130">Per creare una coppia di chiavi di verifica dell'autenticità nel TPM, vedere il metodo [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="98f45-130">To create an endorsement key pair on the TPM, see the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="98f45-131"><dt>**TPM \_ E \_ installazione \_ disabilitata**</dt> <dt>2150105099 (0x8028000B)</dt></span><span class="sxs-lookup"><span data-stu-id="98f45-131"><dt>**TPM\_E\_INSTALL\_DISABLED**</dt> <dt>2150105099 (0x8028000B)</dt></span></span> </dl>     | <span data-ttu-id="98f45-132">Non è possibile installare un proprietario in questo TPM.</span><span class="sxs-lookup"><span data-stu-id="98f45-132">An owner cannot be installed on this TPM.</span></span><br/> <span data-ttu-id="98f45-133">Per informazioni su come consentire l'installazione del proprietario di un dispositivo, vedere [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).</span><span class="sxs-lookup"><span data-stu-id="98f45-133">For information about how to allow installation of a device owner, see [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).</span></span><br/> |
| <dl> <span data-ttu-id="98f45-134"><dt>**TPM \_ E \_ difendono il \_ blocco \_ che esegue**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="98f45-134"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="98f45-135">Il TPM è in difesa dagli attacchi del dizionario e si trova in un periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="98f45-135">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="98f45-136">Per ulteriori informazioni, vedere il metodo [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="98f45-136">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="98f45-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="98f45-137">Remarks</span></span>

<span data-ttu-id="98f45-138">I metodi [**IsEnabled, IsEnabled**](isenabled-win32-tpm.md)e [](isactivated-win32-tpm.md) [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) devono essere tutti true prima che **TakeOwnership** possa avere esito positivo.</span><span class="sxs-lookup"><span data-stu-id="98f45-138">The methods [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) must all be true before **TakeOwnership** can succeed.</span></span>

<span data-ttu-id="98f45-139">È necessario usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per modificare una passphrase nel valore di input usato per il parametro *OwnerAuth* .</span><span class="sxs-lookup"><span data-stu-id="98f45-139">You should use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to change a passphrase into the input value used for the *OwnerAuth* parameter.</span></span>

<span data-ttu-id="98f45-140">Il metodo **TakeOwnership** esegue il backup del valore di autorizzazione del proprietario per Active Directory se sono state configurate le impostazioni criteri di gruppo appropriate.</span><span class="sxs-lookup"><span data-stu-id="98f45-140">The **TakeOwnership** method backs up the owner authorization value to Active Directory if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="98f45-141">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="98f45-141">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="98f45-142">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="98f45-142">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="98f45-143">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="98f45-143">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="98f45-144">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="98f45-144">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98f45-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98f45-145">Requirements</span></span>



| <span data-ttu-id="98f45-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="98f45-146">Requirement</span></span> | <span data-ttu-id="98f45-147">Valore</span><span class="sxs-lookup"><span data-stu-id="98f45-147">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="98f45-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98f45-148">Minimum supported client</span></span><br/> | <span data-ttu-id="98f45-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98f45-149">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="98f45-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98f45-150">Minimum supported server</span></span><br/> | <span data-ttu-id="98f45-151">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98f45-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="98f45-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="98f45-152">Namespace</span></span><br/>                | <span data-ttu-id="98f45-153">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="98f45-153">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="98f45-154">MOF</span><span class="sxs-lookup"><span data-stu-id="98f45-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98f45-155"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98f45-155"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="98f45-156">DLL</span><span class="sxs-lookup"><span data-stu-id="98f45-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98f45-157"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="98f45-157"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98f45-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98f45-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f45-159">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="98f45-159">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

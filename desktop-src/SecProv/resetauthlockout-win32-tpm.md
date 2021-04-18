---
description: Reimposta il periodo di timeout o un altro meccanismo che i produttori di TPM implementano per proteggere da attacchi con dizionario sui valori di autorizzazione TPM.
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Metodo ResetAuthLockOut della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetAuthLockOut
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d28287e410fbaf65ce5b1e617113c35cfece160b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306377"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a><span data-ttu-id="985fb-103">Metodo ResetAuthLockOut della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="985fb-103">ResetAuthLockOut method of the Win32\_Tpm class</span></span>

<span data-ttu-id="985fb-104">Il metodo **ResetAuthLockOut** della classe [**\_ TPM Win32**](win32-tpm.md) Reimposta il periodo di timeout o un altro meccanismo che i produttori di TPM implementano per proteggere da attacchi con dizionario sui valori di autorizzazione TPM.</span><span class="sxs-lookup"><span data-stu-id="985fb-104">The **ResetAuthLockOut** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on TPM authorization values.</span></span> <span data-ttu-id="985fb-105">In un attacco con dizionario, un utente malintenzionato tenta di indovinare un valore di autorizzazione TPM corretto ritentando in modo esaustivo tutti i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="985fb-105">In a dictionary attack, an attacker tries to guess a correct TPM authorization value by exhaustively attempting all possible values.</span></span>

<span data-ttu-id="985fb-106">Utilizzare questo metodo se il TPM è bloccato a causa di un numero eccessivo di tentativi non corretti di immissione dell'autorizzazione del proprietario o di altri valori di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="985fb-106">Use this method if the TPM is locked out due to too many incorrect attempts at entering the owner authorization or other authorization values.</span></span> <span data-ttu-id="985fb-107">Quando il TPM è bloccato, alcuni o tutti i comandi emessi al TPM restituiscono un errore, TPM \_ E \_ difendono il \_ blocco \_ in esecuzione (0x80280803).</span><span class="sxs-lookup"><span data-stu-id="985fb-107">When the TPM is locked out, some or all commands issued to the TPM will return an error, TPM\_E\_DEFEND\_LOCK\_RUNNING (0x80280803).</span></span>

> [!Note]  
> <span data-ttu-id="985fb-108">Questo metodo può essere utilizzato solo una volta quando il TPM è bloccato. Se l'autorizzazione del proprietario fornita a questo metodo non è corretta, il TPM si bloccherà per l'intero periodo di timeout e i tentativi aggiuntivi di reimpostazione del blocco avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="985fb-108">This method can only be used exactly once when the TPM is locked out. If the owner authorization provided to this method is incorrect, the TPM will lock out for the entire time-out period and additional attempts at resetting the lock will fail.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="985fb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="985fb-109">Syntax</span></span>


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="985fb-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="985fb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="985fb-111">*OwnerAuth* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="985fb-111">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="985fb-112">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="985fb-112">Type: **string**</span></span>

<span data-ttu-id="985fb-113">Stringa che identifica il proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="985fb-113">A string that identifies the TPM owner.</span></span>

<span data-ttu-id="985fb-114">Questa stringa deve essere una stringa con codifica Base64 con terminazione null che contiene esattamente 20 byte di dati binari.</span><span class="sxs-lookup"><span data-stu-id="985fb-114">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="985fb-115">Usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per tradurre una passphrase nel formato previsto.</span><span class="sxs-lookup"><span data-stu-id="985fb-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="985fb-116">Il parametro *OwnerAuth* viene letto dal registro di sistema se non ne viene specificato alcuno.</span><span class="sxs-lookup"><span data-stu-id="985fb-116">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="985fb-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="985fb-117">Return value</span></span>

<span data-ttu-id="985fb-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="985fb-118">Type: **uint32**</span></span>

<span data-ttu-id="985fb-119">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="985fb-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span> <span data-ttu-id="985fb-120">Nella tabella seguente sono elencati alcuni dei valori restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="985fb-120">The following table lists some of the common return values.</span></span>



| <span data-ttu-id="985fb-121">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="985fb-121">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="985fb-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="985fb-122">Description</span></span>                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="985fb-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="985fb-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                            | <span data-ttu-id="985fb-124">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="985fb-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="985fb-125"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="985fb-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl> | <span data-ttu-id="985fb-126">Il valore di autorizzazione del proprietario specificato non è corretto.</span><span class="sxs-lookup"><span data-stu-id="985fb-126">The provided owner authorization value is incorrect.</span></span> <span data-ttu-id="985fb-127">Ulteriori tentativi di reimpostazione del blocco avranno esito negativo con lo stesso errore.</span><span class="sxs-lookup"><span data-stu-id="985fb-127">Additional attempts at resetting the lock will fail with this same error.</span></span> <span data-ttu-id="985fb-128">Attendere la scadenza del periodo di timeout o di un altro meccanismo specifico del produttore prima di ritentare i comandi bloccati del TPM.</span><span class="sxs-lookup"><span data-stu-id="985fb-128">Please wait until the time-out period or other manufacturer-specific mechanism has expired before retrying locked TPM commands.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="985fb-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="985fb-129">Remarks</span></span>

<span data-ttu-id="985fb-130">Questo metodo chiama il TPM \_ ResetLockValue comando sul TPM.</span><span class="sxs-lookup"><span data-stu-id="985fb-130">This method calls the TPM\_ResetLockValue command on the TPM.</span></span> <span data-ttu-id="985fb-131">Il comportamento esatto di questo metodo varia tra i produttori di TPM.</span><span class="sxs-lookup"><span data-stu-id="985fb-131">The exact behavior of this method varies among TPM manufacturers.</span></span> <span data-ttu-id="985fb-132">La documentazione del produttore del computer o del TPM può fornire informazioni aggiuntive sull'implementazione del meccanismo di attacco anti-Dictionary.</span><span class="sxs-lookup"><span data-stu-id="985fb-132">Documentation from the computer or TPM manufacturer may provide additional information on the implementation of the anti-dictionary attack mechanism.</span></span>

<span data-ttu-id="985fb-133">In generale, i costruttori possono rilevare gli attacchi con dizionario tenendo traccia delle autenticazioni non riuscite.</span><span class="sxs-lookup"><span data-stu-id="985fb-133">In general, manufacturers can detect dictionary attacks by keeping track of failed authentications.</span></span> <span data-ttu-id="985fb-134">Se il numero o la frequenza degli errori diventa sufficientemente elevata, il TPM bloccherà altri comandi per un certo periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="985fb-134">If the number or frequency of failures become high enough, the TPM will lock out further commands for a certain time.</span></span> <span data-ttu-id="985fb-135">In genere, il periodo di timeout iniziale sarà breve per consentire a un utente legittimo di correggere la situazione.</span><span class="sxs-lookup"><span data-stu-id="985fb-135">Generally, the initial time-out period will be short, to allow a legitimate user a chance to correct the situation.</span></span> <span data-ttu-id="985fb-136">Se gli errori continuano, la durata di ogni periodo di timeout successivo potrebbe aumentare rapidamente.</span><span class="sxs-lookup"><span data-stu-id="985fb-136">If failures continue, the duration of each subsequent time-out period may increase rapidly.</span></span>

<span data-ttu-id="985fb-137">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="985fb-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="985fb-138">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="985fb-138">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="985fb-139">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="985fb-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="985fb-140">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="985fb-140">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="985fb-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="985fb-141">Requirements</span></span>



| <span data-ttu-id="985fb-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="985fb-142">Requirement</span></span> | <span data-ttu-id="985fb-143">Valore</span><span class="sxs-lookup"><span data-stu-id="985fb-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="985fb-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="985fb-144">Minimum supported client</span></span><br/> | <span data-ttu-id="985fb-145">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="985fb-145">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="985fb-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="985fb-146">Minimum supported server</span></span><br/> | <span data-ttu-id="985fb-147">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="985fb-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="985fb-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="985fb-148">Namespace</span></span><br/>                | <span data-ttu-id="985fb-149">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="985fb-149">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="985fb-150">MOF</span><span class="sxs-lookup"><span data-stu-id="985fb-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="985fb-151"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="985fb-151"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="985fb-152">DLL</span><span class="sxs-lookup"><span data-stu-id="985fb-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="985fb-153"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="985fb-153"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="985fb-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="985fb-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="985fb-155">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="985fb-155">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

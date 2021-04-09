---
description: Modifica il valore di autorizzazione del proprietario del TPM.
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Metodo ChangeOwnerAuth della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ChangeOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: fc4b044d58dcaca5364f0ba669b09030cf3b34dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128759"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="6ae14-103">Metodo ChangeOwnerAuth della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="6ae14-103">ChangeOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="6ae14-104">Il metodo **ChangeOwnerAuth** della classe [**\_ TPM Win32**](win32-tpm.md) modifica il valore di autorizzazione del proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="6ae14-104">The **ChangeOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class changes the TPM owner authorization value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ae14-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ae14-105">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="6ae14-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ae14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ae14-107">*OldOwnerAuth* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6ae14-107">*OldOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6ae14-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="6ae14-108">Type: **string**</span></span>

<span data-ttu-id="6ae14-109">Stringa che assegna un nome al valore di autorizzazione corrente del proprietario del TPM del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ae14-109">A string that names the current TPM owner authorization value of the device.</span></span> <span data-ttu-id="6ae14-110">Usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per convertire una password in questo valore di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="6ae14-110">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="6ae14-111">Il parametro *OldOwnerAuth* non è specificato o viene specificata una stringa vuota, questo metodo ottiene il valore dal registro di sistema, se presente.</span><span class="sxs-lookup"><span data-stu-id="6ae14-111">The *OldOwnerAuth* parameter is not supplied or an empty string is provided, this method gets the value from the registry if present.</span></span>

</dd> <dt>

<span data-ttu-id="6ae14-112">*NewOwnerAuth* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6ae14-112">*NewOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6ae14-113">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="6ae14-113">Type: **string**</span></span>

<span data-ttu-id="6ae14-114">Stringa che assegna un nome al nuovo valore di autorizzazione del proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="6ae14-114">A string that names the new TPM owner authorization value.</span></span> <span data-ttu-id="6ae14-115">Usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per convertire una password in questo valore di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="6ae14-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="6ae14-116">Il parametro *NewOwnerAuth* non può essere vuoto o **null.**</span><span class="sxs-lookup"><span data-stu-id="6ae14-116">The *NewOwnerAuth* parameter cannot be empty or **NULL.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ae14-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ae14-117">Return value</span></span>

<span data-ttu-id="6ae14-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ae14-118">Type: **uint32**</span></span>

<span data-ttu-id="6ae14-119">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="6ae14-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="6ae14-120">Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="6ae14-120">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="6ae14-121">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ae14-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="6ae14-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ae14-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6ae14-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6ae14-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                              | <span data-ttu-id="6ae14-124">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="6ae14-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="6ae14-125"><dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="6ae14-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>                   | <span data-ttu-id="6ae14-126">Il valore di autorizzazione del proprietario del TPM corrente non è corretto.</span><span class="sxs-lookup"><span data-stu-id="6ae14-126">The current TPM owner authorization value is incorrect.</span></span><br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="6ae14-127"><dt>**TPM \_ E \_ difendono il \_ blocco \_ che esegue**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="6ae14-127"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl>      | <span data-ttu-id="6ae14-128">Il TPM è in difesa dagli attacchi del dizionario e si trova in un periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="6ae14-128">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="6ae14-129">Per ulteriori informazioni, vedere il metodo [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="6ae14-129">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="6ae14-130"><dt>**FVE \_ \_Schema di ad E \_ \_ non \_ installato**</dt> <dt>2150694922 (0x8031000A)</dt></span><span class="sxs-lookup"><span data-stu-id="6ae14-130"><dt>**FVE\_E\_AD\_SCHEMA\_NOT\_INSTALLED**</dt> <dt>2150694922 (0x8031000A)</dt></span></span> </dl> | <span data-ttu-id="6ae14-131">Non è possibile salvare le informazioni di ripristino nella rete.</span><span class="sxs-lookup"><span data-stu-id="6ae14-131">Cannot save recovery information to the network.</span></span> <span data-ttu-id="6ae14-132">Il computer è stato configurato per archiviare le informazioni di ripristino in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="6ae14-132">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="6ae14-133">Per istruzioni su come configurare Active Directory, vedere [Guida alla configurazione di crittografia unità BitLocker: backup delle informazioni di ripristino di BitLocker e TPM in Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="6ae14-133">For instructions on how to set up Active Directory, see [BitLocker Drive Encryption Configuration Guide: Backing Up BitLocker and TPM Recovery Information to Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).</span></span><br/> |
| <dl> <span data-ttu-id="6ae14-134"><dt>**Connessione non riuscita**</dt> <dt>2147943755 (0x8007054B)</dt></span><span class="sxs-lookup"><span data-stu-id="6ae14-134"><dt>**Connection Failed**</dt> <dt>2147943755 (0x8007054B)</dt></span></span> </dl>                  | <span data-ttu-id="6ae14-135">Non è possibile salvare le informazioni di ripristino nella rete.</span><span class="sxs-lookup"><span data-stu-id="6ae14-135">Cannot save recovery information to the network.</span></span> <span data-ttu-id="6ae14-136">Il computer è stato configurato per archiviare le informazioni di ripristino in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="6ae14-136">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="6ae14-137">Per continuare, è necessaria una connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="6ae14-137">A network connection is required to continue.</span></span><br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="6ae14-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ae14-138">Remarks</span></span>

<span data-ttu-id="6ae14-139">Il metodo **ChangeOwnerAuth** esegue il backup della nuova autorizzazione del proprietario del TPM per Active Directory Domain Services se sono state configurate le impostazioni criteri di gruppo appropriate.</span><span class="sxs-lookup"><span data-stu-id="6ae14-139">The **ChangeOwnerAuth** method backs up the new TPM owner authorization to Active Directory Domain Services if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="6ae14-140">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6ae14-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6ae14-141">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6ae14-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6ae14-142">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="6ae14-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6ae14-143">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="6ae14-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae14-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ae14-144">Requirements</span></span>



| <span data-ttu-id="6ae14-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ae14-145">Requirement</span></span> | <span data-ttu-id="6ae14-146">Valore</span><span class="sxs-lookup"><span data-stu-id="6ae14-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae14-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ae14-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae14-148">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ae14-148">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6ae14-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ae14-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae14-150">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6ae14-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6ae14-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6ae14-151">Namespace</span></span><br/>                | <span data-ttu-id="6ae14-152">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="6ae14-152">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="6ae14-153">MOF</span><span class="sxs-lookup"><span data-stu-id="6ae14-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ae14-154"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ae14-154"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ae14-155">DLL</span><span class="sxs-lookup"><span data-stu-id="6ae14-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ae14-156"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="6ae14-156"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ae14-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ae14-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae14-158">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="6ae14-158">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

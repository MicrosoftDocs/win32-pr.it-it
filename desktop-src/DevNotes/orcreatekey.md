---
description: Crea la chiave del registro di sistema specificata in un hive del registro di sistema offline. Se la chiave esiste già, la funzione la apre.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: Funzione ORCreateKey (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 9a14198cb6f1912612a092e003a68fd9ff49f867
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331957"
---
# <a name="orcreatekey-function"></a><span data-ttu-id="9e9f8-104">ORCreateKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="9e9f8-104">ORCreateKey function</span></span>

<span data-ttu-id="9e9f8-105">Crea la chiave del registro di sistema specificata in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-105">Creates the specified registry key in an offline registry hive.</span></span> <span data-ttu-id="9e9f8-106">Se la chiave esiste già, la funzione la apre.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-106">If the key already exists, the function opens it.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e9f8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e9f8-107">Syntax</span></span>


```C++
DWORD ORCreateKey(
  _In_      ORHKEY               Handle,
  _In_      PCWSTR               lpSubKey,
  _In_opt_  PWSTR                lpClass,
  _In_opt_  DWORD                dwOptions,
  _In_opt_  PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Out_     PORHKEY              phkResult,
  _Out_opt_ PDWORD               pdwDisposition
);
```



## <a name="parameters"></a><span data-ttu-id="9e9f8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e9f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e9f8-109">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e9f8-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9f8-110">Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="9e9f8-111">*lpSubKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e9f8-111">*lpSubKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9f8-112">Puntatore a una stringa Unicode che contiene il nome di una sottochiave che la funzione apre o crea.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-112">A pointer to a Unicode string that contains the name of a subkey that this function opens or creates.</span></span> <span data-ttu-id="9e9f8-113">Il parametro *lpSubKey* deve specificare una sottochiave della chiave identificata dal parametro *handle* . può essere fino a 32 livelli di profondità nell'albero del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-113">The *lpSubKey* parameter must specify a subkey of the key identified by the *Handle* parameter; it can be up to 32 levels deep in the registry tree.</span></span> <span data-ttu-id="9e9f8-114">Per ulteriori informazioni sui nomi delle chiavi, vedere [la struttura del registro di sistema](../sysinfo/structure-of-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="9e9f8-114">For more information about key names, see [Structure of the Registry](../sysinfo/structure-of-the-registry.md).</span></span>

<span data-ttu-id="9e9f8-115">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-115">This parameter cannot be **NULL**.</span></span>

<span data-ttu-id="9e9f8-116">Per i nomi di chiave non viene fatta distinzione tra maiuscole</span><span class="sxs-lookup"><span data-stu-id="9e9f8-116">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="9e9f8-117">*lpClass* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9e9f8-117">*lpClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9f8-118">Classe (tipo di oggetto) della chiave.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-118">The class (object type) of this key.</span></span> <span data-ttu-id="9e9f8-119">Questo parametro può essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-119">This parameter may be ignored.</span></span> <span data-ttu-id="9e9f8-120">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9e9f8-121">*dwOptions* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9e9f8-121">*dwOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9f8-122">Questo parametro può essere 0 o uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-122">This parameter can be 0 or one of the following values.</span></span>



| <span data-ttu-id="9e9f8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9e9f8-123">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="9e9f8-124">Significato</span><span class="sxs-lookup"><span data-stu-id="9e9f8-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <span data-ttu-id="9e9f8-125"><dt>**Reg \_ OPZIONE \_ Crea \_ collegamento**</dt> <dt>0x00000002L</dt></span><span class="sxs-lookup"><span data-stu-id="9e9f8-125"><dt>**REG\_OPTION\_CREATE\_LINK**</dt> <dt>0x00000002L</dt></span></span> </dl>    | <span data-ttu-id="9e9f8-126">La chiave è un collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-126">The key is a symbolic link.</span></span> <span data-ttu-id="9e9f8-127">Il percorso di destinazione viene assegnato al valore L "SymbolicLinkValue" della chiave.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-127">The target path is assigned to the L"SymbolicLinkValue" value of the key.</span></span> <span data-ttu-id="9e9f8-128">Il percorso di destinazione deve essere un percorso assoluto del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-128">The target path must be an absolute registry path.</span></span> <span data-ttu-id="9e9f8-129">Se questa opzione è impostata, è necessario impostare anche l' **\_ opzione reg \_ non \_ volatile** .</span><span class="sxs-lookup"><span data-stu-id="9e9f8-129">If this option is set, **REG\_OPTION\_NON\_VOLATILE** must also be set.</span></span> <br/> <span data-ttu-id="9e9f8-130">Se il parametro *lpSubKey* specifica una chiave esistente, deve essere stato creato con il **\_ \_ \_ collegamento reg Option create**.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-130">If the *lpSubKey* parameter specifies an existing key, it must have been created with **REG\_OPTION\_CREATE\_LINK**.</span></span><br/> <span data-ttu-id="9e9f8-131">I collegamenti simbolici del registro di sistema devono essere usati solo quando sono assolutamente necessari per la compatibilità delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-131">Registry symbolic links should be used only when absolutely necessary for application compatibility.</span></span> <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <span data-ttu-id="9e9f8-132"><dt>**Reg \_ OPZIONE \_ non \_ volatile**</dt> <dt>0x00000000L</dt></span><span class="sxs-lookup"><span data-stu-id="9e9f8-132"><dt>**REG\_OPTION\_NON\_VOLATILE**</dt> <dt>0x00000000L</dt></span></span> </dl> | <span data-ttu-id="9e9f8-133">La chiave non è volatile; si tratta dell'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-133">The key is not volatile; this is the default.</span></span> <span data-ttu-id="9e9f8-134">Le informazioni vengono archiviate in un file e mantenute al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-134">The information is stored in a file and is preserved when the system is restarted.</span></span> <span data-ttu-id="9e9f8-135">La funzione [**ORSaveHive**](orsavehive.md) Salva le chiavi che non sono volatili.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-135">The [**ORSaveHive**](orsavehive.md) function saves keys that are not volatile.</span></span><br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="9e9f8-136">*pSecurityDescriptor* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9e9f8-136">*pSecurityDescriptor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9f8-137">Puntatore a una struttura [di \_ descrittori di sicurezza](/windows/win32/api/winnt/ns-winnt-security_descriptor) che contiene un descrittore di sicurezza per la nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-137">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that contains a security descriptor for the new key.</span></span> <span data-ttu-id="9e9f8-138">Se *pSecurityDescriptor* è **null**, la chiave ottiene un descrittore di sicurezza predefinito.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-138">If *pSecurityDescriptor* is **NULL**, the key gets a default security descriptor.</span></span> <span data-ttu-id="9e9f8-139">Gli ACL in un descrittore di sicurezza predefinito per una chiave vengono ereditati dalla relativa chiave padre diretta.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-139">The ACLs in a default security descriptor for a key are inherited from its direct parent key.</span></span>

</dd> <dt>

<span data-ttu-id="9e9f8-140">*phkResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9e9f8-140">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9f8-141">Puntatore a una variabile che riceve un handle per la chiave aperta o creata.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-141">A pointer to a variable that receives a handle to the opened or created key.</span></span> <span data-ttu-id="9e9f8-142">Usare la funzione [**ORCloseKey**](orclosekey.md) per chiudere la chiave dopo aver terminato di usare l'handle.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-142">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> <dt>

<span data-ttu-id="9e9f8-143">*pdwDisposition* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9e9f8-143">*pdwDisposition* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9e9f8-144">Puntatore a una variabile che riceve uno dei seguenti valori di disposizione.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-144">A pointer to a variable that receives one of the following disposition values.</span></span>



| <span data-ttu-id="9e9f8-145">Valore</span><span class="sxs-lookup"><span data-stu-id="9e9f8-145">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="9e9f8-146">Significato</span><span class="sxs-lookup"><span data-stu-id="9e9f8-146">Meaning</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <span data-ttu-id="9e9f8-147"><dt>**Reg \_ CREAZIONE della \_ nuova \_ chiave**</dt> <dt>0x00000001L</dt></span><span class="sxs-lookup"><span data-stu-id="9e9f8-147"><dt>**REG\_CREATED\_NEW\_KEY**</dt> <dt>0x00000001L</dt></span></span> </dl>             | <span data-ttu-id="9e9f8-148">La chiave non esiste ed è stata creata.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-148">The key did not exist and was created.</span></span><br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <span data-ttu-id="9e9f8-149"><dt>**Reg \_ 0x00000002L \_ \_ chiave esistente aperta**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9e9f8-149"><dt>**REG\_OPENED\_EXISTING\_KEY**</dt> <dt>0x00000002L</dt></span></span> </dl> | <span data-ttu-id="9e9f8-150">La chiave esisteva ed è stata semplicemente aperta senza essere modificata.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-150">The key existed and was simply opened without being changed.</span></span><br/> |



 

<span data-ttu-id="9e9f8-151">Se *pdwDisposition* è **null**, non viene restituita alcuna informazione sulla disposizione.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-151">If *pdwDisposition* is **NULL**, no disposition information is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e9f8-152">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e9f8-152">Return value</span></span>

<span data-ttu-id="9e9f8-153">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-153">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="9e9f8-154">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-154">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="9e9f8-155">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-155">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="9e9f8-156">Se il parametro *dwOptions* è impostato con **l' \_ opzione reg \_ Create \_ link** ma l' **opzione reg \_ \_ non \_ volatile** è deselezionata, oppure se l'handle da restituire è un handle per la chiave radice dell'hive, la funzione restituisce l'errore \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="9e9f8-156">If the *dwOptions* parameter is set with **REG\_OPTION\_CREATE\_LINK** but **REG\_OPTION\_NON\_VOLATILE** is clear, or if the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e9f8-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e9f8-157">Remarks</span></span>

<span data-ttu-id="9e9f8-158">La chiave creata dalla funzione **ORCreateKey** non contiene valori.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-158">The key that the **ORCreateKey** function creates has no values.</span></span> <span data-ttu-id="9e9f8-159">Per impostare i valori delle chiavi, un'applicazione può usare la funzione [**ORSetValue**](orsetvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="9e9f8-159">An application can use the [**ORSetValue**](orsetvalue.md) function to set key values.</span></span>

<span data-ttu-id="9e9f8-160">Non è possibile usare la funzione **ORCreateKey** per creare la chiave radice in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-160">The **ORCreateKey** function cannot be used to create the root key in an offline registry hive.</span></span> <span data-ttu-id="9e9f8-161">Usare la funzione [**ORCreateHive**](orcreatehive.md) per creare la chiave radice e ottenere un handle per la chiave.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-161">Use the [**ORCreateHive**](orcreatehive.md) function to create the root key and obtain a handle to the key.</span></span>

<span data-ttu-id="9e9f8-162">Il registro offline non supporta il salvataggio di singole chiavi.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-162">The offline registry does not support saving individual keys.</span></span> <span data-ttu-id="9e9f8-163">Usare la funzione [**ORSaveHive**](orsavehive.md) per salvare una chiave e le relative sottochiavi in hive.</span><span class="sxs-lookup"><span data-stu-id="9e9f8-163">Use the [**ORSaveHive**](orsavehive.md) function to save a key and its subkeys in a hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e9f8-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e9f8-164">Requirements</span></span>



| <span data-ttu-id="9e9f8-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e9f8-165">Requirement</span></span> | <span data-ttu-id="9e9f8-166">Valore</span><span class="sxs-lookup"><span data-stu-id="9e9f8-166">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e9f8-167">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9e9f8-167">Redistributable</span></span><br/> | <span data-ttu-id="9e9f8-168">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="9e9f8-168">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="9e9f8-169">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e9f8-169">Header</span></span><br/>          | <dl> <span data-ttu-id="9e9f8-170"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e9f8-170"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e9f8-171">DLL</span><span class="sxs-lookup"><span data-stu-id="9e9f8-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="9e9f8-172"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e9f8-172"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e9f8-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e9f8-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e9f8-174">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="9e9f8-174">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="9e9f8-175">**ORCreateHive**</span><span class="sxs-lookup"><span data-stu-id="9e9f8-175">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="9e9f8-176">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="9e9f8-176">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="9e9f8-177">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="9e9f8-177">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="9e9f8-178">descrittore di sicurezza \_</span><span class="sxs-lookup"><span data-stu-id="9e9f8-178">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 

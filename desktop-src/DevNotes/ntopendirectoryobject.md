---
description: Apre un oggetto directory esistente.
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: NtOpenDirectoryObject (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ceea03c36e0617e2f48887275e7867e3589c87ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325672"
---
# <a name="ntopendirectoryobject-function"></a><span data-ttu-id="cbd73-103">NtOpenDirectoryObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="cbd73-103">NtOpenDirectoryObject function</span></span>

<span data-ttu-id="cbd73-104">\[Questa funzione può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="cbd73-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="cbd73-105">Apre un oggetto directory esistente.</span><span class="sxs-lookup"><span data-stu-id="cbd73-105">Opens an existing directory object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd73-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cbd73-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtOpenDirectoryObject(
  _Out_ PHANDLE            DirectoryHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="cbd73-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cbd73-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbd73-108">*DirectoryHandle* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cbd73-108">*DirectoryHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbd73-109">Handle per l'oggetto directory appena aperto.</span><span class="sxs-lookup"><span data-stu-id="cbd73-109">A handle to the newly opened directory object.</span></span>

</dd> <dt>

<span data-ttu-id="cbd73-110">*DesiredAccess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cbd73-110">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbd73-111">[**\_ Maschera di accesso**](../secauthz/access-mask.md) che specifica l'accesso richiesto all'oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="cbd73-111">An [**ACCESS\_MASK**](../secauthz/access-mask.md) that specifies the requested access to the directory object.</span></span> <span data-ttu-id="cbd73-112">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="cbd73-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="cbd73-113">Valore</span><span class="sxs-lookup"><span data-stu-id="cbd73-113">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="cbd73-114">Significato</span><span class="sxs-lookup"><span data-stu-id="cbd73-114">Meaning</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <span data-ttu-id="cbd73-115"><dt>**Directory \_ di**</dt> <dt>0x0001</dt> query</span><span class="sxs-lookup"><span data-stu-id="cbd73-115"><dt>**DIRECTORY\_QUERY**</dt> <dt>0x0001</dt></span></span> </dl>                                            | <span data-ttu-id="cbd73-116">Eseguire query sull'accesso all'oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="cbd73-116">Query access to the directory object.</span></span><br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <span data-ttu-id="cbd73-117"><dt>**Directory \_ di ATTRAVERSA**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="cbd73-117"><dt>**DIRECTORY\_TRAVERSE**</dt> <dt>0x0002</dt></span></span> </dl>                                   | <span data-ttu-id="cbd73-118">Accesso nome-ricerca all'oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="cbd73-118">Name-lookup access to the directory object.</span></span><br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <span data-ttu-id="cbd73-119"><dt>**Directory \_ di Crea \_ oggetto**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="cbd73-119"><dt>**DIRECTORY\_CREATE\_OBJECT**</dt> <dt>0x0004</dt></span></span> </dl>                   | <span data-ttu-id="cbd73-120">Accesso per la creazione di nomi all'oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="cbd73-120">Name-creation access to the directory object.</span></span><br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <span data-ttu-id="cbd73-121"><dt>**Directory \_ di CREAZIONE della \_ sottodirectory**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="cbd73-121"><dt>**DIRECTORY\_CREATE\_SUBDIRECTORY**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="cbd73-122">Sottodirectory-creazione dell'accesso all'oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="cbd73-122">Subdirectory-creation access to the directory object.</span></span><br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <span data-ttu-id="cbd73-123"><dt>**Directory \_ di TUTTI \_**</dt> <dt>i diritti di accesso standard \_ \_ richiesti \| 0xF</dt></span><span class="sxs-lookup"><span data-stu-id="cbd73-123"><dt>**DIRECTORY\_ALL\_ACCESS**</dt> <dt>STANDARD\_RIGHTS\_REQUIRED \| 0xF</dt></span></span> </dl> | <span data-ttu-id="cbd73-124">Tutti i diritti precedenti e i **diritti standard sono \_ \_ obbligatori**.</span><span class="sxs-lookup"><span data-stu-id="cbd73-124">All of the preceding rights plus **STANDARD\_RIGHTS\_REQUIRED**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cbd73-125">*ObjectAttributes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cbd73-125">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbd73-126">Attributi per l'oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="cbd73-126">The attributes for the directory object.</span></span> <span data-ttu-id="cbd73-127">Per inizializzare la struttura degli **\_ attributi dell'oggetto** , usare la macro **InitializeObjectAttributes** .</span><span class="sxs-lookup"><span data-stu-id="cbd73-127">To initialize the **OBJECT\_ATTRIBUTES** structure, use the **InitializeObjectAttributes** macro.</span></span> <span data-ttu-id="cbd73-128">Per ulteriori informazioni, vedere la documentazione relativa a questi elementi nella documentazione relativa a WDK.</span><span class="sxs-lookup"><span data-stu-id="cbd73-128">For more information, see the documentation for these items in the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbd73-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cbd73-129">Return value</span></span>

<span data-ttu-id="cbd73-130">La funzione restituisce lo stato \_ di esito positivo o uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="cbd73-130">The function returns STATUS\_SUCCESS or an error status.</span></span> <span data-ttu-id="cbd73-131">I codici di stato possibili includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="cbd73-131">The possible status codes include the following.</span></span>



| <span data-ttu-id="cbd73-132">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cbd73-132">Return code</span></span>                                                                                                       | <span data-ttu-id="cbd73-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbd73-133">Description</span></span>                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cbd73-134"><dt>**STATO \_ risorse insufficienti \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd73-134"><dt>**STATUS\_INSUFFICIENT\_RESOURCES**</dt></span></span> </dl>    | <span data-ttu-id="cbd73-135">Non è stato possibile allocare un buffer temporaneo richiesto da questa funzione.</span><span class="sxs-lookup"><span data-stu-id="cbd73-135">A temporary buffer required by this function could not be allocated.</span></span><br/>                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="cbd73-136"><dt>**STATO \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd73-136"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>         | <span data-ttu-id="cbd73-137">Il parametro ObjectAttributes specificato è un puntatore **null** , non un puntatore valido a una struttura degli **\_ attributi degli oggetti** oppure alcuni membri specificati nella struttura degli **\_ attributi dell'oggetto** non sono validi.</span><span class="sxs-lookup"><span data-stu-id="cbd73-137">The specified ObjectAttributes parameter was a **NULL** pointer, not a valid pointer to an **OBJECT\_ATTRIBUTES** structure, or some of the members specified in the **OBJECT\_ATTRIBUTES** structure were not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="cbd73-138"><dt>**\_nome oggetto \_ stato \_ non valido**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd73-138"><dt>**STATUS\_OBJECT\_NAME\_INVALID**</dt></span></span> </dl>      | <span data-ttu-id="cbd73-139">Il parametro *ObjectAttributes* contiene un membro **ObjectName** nella struttura degli **\_ attributi dell'oggetto** non valida perché è stata trovata una stringa vuota dopo il carattere **\_ \_ \_ separatore del percorso del nome dell'oggetto** .</span><span class="sxs-lookup"><span data-stu-id="cbd73-139">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure that was not valid because an empty string was found after the **OBJECT\_NAME\_PATH\_SEPARATOR** character.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="cbd73-140"><dt>**\_nome oggetto \_ stato \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd73-140"><dt>**STATUS\_OBJECT\_NAME\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="cbd73-141">Il parametro *ObjectAttributes* contiene un membro **ObjectName** nella struttura degli **\_ attributi dell'oggetto** che non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="cbd73-141">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure that could not be found.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="cbd73-142"><dt>**il \_ percorso dell'oggetto stato non è stato \_ \_ \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd73-142"><dt>**STATUS\_OBJECT\_PATH\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="cbd73-143">Il parametro *ObjectAttributes* contiene un membro **ObjectName** nella struttura degli **\_ attributi dell'oggetto** con un percorso dell'oggetto che non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="cbd73-143">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure with an object path that could not be found.</span></span> <br/>                                                                                                                                      |
| <dl> <span data-ttu-id="cbd73-144"><dt>**Stato \_ di sintassi del percorso dell'oggetto non \_ \_ \_ valida**</dt></span><span class="sxs-lookup"><span data-stu-id="cbd73-144"><dt>**STATUS\_OBJECT\_PATH\_SYNTAX\_BAD** </dt></span></span> </dl> | <span data-ttu-id="cbd73-145">Il parametro *ObjectAttributes* non contiene un membro **RootDirectory** , ma il membro **ObjectName** nella struttura **degli \_ attributi dell'oggetto** è una stringa vuota o non contiene un **carattere \_ \_ \_ separatore del percorso del nome dell'oggetto** .</span><span class="sxs-lookup"><span data-stu-id="cbd73-145">The *ObjectAttributes* parameter did not contain a **RootDirectory** member, but the **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure was an empty string or did not contain an **OBJECT\_NAME\_PATH\_SEPARATOR** character.</span></span> <span data-ttu-id="cbd73-146">Indica una sintassi non corretta per il percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cbd73-146">This indicates incorrect syntax for the object path.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cbd73-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbd73-147">Remarks</span></span>

<span data-ttu-id="cbd73-148">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="cbd73-148">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbd73-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbd73-149">Requirements</span></span>



| <span data-ttu-id="cbd73-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbd73-150">Requirement</span></span> | <span data-ttu-id="cbd73-151">Valore</span><span class="sxs-lookup"><span data-stu-id="cbd73-151">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd73-152">DLL</span><span class="sxs-lookup"><span data-stu-id="cbd73-152">DLL</span></span><br/> | <dl> <span data-ttu-id="cbd73-153"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbd73-153"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbd73-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbd73-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd73-155">**NtQueryDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="cbd73-155">**NtQueryDirectoryObject**</span></span>](ntquerydirectoryobject.md)
</dt> </dl>

 

 

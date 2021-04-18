---
description: Recupera i flag virtuali nella chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.
ms.assetid: 2a04c257-e3b0-415b-97d2-616e12513a0a
title: Funzione ORGetVirtualFlags (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 36c41bb9e510a107689790162e03e3bb86c8de1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329422"
---
# <a name="orgetvirtualflags-function"></a><span data-ttu-id="a2a79-103">ORGetVirtualFlags (funzione)</span><span class="sxs-lookup"><span data-stu-id="a2a79-103">ORGetVirtualFlags function</span></span>

<span data-ttu-id="a2a79-104">Recupera i flag virtuali nella chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="a2a79-104">Retrieves the virtual flags on the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2a79-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2a79-105">Syntax</span></span>


```C++
DWORD ORGetVirtualFlags(
  _In_  ORHKEY Handle,
  _Out_ PDWORD pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a2a79-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2a79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2a79-107">*Gestisci* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2a79-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a79-108">Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="a2a79-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="a2a79-109">*pdwFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a2a79-109">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a79-110">Puntatore a una variabile per ricevere i flag di virtualizzazione impostati per la chiave.</span><span class="sxs-lookup"><span data-stu-id="a2a79-110">A pointer to a variable to receive the virtualization flags set for the key.</span></span> <span data-ttu-id="a2a79-111">Dopo la restituzione della funzione, questo parametro può essere uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a2a79-111">After the function returns, this parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="a2a79-112">Valore</span><span class="sxs-lookup"><span data-stu-id="a2a79-112">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="a2a79-113">Significato</span><span class="sxs-lookup"><span data-stu-id="a2a79-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <span data-ttu-id="a2a79-114"><dt>**Reg \_ CHIAVE \_ \_ \_ non riuscita**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a2a79-114"><dt>**REG\_KEY\_DONT\_SILENT\_FAIL**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="a2a79-115">Se questo flag è impostato e un'operazione di apertura non riesce su una chiave abilitata per la virtualizzazione, il registro di sistema non tenta di riaprire la chiave.</span><span class="sxs-lookup"><span data-stu-id="a2a79-115">If this flag is set and an Open operation fails on a key that has virtualization enabled, the registry does not attempt to reopen the key.</span></span> <span data-ttu-id="a2a79-116">Se questo flag è chiaro, il registro di sistema tenta di riaprire la chiave con l' \_ accesso massimo consentito.</span><span class="sxs-lookup"><span data-stu-id="a2a79-116">If this flag is clear, the registry attempts to reopen the key with MAXIMUM\_ALLOWED access.</span></span><br/>                                                                                            |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <span data-ttu-id="a2a79-117"><dt>**Reg \_ CHIAVE \_ dont \_ virtualizza**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a2a79-117"><dt>**REG\_KEY\_DONT\_VIRTUALIZE**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="a2a79-118">Se questo flag è impostato e un'operazione di creazione della chiave ha esito negativo perché il chiamante non ha la chiave \_ di creazione della chiave \_ secondaria \_ direttamente nella chiave padre, il registro di sistema non riesce a creare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a2a79-118">If this flag is set and a Create Key operation fails because the caller does not have the KEY\_CREATE\_SUB\_KEY right on the parent key, the registry fails the Create operation.</span></span> <span data-ttu-id="a2a79-119">Se questo flag è chiaro, il registro di sistema tenta di creare la chiave nell'archivio virtuale.</span><span class="sxs-lookup"><span data-stu-id="a2a79-119">If this flag is clear, the registry attempts to create the key in the virtual store.</span></span> <span data-ttu-id="a2a79-120">Il chiamante deve avere la chiave \_ Read right sulla chiave padre.</span><span class="sxs-lookup"><span data-stu-id="a2a79-120">The caller must have the KEY\_READ right on the parent key.</span></span><br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <span data-ttu-id="a2a79-121"><dt>**Reg \_ \_ \_ Flag di rimaledizione della chiave**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a2a79-121"><dt>**REG\_KEY\_RECURSE\_FLAG**</dt> <dt>8</dt></span></span> </dl>              | <span data-ttu-id="a2a79-122">Se questo flag è impostato, i flag di virtualizzazione del registro di sistema vengono propagati dalla chiave padre.</span><span class="sxs-lookup"><span data-stu-id="a2a79-122">If this flag is set, registry virtualization flags are propagated from the parent key.</span></span> <span data-ttu-id="a2a79-123">Se questo flag è chiaro, i flag di virtualizzazione del registro di sistema non vengono propagati.</span><span class="sxs-lookup"><span data-stu-id="a2a79-123">If this flag is clear, registry virtualization flags are not propagated.</span></span><br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2a79-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2a79-124">Return value</span></span>

<span data-ttu-id="a2a79-125">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a2a79-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a2a79-126">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="a2a79-126">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="a2a79-127">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="a2a79-127">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2a79-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2a79-128">Remarks</span></span>

<span data-ttu-id="a2a79-129">La virtualizzazione del registro di sistema è una tecnologia provvisoria per la compatibilità delle applicazioni che consente di reindirizzare le operazioni di scrittura del registro di sistema a posizioni per utente.</span><span class="sxs-lookup"><span data-stu-id="a2a79-129">Registry virtualization is an interim application compatibility technology that enables registry write operations that have global impact to be redirected to per-user locations.</span></span> <span data-ttu-id="a2a79-130">Questo reindirizzamento è trasparente per le applicazioni che leggono o scrivono nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a2a79-130">This redirection is transparent to applications reading from or writing to the registry.</span></span>

<span data-ttu-id="a2a79-131">La virtualizzazione del registro di sistema è supportata a partire da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a2a79-131">Registry virtualization is supported starting with Windows Vista.</span></span> <span data-ttu-id="a2a79-132">Tuttavia, Microsoft intende rimuoverlo dalle versioni future del sistema operativo Windows, in quanto le altre applicazioni vengono rese compatibili con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a2a79-132">However, Microsoft intends to remove it from future versions of the Windows operating system as more applications are made compatible with Windows Vista.</span></span> <span data-ttu-id="a2a79-133">Pertanto, le applicazioni non devono dipendere dal comportamento della virtualizzazione del registro di sistema nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a2a79-133">Therefore, applications should not depend on the behavior of registry virtualization in the system.</span></span>

<span data-ttu-id="a2a79-134">La virtualizzazione del registro di sistema è abilitata solo per gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2a79-134">Registry virtualization is enabled only for the following:</span></span>

-   <span data-ttu-id="a2a79-135">processi interattivi a 32 bit</span><span class="sxs-lookup"><span data-stu-id="a2a79-135">32-bit interactive processes</span></span>
-   <span data-ttu-id="a2a79-136">Chiavi nel **\_ software del \_ computer \\ locale HKEY**</span><span class="sxs-lookup"><span data-stu-id="a2a79-136">Keys in **HKEY\_LOCAL\_MACHINE\\Software**</span></span>
-   <span data-ttu-id="a2a79-137">Chiavi in cui un amministratore può scrivere</span><span class="sxs-lookup"><span data-stu-id="a2a79-137">Keys that an administrator can write to</span></span>

<span data-ttu-id="a2a79-138">Per ulteriori informazioni, vedere la pagina relativa alla [virtualizzazione del registro](../sysinfo/registry-virtualization.md).</span><span class="sxs-lookup"><span data-stu-id="a2a79-138">For more information, see [Registry Virtualization](../sysinfo/registry-virtualization.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2a79-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2a79-139">Requirements</span></span>



| <span data-ttu-id="a2a79-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2a79-140">Requirement</span></span> | <span data-ttu-id="a2a79-141">Valore</span><span class="sxs-lookup"><span data-stu-id="a2a79-141">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2a79-142">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a2a79-142">Redistributable</span></span><br/> | <span data-ttu-id="a2a79-143">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="a2a79-143">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="a2a79-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2a79-144">Header</span></span><br/>          | <dl> <span data-ttu-id="a2a79-145"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2a79-145"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2a79-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a2a79-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="a2a79-147"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2a79-147"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2a79-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2a79-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2a79-149">**ORSetVirtualFlags**</span><span class="sxs-lookup"><span data-stu-id="a2a79-149">**ORSetVirtualFlags**</span></span>](orsetvirtualflags.md)
</dt> <dt>

[<span data-ttu-id="a2a79-150">Virtualizzazione del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="a2a79-150">Registry Virtualization</span></span>](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 

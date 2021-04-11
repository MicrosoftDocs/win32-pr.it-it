---
title: Funzione DsIsNTDSOnline (ntdsbcli. h)
description: Determina se Active Directory Domain Services sono online nel server specificato.
ms.assetid: 8f46e4d8-6d05-402c-a5b4-291fd2d6609b
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsIsNTDSOnline
topic_type:
- apiref
api_name:
- DsIsNTDSOnline
- DsIsNTDSOnlineA
- DsIsNTDSOnlineW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f6728f4481eb8820055b48f10cfa0f94c7aaa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119850"
---
# <a name="dsisntdsonline-function"></a><span data-ttu-id="f70b2-104">DsIsNTDSOnline (funzione)</span><span class="sxs-lookup"><span data-stu-id="f70b2-104">DsIsNTDSOnline function</span></span>

<span data-ttu-id="f70b2-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="f70b2-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f70b2-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="f70b2-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f70b2-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="f70b2-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="f70b2-108">La funzione **DsIsNTDSOnline** determina se Active Directory Domain Services sono online nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="f70b2-108">The **DsIsNTDSOnline** function determines if Active Directory Domain Services are online on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f70b2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f70b2-109">Syntax</span></span>


```C++
HRESULT DsIsNTDSOnline(
  _In_  LPCTSTR szServerName,
  _Out_ BOOL    *pfNTDSOnline
);
```



## <a name="parameters"></a><span data-ttu-id="f70b2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f70b2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f70b2-111">*szServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f70b2-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f70b2-112">Puntatore a una stringa con terminazione null che contiene il nome del server da testare.</span><span class="sxs-lookup"><span data-stu-id="f70b2-112">Pointer to a null-terminated string that contains the name of the server to test.</span></span> <span data-ttu-id="f70b2-113">Le barre rovesciate precedenti sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="f70b2-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="f70b2-114">Il server deve essere lo stesso computer da cui viene chiamata la funzione.</span><span class="sxs-lookup"><span data-stu-id="f70b2-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="f70b2-115">Il nome del server non può contenere caratteri di sottolineatura ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="f70b2-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="f70b2-116">Un esempio di nome di server è " \\ \\ Server1".</span><span class="sxs-lookup"><span data-stu-id="f70b2-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="f70b2-117">*pfNTDSOnline* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f70b2-117">*pfNTDSOnline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f70b2-118">Puntatore al valore **bool** che riceve il risultato.</span><span class="sxs-lookup"><span data-stu-id="f70b2-118">Pointer to **BOOL** value that receives the result.</span></span> <span data-ttu-id="f70b2-119">Riceve **true** se il servizio directory è online o **false** se il servizio directory è offline.</span><span class="sxs-lookup"><span data-stu-id="f70b2-119">Receives **TRUE** if the directory service is online or **FALSE** if the directory service is offline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f70b2-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f70b2-120">Return value</span></span>

<span data-ttu-id="f70b2-121">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="f70b2-121">Returns **S\_OK** if the function is successful or an error code otherwise.</span></span> <span data-ttu-id="f70b2-122">Nell'elenco seguente sono elencati i possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="f70b2-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="f70b2-123">**ERRORE di \_ accesso \_ negato**</span><span class="sxs-lookup"><span data-stu-id="f70b2-123">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="f70b2-124">Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="f70b2-124">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="f70b2-125">La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="f70b2-125">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="f70b2-126">**hrCouldNotConnect**</span><span class="sxs-lookup"><span data-stu-id="f70b2-126">**hrCouldNotConnect**</span></span>
</dt> <dd>

<span data-ttu-id="f70b2-127">Il server in *szServerName* non è stato trovato, non è un controller di dominio oppure *szServerName* non è formattato correttamente.</span><span class="sxs-lookup"><span data-stu-id="f70b2-127">The server in *szServerName* cannot be found, is not a domain controller, or *szServerName* is not formatted correctly.</span></span> <span data-ttu-id="f70b2-128">Questo valore è definito in ntdsbmsg. h.</span><span class="sxs-lookup"><span data-stu-id="f70b2-128">This value is defined in Ntdsbmsg.h.</span></span>

</dd> <dt>

<span data-ttu-id="f70b2-129">**\_binding RPC S \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="f70b2-129">**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd>

<span data-ttu-id="f70b2-130">La funzione [**DsIsNTDSOnline**](dsisntdsonline.md) viene chiamata in modalità remota o il server in *szServerName* non è un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="f70b2-130">The [**DsIsNTDSOnline**](dsisntdsonline.md) function is being called remotely or the server in *szServerName* is not a domain controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f70b2-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="f70b2-131">Remarks</span></span>

<span data-ttu-id="f70b2-132">Chiamare questa funzione prima di chiamare una delle funzioni di backup o ripristino della directory.</span><span class="sxs-lookup"><span data-stu-id="f70b2-132">Call this function before calling any of the directory backup or restore functions.</span></span> <span data-ttu-id="f70b2-133">Per eseguire un backup, la directory deve essere online.</span><span class="sxs-lookup"><span data-stu-id="f70b2-133">The directory must be online in order to perform a backup.</span></span> <span data-ttu-id="f70b2-134">Per eseguire un ripristino è necessario che la directory sia offline.</span><span class="sxs-lookup"><span data-stu-id="f70b2-134">The directory must by offline to perform a restore.</span></span>

<span data-ttu-id="f70b2-135">Questa funzione può essere chiamata solo da un controller di dominio che è anche il server di destinazione specificato in *szServerName*.</span><span class="sxs-lookup"><span data-stu-id="f70b2-135">This function can only be called from a domain controller that is also the target server specified in *szServerName*.</span></span> <span data-ttu-id="f70b2-136">Questa funzione non può essere chiamata in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="f70b2-136">This function cannot be called remotely.</span></span>

## <a name="requirements"></a><span data-ttu-id="f70b2-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f70b2-137">Requirements</span></span>



| <span data-ttu-id="f70b2-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f70b2-138">Requirement</span></span> | <span data-ttu-id="f70b2-139">Valore</span><span class="sxs-lookup"><span data-stu-id="f70b2-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f70b2-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f70b2-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f70b2-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f70b2-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f70b2-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f70b2-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f70b2-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f70b2-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f70b2-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f70b2-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f70b2-145"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="f70b2-145"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="f70b2-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="f70b2-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="f70b2-147"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f70b2-147"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="f70b2-148">DLL</span><span class="sxs-lookup"><span data-stu-id="f70b2-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f70b2-149"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f70b2-149"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="f70b2-150">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f70b2-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f70b2-151">**DsIsNTDSOnlineW** (Unicode) e **DsIsNTDSOnlineA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f70b2-151">**DsIsNTDSOnlineW** (Unicode) and **DsIsNTDSOnlineA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f70b2-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f70b2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70b2-153">**DsSetAuthIdentity**</span><span class="sxs-lookup"><span data-stu-id="f70b2-153">**DsSetAuthIdentity**</span></span>](dssetauthidentity.md)
</dt> <dt>

[<span data-ttu-id="f70b2-154">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="f70b2-154">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="f70b2-155">Backup e ripristino di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="f70b2-155">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> </dl>

 


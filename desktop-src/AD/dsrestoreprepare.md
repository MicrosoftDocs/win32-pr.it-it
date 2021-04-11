---
title: Funzione DsRestorePrepare (ntdsbcli. h)
description: Si connette al server di directory specificato e lo prepara per l'operazione di ripristino.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsRestorePrepare
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb040a315b6cc94f2d296b032a954b00473a4ca2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119606"
---
# <a name="dsrestoreprepare-function"></a><span data-ttu-id="eb311-104">DsRestorePrepare (funzione)</span><span class="sxs-lookup"><span data-stu-id="eb311-104">DsRestorePrepare function</span></span>

<span data-ttu-id="eb311-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="eb311-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eb311-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="eb311-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="eb311-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="eb311-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="eb311-108">La funzione **DsRestorePrepare** si connette al server di directory specificato e la prepara per l'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="eb311-108">The **DsRestorePrepare** function connects to the specified directory server and prepares it for the restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb311-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb311-109">Syntax</span></span>


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a><span data-ttu-id="eb311-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb311-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb311-111">*szServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb311-111">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb311-112">Puntatore a una stringa con terminazione null che contiene il nome del server da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="eb311-112">Pointer to a null-terminated string that contains the name of the server to restore.</span></span> <span data-ttu-id="eb311-113">Le barre rovesciate precedenti sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="eb311-113">Preceding backslashes are optional.</span></span> <span data-ttu-id="eb311-114">Il server deve essere lo stesso computer da cui viene chiamata la funzione.</span><span class="sxs-lookup"><span data-stu-id="eb311-114">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="eb311-115">Il nome del server non può contenere caratteri di sottolineatura ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="eb311-115">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="eb311-116">Un esempio di nome di server è " \\ \\ Server1".</span><span class="sxs-lookup"><span data-stu-id="eb311-116">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="eb311-117">*rtFlag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb311-117">*rtFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb311-118">Specifica il tipo di ripristino da eseguire.</span><span class="sxs-lookup"><span data-stu-id="eb311-118">Specifies the type of restoration to perform.</span></span> <span data-ttu-id="eb311-119">Può essere zero o uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="eb311-119">This can be zero or one of the following values.</span></span>

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span data-ttu-id="eb311-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**tipo di ripristino \_ \_ Catchup**</span><span class="sxs-lookup"><span data-stu-id="eb311-120"><span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**RESTORE\_TYPE\_CATCHUP**</span></span>


</dt> <dd>

<span data-ttu-id="eb311-121">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="eb311-121">Default.</span></span> <span data-ttu-id="eb311-122">La versione ripristinata viene riconciliata attraverso la logica di riconciliazione standard, in modo che il DIT ripristinato possa essere sincronizzato con altri computer server aziendali.</span><span class="sxs-lookup"><span data-stu-id="eb311-122">The restored version is reconciled through the standard reconciliation logic so that the restored DIT can synchronize with other enterprise server computers.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span data-ttu-id="eb311-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**tipo di ripristino \_ \_ AUTHORATATIVE**</span><span class="sxs-lookup"><span data-stu-id="eb311-123"><span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**RESTORE\_TYPE\_AUTHORATATIVE**</span></span>


</dt> <dd>

<span data-ttu-id="eb311-124">Non supportato.</span><span class="sxs-lookup"><span data-stu-id="eb311-124">Not Supported.</span></span>

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span data-ttu-id="eb311-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**tipo di ripristino \_ \_ online**</span><span class="sxs-lookup"><span data-stu-id="eb311-125"><span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**RESTORE\_TYPE\_ONLINE**</span></span>


</dt> <dd>

<span data-ttu-id="eb311-126">Non supportato.</span><span class="sxs-lookup"><span data-stu-id="eb311-126">Not Supported.</span></span> <span data-ttu-id="eb311-127">Il ripristino viene eseguito quando NTDS è online.</span><span class="sxs-lookup"><span data-stu-id="eb311-127">Restoration is performed when NTDS is online.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="eb311-128">*pvExpiryToken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb311-128">*pvExpiryToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb311-129">Puntatore al token di scadenza associato al backup da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="eb311-129">Pointer to the expiry token associated with the backup being restored.</span></span> <span data-ttu-id="eb311-130">Questo token è stato ottenuto dalla funzione [**DsBackupPrepare**](dsbackupprepare.md) quando è stato eseguito il backup della directory.</span><span class="sxs-lookup"><span data-stu-id="eb311-130">This token was obtained from the [**DsBackupPrepare**](dsbackupprepare.md) function when the directory was backed up.</span></span>

<span data-ttu-id="eb311-131">Se questo parametro è **null**, l'handle restituito in *phbc* può essere utilizzato solo per ottenere le directory di ripristino con la funzione [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) .</span><span class="sxs-lookup"><span data-stu-id="eb311-131">If this parameter is **NULL**, the handle returned in *phbc* can only be used to obtain the restoration directories with the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="eb311-132">Non è possibile usare l'handle per altre funzioni di ripristino.</span><span class="sxs-lookup"><span data-stu-id="eb311-132">The handle cannot be used for any other restoration functions.</span></span>

</dd> <dt>

<span data-ttu-id="eb311-133">*cbExpiryTokenSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb311-133">*cbExpiryTokenSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb311-134">Contiene la dimensione, in byte, del token di scadenza in *pvExpiryToken*.</span><span class="sxs-lookup"><span data-stu-id="eb311-134">Contains the size, in bytes, of the expiry token in *pvExpiryToken*.</span></span>

</dd> <dt>

<span data-ttu-id="eb311-135">*phbc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="eb311-135">*phbc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb311-136">Puntatore a un valore **HBC** che riceve l'handle per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="eb311-136">Pointer to an **HBC** value that receives the handle for the restore.</span></span> <span data-ttu-id="eb311-137">Questo handle viene utilizzato per chiamare altre funzioni di ripristino del servizio directory, ad esempio [**DsBackupOpenFile**](dsbackupopenfile.md) e [**DsRestoreEnd**](dsrestoreend.md).</span><span class="sxs-lookup"><span data-stu-id="eb311-137">This handle is used when calling other Directory Service restore functions, such as [**DsBackupOpenFile**](dsbackupopenfile.md) and [**DsRestoreEnd**](dsrestoreend.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb311-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb311-138">Return value</span></span>

<span data-ttu-id="eb311-139">Se ha esito positivo, restituisce un codice **HRESULT** standard; in caso contrario, viene restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="eb311-139">If successful, returns a standard **HRESULT** codes; otherwise, a failure code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb311-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb311-140">Remarks</span></span>

<span data-ttu-id="eb311-141">La funzione **DsRestorePrepare** richiede che il chiamante sia un membro del gruppo Administrators nel server.</span><span class="sxs-lookup"><span data-stu-id="eb311-141">The **DsRestorePrepare** function requires that the caller is a member of the Administrators group on the server.</span></span>

<span data-ttu-id="eb311-142">**DsRestorePrepare** può essere usato con o senza un token fornito.</span><span class="sxs-lookup"><span data-stu-id="eb311-142">**DsRestorePrepare** may be used with or without a token provided.</span></span> <span data-ttu-id="eb311-143">Se il token viene fornito, viene verificata la scadenza e tutte le operazioni sono consentite nel contesto restituito.</span><span class="sxs-lookup"><span data-stu-id="eb311-143">If the token is provided, it is checked for expiration, and all operations are allowed on the context returned.</span></span> <span data-ttu-id="eb311-144">Se il token non viene specificato, il contesto restituito viene limitato e può essere usato solo per la funzione [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) .</span><span class="sxs-lookup"><span data-stu-id="eb311-144">If the token is not provided, the context returned is restricted, and may be used only for the [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) function.</span></span> <span data-ttu-id="eb311-145">Non può essere usata per la funzione [**DsRestoreRegister**](dsrestoreregister.md) .</span><span class="sxs-lookup"><span data-stu-id="eb311-145">It may not be used for the [**DsRestoreRegister**](dsrestoreregister.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb311-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb311-146">Requirements</span></span>



| <span data-ttu-id="eb311-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb311-147">Requirement</span></span> | <span data-ttu-id="eb311-148">Valore</span><span class="sxs-lookup"><span data-stu-id="eb311-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb311-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb311-149">Minimum supported client</span></span><br/> | <span data-ttu-id="eb311-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb311-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb311-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb311-151">Minimum supported server</span></span><br/> | <span data-ttu-id="eb311-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb311-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb311-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb311-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb311-154"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb311-154"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb311-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="eb311-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb311-156"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb311-156"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="eb311-157">DLL</span><span class="sxs-lookup"><span data-stu-id="eb311-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb311-158"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb311-158"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb311-159">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="eb311-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="eb311-160">**DsRestorePrepareW** (Unicode) e **DsRestorePrepareA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="eb311-160">**DsRestorePrepareW** (Unicode) and **DsRestorePrepareA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="eb311-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb311-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb311-162">Ripristino di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="eb311-162">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="eb311-163">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="eb311-163">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> <dt>

[<span data-ttu-id="eb311-164">**DsRestoreGetDatabaseLocations**</span><span class="sxs-lookup"><span data-stu-id="eb311-164">**DsRestoreGetDatabaseLocations**</span></span>](dsrestoregetdatabaselocations.md)
</dt> <dt>

[<span data-ttu-id="eb311-165">**DsRestoreRegister**</span><span class="sxs-lookup"><span data-stu-id="eb311-165">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="eb311-166">**DsRestoreRegisterComplete**</span><span class="sxs-lookup"><span data-stu-id="eb311-166">**DsRestoreRegisterComplete**</span></span>](dsrestoreregistercomplete.md)
</dt> <dt>

[<span data-ttu-id="eb311-167">**DsRestoreEnd**</span><span class="sxs-lookup"><span data-stu-id="eb311-167">**DsRestoreEnd**</span></span>](dsrestoreend.md)
</dt> </dl>

 


---
title: Funzione DsBackupOpenFile (ntdsbcli. h)
description: Apre il file specificato ed esegue le operazioni client e server necessarie per preparare il file per il backup.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupOpenFile
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f9c4eac9c9825f510848583d7f707a2c244c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120022"
---
# <a name="dsbackupopenfile-function"></a><span data-ttu-id="64eff-104">DsBackupOpenFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="64eff-104">DsBackupOpenFile function</span></span>

<span data-ttu-id="64eff-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="64eff-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="64eff-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="64eff-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="64eff-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="64eff-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="64eff-108">La funzione **DsBackupOpenFile** apre il file specificato ed esegue le operazioni client e server necessarie per preparare il file per il backup.</span><span class="sxs-lookup"><span data-stu-id="64eff-108">The **DsBackupOpenFile** function opens the specified file and performs the client and server operations necessary to prepare the file for backup.</span></span>

## <a name="syntax"></a><span data-ttu-id="64eff-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64eff-109">Syntax</span></span>


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a><span data-ttu-id="64eff-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="64eff-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64eff-111">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64eff-111">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64eff-112">Contiene l'handle del contesto di backup ottenuto con la funzione [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="64eff-112">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="64eff-113">*szAttachmentName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64eff-113">*szAttachmentName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64eff-114">Puntatore a una stringa con terminazione null che specifica il nome del file di backup da aprire.</span><span class="sxs-lookup"><span data-stu-id="64eff-114">Pointer to a null-terminated string that specifies the name of the backup file to open.</span></span>

</dd> <dt>

<span data-ttu-id="64eff-115">*cbReadHintSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64eff-115">*cbReadHintSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64eff-116">Contiene le dimensioni possibili, in byte, del buffer passato come argomento *pvBuffer* nella funzione [**DsBackupRead**](dsbackupread.md) .</span><span class="sxs-lookup"><span data-stu-id="64eff-116">Contains the possible size, in bytes, of the buffer passed as the *pvBuffer* argument in the [**DsBackupRead**](dsbackupread.md) function.</span></span> <span data-ttu-id="64eff-117">Le funzioni di backup utilizzano questo valore come hint per ottimizzare il traffico di rete.</span><span class="sxs-lookup"><span data-stu-id="64eff-117">The backup functions use this value as a hint to optimize the network traffic.</span></span> <span data-ttu-id="64eff-118">Questo valore deve essere un multiplo di 8192 e deve essere maggiore o uguale a 24576.</span><span class="sxs-lookup"><span data-stu-id="64eff-118">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="64eff-119">*pliFileSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="64eff-119">*pliFileSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64eff-120">Puntatore a un **valore \_ Integer grande** che riceve le dimensioni, in byte, del file di backup aperto.</span><span class="sxs-lookup"><span data-stu-id="64eff-120">Pointer to a **LARGE\_INTEGER** value that receives the size, in bytes, of the backup file opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64eff-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64eff-121">Return value</span></span>

<span data-ttu-id="64eff-122">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="64eff-122">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="64eff-123">Nell'elenco seguente sono elencati altri possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="64eff-123">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="64eff-124">**ERRORE di \_ accesso \_ negato**</span><span class="sxs-lookup"><span data-stu-id="64eff-124">**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="64eff-125">Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="64eff-125">The caller does not have the proper access privileges to call this function.</span></span> <span data-ttu-id="64eff-126">La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="64eff-126">The [**DsSetAuthIdentity**](dssetauthidentity.md) function can be used to set the credentials to use for the backup and restore functions.</span></span>

</dd> <dt>

<span data-ttu-id="64eff-127">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="64eff-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="64eff-128">*HBC*, *szAttachmentName* o *pliFileSize* non sono validi.</span><span class="sxs-lookup"><span data-stu-id="64eff-128">*hbc*, *szAttachmentName*, or *pliFileSize* are invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64eff-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64eff-129">Requirements</span></span>



| <span data-ttu-id="64eff-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="64eff-130">Requirement</span></span> | <span data-ttu-id="64eff-131">Valore</span><span class="sxs-lookup"><span data-stu-id="64eff-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64eff-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64eff-132">Minimum supported client</span></span><br/> | <span data-ttu-id="64eff-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64eff-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64eff-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64eff-134">Minimum supported server</span></span><br/> | <span data-ttu-id="64eff-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64eff-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64eff-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64eff-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="64eff-137"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="64eff-137"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="64eff-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="64eff-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="64eff-139"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64eff-139"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="64eff-140">DLL</span><span class="sxs-lookup"><span data-stu-id="64eff-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64eff-141"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64eff-141"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="64eff-142">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="64eff-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="64eff-143">**DsBackupOpenFileW** (Unicode) e **DsBackupOpenFileA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="64eff-143">**DsBackupOpenFileW** (Unicode) and **DsBackupOpenFileA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="64eff-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64eff-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64eff-145">**DsBackupRead**</span><span class="sxs-lookup"><span data-stu-id="64eff-145">**DsBackupRead**</span></span>](dsbackupread.md)
</dt> <dt>

[<span data-ttu-id="64eff-146">Esecuzione del backup di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="64eff-146">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="64eff-147">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="64eff-147">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 


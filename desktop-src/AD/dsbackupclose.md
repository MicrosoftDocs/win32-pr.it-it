---
title: Funzione DsBackupClose (ntdsbcli. h)
description: Chiude un file di backup aperto con la funzione DsBackupOpenFile.
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupClose
topic_type:
- apiref
api_name:
- DsBackupClose
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d03c9cd7f125d223d264236a52120714d5198c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476360"
---
# <a name="dsbackupclose-function"></a><span data-ttu-id="03189-104">DsBackupClose (funzione)</span><span class="sxs-lookup"><span data-stu-id="03189-104">DsBackupClose function</span></span>

<span data-ttu-id="03189-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="03189-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="03189-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="03189-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="03189-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="03189-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="03189-108">La funzione **DsBackupClose** chiude un file di backup aperto con la funzione [**DsBackupOpenFile**](dsbackupopenfile.md) .</span><span class="sxs-lookup"><span data-stu-id="03189-108">The **DsBackupClose** function closes a backup file opened with the [**DsBackupOpenFile**](dsbackupopenfile.md) function.</span></span> <span data-ttu-id="03189-109">Per ogni handle di backup, è possibile aprire un solo file alla volta, quindi questa funzione chiude il file attualmente aperto.</span><span class="sxs-lookup"><span data-stu-id="03189-109">For each backup handle, only one file can be opened at a time, so this function closes the currently open file.</span></span>

## <a name="syntax"></a><span data-ttu-id="03189-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03189-110">Syntax</span></span>


```C++
HRESULT DsBackupClose(
  _In_ HBC hbc
);
```



## <a name="parameters"></a><span data-ttu-id="03189-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="03189-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03189-112">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03189-112">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03189-113">Contiene l'handle del contesto di backup ottenuto con la funzione [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="03189-113">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03189-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03189-114">Return value</span></span>

<span data-ttu-id="03189-115">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="03189-115">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="03189-116">Nell'elenco seguente sono elencati altri possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="03189-116">The following list lists other possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="03189-117">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="03189-117">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="03189-118">*HBC* non è valido.</span><span class="sxs-lookup"><span data-stu-id="03189-118">*hbc* is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="03189-119">**hrInvalidHandle**</span><span class="sxs-lookup"><span data-stu-id="03189-119">**hrInvalidHandle**</span></span>
</dt> <dd>

<span data-ttu-id="03189-120">Nessun file attualmente aperto.</span><span class="sxs-lookup"><span data-stu-id="03189-120">No file is currently open.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03189-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03189-121">Requirements</span></span>



| <span data-ttu-id="03189-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="03189-122">Requirement</span></span> | <span data-ttu-id="03189-123">Valore</span><span class="sxs-lookup"><span data-stu-id="03189-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03189-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03189-124">Minimum supported client</span></span><br/> | <span data-ttu-id="03189-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03189-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03189-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03189-126">Minimum supported server</span></span><br/> | <span data-ttu-id="03189-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03189-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03189-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03189-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="03189-129"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="03189-129"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="03189-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="03189-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="03189-131"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03189-131"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="03189-132">DLL</span><span class="sxs-lookup"><span data-stu-id="03189-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03189-133"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03189-133"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03189-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03189-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03189-135">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="03189-135">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="03189-136">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="03189-136">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="03189-137">Esecuzione del backup di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="03189-137">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="03189-138">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="03189-138">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 


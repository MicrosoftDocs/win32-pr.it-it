---
title: Funzione DsSetCurrentBackupLog (ntdsbcli. h)
description: Imposta il numero di log di backup corrente dopo un ripristino riuscito.
ms.assetid: 903bddea-c5a7-4b3f-819c-0467a9c5ae1b
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsSetCurrentBackupLog
topic_type:
- apiref
api_name:
- DsSetCurrentBackupLog
- DsSetCurrentBackupLogA
- DsSetCurrentBackupLogW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f50fc41317ae22ae89c47f63bb19f981563e5c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874057"
---
# <a name="dssetcurrentbackuplog-function"></a><span data-ttu-id="c4212-104">DsSetCurrentBackupLog (funzione)</span><span class="sxs-lookup"><span data-stu-id="c4212-104">DsSetCurrentBackupLog function</span></span>

<span data-ttu-id="c4212-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="c4212-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c4212-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="c4212-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c4212-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="c4212-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="c4212-108">La funzione **DsSetCurrentBackupLog** imposta il numero di log di backup corrente dopo un ripristino riuscito.</span><span class="sxs-lookup"><span data-stu-id="c4212-108">The **DsSetCurrentBackupLog** function sets the current backup log number after a successful restore.</span></span> <span data-ttu-id="c4212-109">Poiché Active Directory Domain Services supporta solo la registrazione circolare, questa funzione non viene in genere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4212-109">Because Active Directory Domain Services only support circular logging, this function is not normally used.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4212-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4212-110">Syntax</span></span>


```C++
HRESULT DsSetCurrentBackupLog(
  _In_ LPCWSTR szServerName,
  _In_ DWORD   dwCurrentLog
);
```



## <a name="parameters"></a><span data-ttu-id="c4212-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4212-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4212-112">*szServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4212-112">*szServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4212-113">Puntatore a una stringa con terminazione null che contiene il nome del server per il quale impostare il numero di log di backup.</span><span class="sxs-lookup"><span data-stu-id="c4212-113">Pointer to a null-terminated string that contains the name of the server to set the backup log number for.</span></span> <span data-ttu-id="c4212-114">Le barre rovesciate precedenti sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="c4212-114">Preceding backslashes are optional.</span></span> <span data-ttu-id="c4212-115">Il server deve essere lo stesso computer da cui viene chiamata la funzione.</span><span class="sxs-lookup"><span data-stu-id="c4212-115">The server must be the same computer that this function is called from.</span></span> <span data-ttu-id="c4212-116">Il nome del server non può contenere caratteri di sottolineatura ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="c4212-116">The server name cannot contain any underscore (\_) characters.</span></span> <span data-ttu-id="c4212-117">Un esempio di nome di server è " \\ \\ Server1".</span><span class="sxs-lookup"><span data-stu-id="c4212-117">An example of a server name is "\\\\server1".</span></span>

</dd> <dt>

<span data-ttu-id="c4212-118">*dwCurrentLog* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4212-118">*dwCurrentLog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4212-119">Contiene il numero di log di backup da impostare.</span><span class="sxs-lookup"><span data-stu-id="c4212-119">Contains the backup log number to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4212-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4212-120">Return value</span></span>

<span data-ttu-id="c4212-121">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c4212-121">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="c4212-122">Nell'elenco seguente sono elencati i possibili codici di errore.</span><span class="sxs-lookup"><span data-stu-id="c4212-122">The following list lists possible error codes.</span></span>

<dl> <dt>

<span data-ttu-id="c4212-123">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="c4212-123">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="c4212-124">Uno o più parametri non sono validi.</span><span class="sxs-lookup"><span data-stu-id="c4212-124">One or more parameters are invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c4212-125">**ERRORE \_ di \_ memoria insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="c4212-125">**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd>

<span data-ttu-id="c4212-126">Si è verificato un errore di allocazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="c4212-126">A memory allocation failure occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4212-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4212-127">Remarks</span></span>

<span data-ttu-id="c4212-128">In genere non è necessario chiamare la funzione **DsSetCurrentBackupLog** .</span><span class="sxs-lookup"><span data-stu-id="c4212-128">It is not normally required to call the **DsSetCurrentBackupLog** function.</span></span> <span data-ttu-id="c4212-129">Le funzioni di backup determinano e impostano automaticamente il backup dell'ultimo numero di log.</span><span class="sxs-lookup"><span data-stu-id="c4212-129">The backup functions automatically determine and set the last log number backed up.</span></span> <span data-ttu-id="c4212-130">Usare **DsSetCurrentBackupLog** per evitare che un altro backup incrementale riesca fino a quando non viene eseguito un backup completo.</span><span class="sxs-lookup"><span data-stu-id="c4212-130">Use **DsSetCurrentBackupLog** to prevent another incremental backup from succeeding until a full backup is performed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4212-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4212-131">Requirements</span></span>



| <span data-ttu-id="c4212-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4212-132">Requirement</span></span> | <span data-ttu-id="c4212-133">Valore</span><span class="sxs-lookup"><span data-stu-id="c4212-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4212-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4212-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c4212-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4212-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c4212-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4212-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c4212-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4212-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4212-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4212-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4212-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4212-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4212-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4212-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4212-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4212-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="c4212-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c4212-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4212-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4212-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4212-144">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c4212-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c4212-145">**DsSetCurrentBackupLogW** (Unicode) e **DsSetCurrentBackupLogA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c4212-145">**DsSetCurrentBackupLogW** (Unicode) and **DsSetCurrentBackupLogA** (ANSI)</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="c4212-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4212-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4212-147">Backup e ripristino di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="c4212-147">Backing Up and Restoring an Active Directory Server</span></span>](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="c4212-148">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="c4212-148">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 


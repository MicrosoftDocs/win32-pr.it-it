---
title: Funzione DsBackupRead (ntdsbcli. h)
description: Legge un blocco di dati dal file aperto corrente in un buffer.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupRead
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409c2a7d93503aad4edff88070c0458efc961d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964125"
---
# <a name="dsbackupread-function"></a><span data-ttu-id="da0e5-104">DsBackupRead (funzione)</span><span class="sxs-lookup"><span data-stu-id="da0e5-104">DsBackupRead function</span></span>

<span data-ttu-id="da0e5-105">\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="da0e5-105">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="da0e5-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="da0e5-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="da0e5-107">A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]</span><span class="sxs-lookup"><span data-stu-id="da0e5-107">Beginning with Windows Vista, use [Volume Shadow Copy Service (VSS)](../vss/volume-shadow-copy-service-overview.md) instead.\]</span></span>

<span data-ttu-id="da0e5-108">La funzione **DsBackupRead** legge un blocco di dati dal file aperto corrente in un buffer.</span><span class="sxs-lookup"><span data-stu-id="da0e5-108">The **DsBackupRead** function reads a block of data from the current open file, into a buffer.</span></span> <span data-ttu-id="da0e5-109">Si prevede che l'applicazione client chiami ripetutamente questa funzione fino a quando non viene ricevuto l'intero file di backup.</span><span class="sxs-lookup"><span data-stu-id="da0e5-109">The client application is expected to call this function repeatedly until the entire backup file has been received.</span></span> <span data-ttu-id="da0e5-110">La funzione [**DsBackupOpenFile**](dsbackupopenfile.md) fornisce l'intera dimensione del file di backup.</span><span class="sxs-lookup"><span data-stu-id="da0e5-110">The [**DsBackupOpenFile**](dsbackupopenfile.md) function provides the entire size of the backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="da0e5-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da0e5-111">Syntax</span></span>


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="da0e5-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="da0e5-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da0e5-113">*HBC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da0e5-113">*hbc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da0e5-114">Contiene l'handle del contesto di backup ottenuto con la funzione [**DsBackupPrepare**](dsbackupprepare.md) .</span><span class="sxs-lookup"><span data-stu-id="da0e5-114">Contains the backup context handle obtained with the [**DsBackupPrepare**](dsbackupprepare.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="da0e5-115">*pvBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da0e5-115">*pvBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da0e5-116">Puntatore a un buffer che riceve i dati.</span><span class="sxs-lookup"><span data-stu-id="da0e5-116">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="da0e5-117">Il buffer deve avere una dimensione di almeno *cbBuffer* byte.</span><span class="sxs-lookup"><span data-stu-id="da0e5-117">This buffer must be at least *cbBuffer* bytes in size.</span></span>

</dd> <dt>

<span data-ttu-id="da0e5-118">*cbBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da0e5-118">*cbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da0e5-119">Contiene la dimensione, in byte, del buffer in corrispondenza di *pvBuffer*.</span><span class="sxs-lookup"><span data-stu-id="da0e5-119">Contains the size, in bytes, of the buffer at *pvBuffer*.</span></span> <span data-ttu-id="da0e5-120">Questo valore deve essere un multiplo di 8192 e deve essere maggiore o uguale a 24576.</span><span class="sxs-lookup"><span data-stu-id="da0e5-120">This value must be a multiple of 8192 and must be greater than or equal to 24576.</span></span>

</dd> <dt>

<span data-ttu-id="da0e5-121">*pcbRead* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="da0e5-121">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da0e5-122">Puntatore a un valore **DWORD** che riceve il numero effettivo di byte letti.</span><span class="sxs-lookup"><span data-stu-id="da0e5-122">Pointer to a **DWORD** value that receives the actual number of bytes read.</span></span> <span data-ttu-id="da0e5-123">Può essere minore del numero di byte richiesti perché alcuni trasporti frammentano il buffer trasmesso invece di riempire l'intero buffer con i dati.</span><span class="sxs-lookup"><span data-stu-id="da0e5-123">This may be less than the number of bytes requested because some transports fragment the buffer being transmitted instead of filling the entire buffer with data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da0e5-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da0e5-124">Return value</span></span>

<span data-ttu-id="da0e5-125">Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="da0e5-125">Returns **S\_OK** if the function is successful or a Win32 or RPC error code otherwise.</span></span> <span data-ttu-id="da0e5-126">I codici di errore possibili includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="da0e5-126">Possible error codes include the following.</span></span>

<dl> <dt>

<span data-ttu-id="da0e5-127">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="da0e5-127">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="da0e5-128">Uno o più parametri non sono validi.</span><span class="sxs-lookup"><span data-stu-id="da0e5-128">One or more parameters are not valid.</span></span>

</dd> <dt>

<span data-ttu-id="da0e5-129">**HANDLE di errore \_ \_ EOF**</span><span class="sxs-lookup"><span data-stu-id="da0e5-129">**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd>

<span data-ttu-id="da0e5-130">È stata raggiunta la fine del file di backup.</span><span class="sxs-lookup"><span data-stu-id="da0e5-130">The end of the backup file was reached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da0e5-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da0e5-131">Requirements</span></span>



| <span data-ttu-id="da0e5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="da0e5-132">Requirement</span></span> | <span data-ttu-id="da0e5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="da0e5-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da0e5-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da0e5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="da0e5-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da0e5-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da0e5-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da0e5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="da0e5-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da0e5-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da0e5-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da0e5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="da0e5-139"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="da0e5-139"><dt>Ntdsbcli.h</dt></span></span> </dl>   |
| <span data-ttu-id="da0e5-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="da0e5-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="da0e5-141"><dt>Ntdsbcli. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da0e5-141"><dt>Ntdsbcli.lib</dt></span></span> </dl> |
| <span data-ttu-id="da0e5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="da0e5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da0e5-143"><dt>Ntdsbcli.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da0e5-143"><dt>Ntdsbcli.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da0e5-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da0e5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0e5-145">**DsBackupOpenFile**</span><span class="sxs-lookup"><span data-stu-id="da0e5-145">**DsBackupOpenFile**</span></span>](dsbackupopenfile.md)
</dt> <dt>

[<span data-ttu-id="da0e5-146">**DsBackupPrepare**</span><span class="sxs-lookup"><span data-stu-id="da0e5-146">**DsBackupPrepare**</span></span>](dsbackupprepare.md)
</dt> <dt>

[<span data-ttu-id="da0e5-147">**DsBackupFree**</span><span class="sxs-lookup"><span data-stu-id="da0e5-147">**DsBackupFree**</span></span>](dsbackupfree.md)
</dt> <dt>

[<span data-ttu-id="da0e5-148">Esecuzione del backup di un server di Active Directory</span><span class="sxs-lookup"><span data-stu-id="da0e5-148">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
</dt> <dt>

[<span data-ttu-id="da0e5-149">Funzioni di backup della directory</span><span class="sxs-lookup"><span data-stu-id="da0e5-149">Directory Backup Functions</span></span>](directory-backup-functions.md)
</dt> </dl>

 


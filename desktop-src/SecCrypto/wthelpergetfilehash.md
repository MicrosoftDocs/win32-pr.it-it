---
description: Verifica la firma di un file firmato e ottiene il valore hash e l'identificatore dell'algoritmo per il file.
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: WTHelperGetFileHash (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperGetFileHash
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 1597dfda630b1ae8cbc0d3b700b6ed9bc1a09472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967615"
---
# <a name="wthelpergetfilehash-function"></a><span data-ttu-id="2aab2-103">WTHelperGetFileHash (funzione)</span><span class="sxs-lookup"><span data-stu-id="2aab2-103">WTHelperGetFileHash function</span></span>

<span data-ttu-id="2aab2-104">\[La funzione **WTHelperGetFileHash** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="2aab2-104">\[The **WTHelperGetFileHash** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2aab2-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="2aab2-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="2aab2-106">La funzione **WTHelperGetFileHash** verifica la firma di un file firmato e ottiene il valore hash e l'identificatore dell'algoritmo per il file.</span><span class="sxs-lookup"><span data-stu-id="2aab2-106">The **WTHelperGetFileHash** function verifies the signature of a signed file and obtains the hash value and algorithm identifier for the file.</span></span>

> [!Note]  
> <span data-ttu-id="2aab2-107">Questa funzione non è dichiarata in un file di intestazione pubblicato.</span><span class="sxs-lookup"><span data-stu-id="2aab2-107">This function is not declared in a published header file.</span></span> <span data-ttu-id="2aab2-108">Per usare questa funzione, dichiararla nel formato esatto indicato.</span><span class="sxs-lookup"><span data-stu-id="2aab2-108">To use this function, declare it in the exact format shown.</span></span> <span data-ttu-id="2aab2-109">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="2aab2-109">This function also has no associated import library.</span></span> <span data-ttu-id="2aab2-110">È necessario utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Wintrust.dll.</span><span class="sxs-lookup"><span data-stu-id="2aab2-110">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2aab2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2aab2-111">Syntax</span></span>


```C++
LONG WINAPI WTHelperGetFileHash(
  _In_        LPCWSTR pwszFilename,
  _In_        DWORD   dwFlags,
  _Inout_opt_ PVOID   pvReserved,
  _Out_opt_   BYTE    *pbFileHash,
  _Inout_opt_ DWORD   *pcbFileHash,
  _Out_opt_   ALG_ID  *pHashAlgid
);
```



## <a name="parameters"></a><span data-ttu-id="2aab2-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="2aab2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aab2-113">*pwszFilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aab2-113">*pwszFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab2-114">Puntatore a una stringa Unicode con terminazione null che contiene il percorso e il nome file del file per il quale ottenere l'hash.</span><span class="sxs-lookup"><span data-stu-id="2aab2-114">A pointer to a null-terminated Unicode string that contains the path and file name of the file to get the hash for.</span></span>

</dd> <dt>

<span data-ttu-id="2aab2-115">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aab2-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab2-116">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2aab2-116">This parameter is not used and should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2aab2-117">*pvReserved* \[ in, out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2aab2-117">*pvReserved* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab2-118">Questo parametro non viene utilizzato e deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="2aab2-118">This parameter is not used and should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2aab2-119">*pbFileHash* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2aab2-119">*pbFileHash* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab2-120">Puntatore a un buffer per ricevere il valore hash per il file.</span><span class="sxs-lookup"><span data-stu-id="2aab2-120">A pointer to a buffer to receive the hash value for the file.</span></span> <span data-ttu-id="2aab2-121">Il parametro *pcbFileHash* contiene la dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="2aab2-121">The *pcbFileHash* parameter contains the size of this buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2aab2-122">*pcbFileHash* \[ in, out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2aab2-122">*pcbFileHash* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab2-123">Puntatore a una variabile **DWORD** che, in input, contiene la dimensione, in byte, del buffer *pbFileHash* e, in output, riceve la dimensione, in byte, del valore hash.</span><span class="sxs-lookup"><span data-stu-id="2aab2-123">A pointer to a **DWORD** variable that, on input, contains the size, in bytes, of the *pbFileHash* buffer and, on output, receives the size, in bytes, of the hash value.</span></span>

<span data-ttu-id="2aab2-124">Per ottenere le dimensioni richieste del valore hash, passare **null** per il parametro *pbFileHash* .</span><span class="sxs-lookup"><span data-stu-id="2aab2-124">To obtain the required size of the hash value, pass **NULL** for the *pbFileHash* parameter.</span></span> <span data-ttu-id="2aab2-125">Questa funzione inserisce la dimensione richiesta, in byte, del valore hash in questa posizione.</span><span class="sxs-lookup"><span data-stu-id="2aab2-125">This function will place the required size, in bytes, of the hash value in this location.</span></span>

<span data-ttu-id="2aab2-126">Se il parametro *pbFileHash* non è **null** e la dimensione non è sufficiente per ricevere il valore hash, questa funzione inserisce la dimensione richiesta, in byte, in questo percorso e restituisce un errore di **\_ altri \_ dati**.</span><span class="sxs-lookup"><span data-stu-id="2aab2-126">If the *pbFileHash* parameter is not **NULL**, and the size is not large enough to receive the hash value, this function will place the required size, in bytes, in this location and return **ERROR\_MORE\_DATA**.</span></span>

</dd> <dt>

<span data-ttu-id="2aab2-127">*pHashAlgid* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2aab2-127">*pHashAlgid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2aab2-128">Puntatore a una variabile [**\_ ID ALG**](alg-id.md) per ricevere l'identificatore dell'algoritmo utilizzato per creare il valore hash.</span><span class="sxs-lookup"><span data-stu-id="2aab2-128">A pointer to an [**ALG\_ID**](alg-id.md) variable to receive the identifier of the algorithm used to create the hash value.</span></span> <span data-ttu-id="2aab2-129">Questo parametro può essere **null** se queste informazioni non sono necessarie.</span><span class="sxs-lookup"><span data-stu-id="2aab2-129">This parameter can be **NULL** if this information is not needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aab2-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2aab2-130">Return value</span></span>

<span data-ttu-id="2aab2-131">Restituisce un codice di stato che indica l'esito positivo o negativo della funzione.</span><span class="sxs-lookup"><span data-stu-id="2aab2-131">Returns a status code that indicates the success or failure of the function.</span></span>

<span data-ttu-id="2aab2-132">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="2aab2-132">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="2aab2-133">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2aab2-133">Return code</span></span>                                                                                               | <span data-ttu-id="2aab2-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2aab2-134">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2aab2-135"><dt>**ERRORE \_ riuscito**</dt></span><span class="sxs-lookup"><span data-stu-id="2aab2-135"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>             | <span data-ttu-id="2aab2-136">Il file è firmato e la firma è stata verificata.</span><span class="sxs-lookup"><span data-stu-id="2aab2-136">The file is signed, and the signature was verified.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="2aab2-137"><dt>**ERRORE di \_ più \_ dati**</dt></span><span class="sxs-lookup"><span data-stu-id="2aab2-137"><dt>**ERROR\_MORE\_DATA**</dt></span></span> </dl>          | <span data-ttu-id="2aab2-138">Il parametro *pbFileHash* non è **null** e le dimensioni specificate dal parametro *pcbFileHash* non sono sufficientemente grandi per la ricezione dell'hash.</span><span class="sxs-lookup"><span data-stu-id="2aab2-138">The *pbFileHash* parameter is not **NULL**, and the size specified by the *pcbFileHash* parameter is not large enough to receive the hash.</span></span><br/> |
| <dl> <span data-ttu-id="2aab2-139"><dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2aab2-139"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="2aab2-140">Si è verificato un errore di allocazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="2aab2-140">A memory allocation failure occurred.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="2aab2-141"><dt>**TRUST \_ E \_ digest non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2aab2-141"><dt>**TRUST\_E\_BAD\_DIGEST**</dt></span></span> </dl>      | <span data-ttu-id="2aab2-142">La firma del file non è stata verificata.</span><span class="sxs-lookup"><span data-stu-id="2aab2-142">The signature of the file was not verified.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="2aab2-143"><dt>**TRUST \_ E \_ NoSignature**</dt></span><span class="sxs-lookup"><span data-stu-id="2aab2-143"><dt>**TRUST\_E\_NOSIGNATURE**</dt></span></span> </dl>      | <span data-ttu-id="2aab2-144">Il file non è stato firmato o non ha una firma valida.</span><span class="sxs-lookup"><span data-stu-id="2aab2-144">The file was not signed or had a signature that is not valid.</span></span><br/>                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="2aab2-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2aab2-145">Requirements</span></span>



| <span data-ttu-id="2aab2-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="2aab2-146">Requirement</span></span> | <span data-ttu-id="2aab2-147">Valore</span><span class="sxs-lookup"><span data-stu-id="2aab2-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2aab2-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2aab2-148">Minimum supported client</span></span><br/> | <span data-ttu-id="2aab2-149">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2aab2-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2aab2-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2aab2-150">Minimum supported server</span></span><br/> | <span data-ttu-id="2aab2-151">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2aab2-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2aab2-152">DLL</span><span class="sxs-lookup"><span data-stu-id="2aab2-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2aab2-153"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2aab2-153"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 

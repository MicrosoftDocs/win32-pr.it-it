---
description: Timestamp l'oggetto specificato e, facoltativamente, restituisce un puntatore a una struttura del contesto del FIRMATARIo \_ che contiene un puntatore a un BLOB.
ms.assetid: f3a910f6-64f8-4cf5-b008-2a16872f9a98
title: SignerTimeStampEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a4562ca84f8b3376a22d00a5e9501947152ed875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758771"
---
# <a name="signertimestampex-function"></a><span data-ttu-id="87f53-103">SignerTimeStampEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="87f53-103">SignerTimeStampEx function</span></span>

<span data-ttu-id="87f53-104">Il timestamp della funzione **SignerTimeStampEx** indica l'oggetto specificato e, facoltativamente, restituisce un puntatore a una struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene un puntatore a un [*BLOB*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="87f53-104">The **SignerTimeStampEx** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="87f53-105">Questa funzione supporta l'indicatore di data e ora Authenticode.</span><span class="sxs-lookup"><span data-stu-id="87f53-105">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="87f53-106">Per eseguire il timestamp dell'infrastruttura a chiave pubblica (RFC 3161) X. 509, usare la funzione [**SignerTimeStampEx2**](signertimestampex2.md) .</span><span class="sxs-lookup"><span data-stu-id="87f53-106">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="87f53-107">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="87f53-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="87f53-108">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="87f53-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="87f53-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87f53-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="87f53-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="87f53-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87f53-111">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87f53-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f53-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="87f53-112">Reserved.</span></span> <span data-ttu-id="87f53-113">Questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="87f53-113">This parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="87f53-114">*pSubjectInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87f53-114">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f53-115">Indirizzo di una struttura di [**\_ \_ informazioni sul soggetto del firmatario**](signer-subject-info.md) che rappresenta l'oggetto di cui è stato indicato il timestamp.</span><span class="sxs-lookup"><span data-stu-id="87f53-115">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="87f53-116">*pwszHttpTimeStamp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87f53-116">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f53-117">Indirizzo di una stringa Unicode con terminazione null che contiene l'URL di un server di timestamp.</span><span class="sxs-lookup"><span data-stu-id="87f53-117">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="87f53-118">*psRequest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87f53-118">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f53-119">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="87f53-119">Optional.</span></span> <span data-ttu-id="87f53-120">Indirizzo di una struttura [**degli \_ attributi Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) che contiene attributi aggiuntivi aggiunti alla richiesta del timestamp.</span><span class="sxs-lookup"><span data-stu-id="87f53-120">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="87f53-121">Questo parametro è facoltativo e può essere **null** se non è incluso.</span><span class="sxs-lookup"><span data-stu-id="87f53-121">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="87f53-122">*pSipData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87f53-122">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f53-123">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="87f53-123">Optional.</span></span> <span data-ttu-id="87f53-124">Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP ( [*Subject Interface Package*](../secgloss/s-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="87f53-124">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="87f53-125">Il formato e il contenuto di questo parametro sono definiti dal provider SIP.</span><span class="sxs-lookup"><span data-stu-id="87f53-125">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="87f53-126">Questo parametro è facoltativo e può essere **null** se non è incluso.</span><span class="sxs-lookup"><span data-stu-id="87f53-126">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="87f53-127">*ppSignerContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="87f53-127">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87f53-128">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="87f53-128">Optional.</span></span> <span data-ttu-id="87f53-129">Indirizzo di un puntatore alla struttura del [**\_ contesto del firmatario**](signer-context.md) che contiene il BLOB firmato.</span><span class="sxs-lookup"><span data-stu-id="87f53-129">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="87f53-130">Al termine dell'uso della struttura del **\_ contesto del firmatario** , liberarla chiamando la funzione [**SignerFreeSignerContext**](signerfreesignercontext.md) .</span><span class="sxs-lookup"><span data-stu-id="87f53-130">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87f53-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87f53-131">Return value</span></span>

<span data-ttu-id="87f53-132">Se la funzione ha esito positivo, la funzione restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="87f53-132">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="87f53-133">Se la funzione ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="87f53-133">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="87f53-134">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="87f53-134">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87f53-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87f53-135">Requirements</span></span>



| <span data-ttu-id="87f53-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="87f53-136">Requirement</span></span> | <span data-ttu-id="87f53-137">Valore</span><span class="sxs-lookup"><span data-stu-id="87f53-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87f53-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87f53-138">Minimum supported client</span></span><br/> | <span data-ttu-id="87f53-139">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="87f53-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="87f53-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87f53-140">Minimum supported server</span></span><br/> | <span data-ttu-id="87f53-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="87f53-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="87f53-142">DLL</span><span class="sxs-lookup"><span data-stu-id="87f53-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87f53-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87f53-143"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87f53-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87f53-144">See also</span></span>

<dl> <span data-ttu-id="87f53-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="87f53-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="87f53-146">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="87f53-146">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> </dl>

 

 

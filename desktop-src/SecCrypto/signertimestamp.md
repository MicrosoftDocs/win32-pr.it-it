---
description: Timestamp dell'oggetto specificato. Questa funzione supporta l'indicatore di data e ora Authenticode. Per eseguire il timestamp dell'infrastruttura a chiave pubblica (RFC 3161) X. 509, usare la funzione SignerTimeStampEx2.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: SignerTimeStamp (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c4c57f231f70477a76b4d4f6156354ebc847a715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968205"
---
# <a name="signertimestamp-function"></a><span data-ttu-id="6e08f-105">SignerTimeStamp (funzione)</span><span class="sxs-lookup"><span data-stu-id="6e08f-105">SignerTimeStamp function</span></span>

<span data-ttu-id="6e08f-106">Il timestamp della funzione **SignerTimeStamp** contrassegna l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="6e08f-106">The **SignerTimeStamp** function time stamps the specified subject.</span></span> <span data-ttu-id="6e08f-107">Questa funzione supporta l'indicatore di data e ora Authenticode.</span><span class="sxs-lookup"><span data-stu-id="6e08f-107">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="6e08f-108">Per eseguire il timestamp dell'infrastruttura a chiave pubblica (RFC 3161) X. 509, usare la funzione [**SignerTimeStampEx2**](signertimestampex2.md) .</span><span class="sxs-lookup"><span data-stu-id="6e08f-108">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="6e08f-109">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="6e08f-109">This function has no associated header file or import library.</span></span> <span data-ttu-id="6e08f-110">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="6e08f-110">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6e08f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e08f-111">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="6e08f-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e08f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e08f-113">*pSubjectInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e08f-113">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e08f-114">Indirizzo di una struttura di [**\_ \_ informazioni sul soggetto del firmatario**](signer-subject-info.md) che rappresenta l'oggetto di cui è stato indicato il timestamp.</span><span class="sxs-lookup"><span data-stu-id="6e08f-114">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="6e08f-115">*pwszHttpTimeStamp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e08f-115">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e08f-116">Indirizzo di una stringa Unicode con terminazione null che contiene l'URL di un server di timestamp.</span><span class="sxs-lookup"><span data-stu-id="6e08f-116">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="6e08f-117">*psRequest* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6e08f-117">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6e08f-118">Indirizzo di una struttura [**degli \_ attributi Crypt**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) che contiene attributi aggiuntivi aggiunti alla richiesta del timestamp.</span><span class="sxs-lookup"><span data-stu-id="6e08f-118">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="6e08f-119">Questo parametro è facoltativo e può essere **null** se non è incluso.</span><span class="sxs-lookup"><span data-stu-id="6e08f-119">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="6e08f-120">*pSipData* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6e08f-120">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6e08f-121">Valore a 32 bit passato come dati aggiuntivi alle funzioni SIP.</span><span class="sxs-lookup"><span data-stu-id="6e08f-121">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="6e08f-122">Il formato e il contenuto di questo oggetto sono definiti dal provider SIP.</span><span class="sxs-lookup"><span data-stu-id="6e08f-122">The format and content of this is defined by the SIP provider.</span></span>

<span data-ttu-id="6e08f-123">Questo parametro è facoltativo e può essere **null** se non è incluso.</span><span class="sxs-lookup"><span data-stu-id="6e08f-123">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e08f-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e08f-124">Return value</span></span>

<span data-ttu-id="6e08f-125">Se la funzione ha esito positivo, la funzione restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6e08f-125">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="6e08f-126">Se la funzione ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="6e08f-126">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="6e08f-127">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="6e08f-127">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e08f-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e08f-128">Requirements</span></span>



| <span data-ttu-id="6e08f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e08f-129">Requirement</span></span> | <span data-ttu-id="6e08f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="6e08f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e08f-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e08f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6e08f-132">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6e08f-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6e08f-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e08f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6e08f-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e08f-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e08f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6e08f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e08f-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e08f-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 

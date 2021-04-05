---
description: Ottiene un handle per un provider del servizio di crittografia (CSP) in base a un file di chiave privata o a un nome del contenitore di chiavi.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: PvkGetCryptProv (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkGetCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 026b31d021dc6ff2569ad9ce8f17d2e7f0d17b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885645"
---
# <a name="pvkgetcryptprov-function"></a><span data-ttu-id="bad74-103">PvkGetCryptProv (funzione)</span><span class="sxs-lookup"><span data-stu-id="bad74-103">PvkGetCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bad74-104">Questa API è deprecata.</span><span class="sxs-lookup"><span data-stu-id="bad74-104">This API is deprecated.</span></span> <span data-ttu-id="bad74-105">Microsoft può rimuovere questa API nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="bad74-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="bad74-106">La funzione **PvkGetCryptProv** ottiene un handle per un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) in base a un file di [*chiave privata*](../secgloss/p-gly.md) o a un nome del contenitore di chiavi.</span><span class="sxs-lookup"><span data-stu-id="bad74-106">The **PvkGetCryptProv** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) based on either a [*private key*](../secgloss/p-gly.md) file or a key container name.</span></span>

> [!Note]  
> <span data-ttu-id="bad74-107">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="bad74-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="bad74-108">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="bad74-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bad74-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bad74-109">Syntax</span></span>


```C++
HRESULT WINAPI PvkGetCryptProv(
  _In_      HWND       hwnd,
  _In_      LPCWSTR    pwszCaption,
  _In_      LPCWSTR    pwszCapiProvider,
  _In_      DWORD      dwProviderType,
  _In_      LPCWSTR    pwszPvkFile,
  _In_      LPCWSTR    pwszKeyContainerName,
  _Out_     DWORD      *pdwKeySpec,
  _Out_opt_ LPWSTR     *ppwszTmpContainer,
  _Out_     HCRYPTPROV *phCryptProv
);
```



## <a name="parameters"></a><span data-ttu-id="bad74-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="bad74-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bad74-111">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bad74-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bad74-112">Se è necessaria una password per decrittografare il file di chiave privata, questo parametro è un handle per l'elemento padre della finestra di dialogo password; in caso contrario, è **null**.</span><span class="sxs-lookup"><span data-stu-id="bad74-112">If a password is required to decrypt the private key file, this parameter is a handle to the parent of the password dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bad74-113">*pwszCaption* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bad74-113">*pwszCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bad74-114">Puntatore a una stringa con terminazione null per la didascalia della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="bad74-114">A pointer to a null-terminated string for the dialog box caption.</span></span>

</dd> <dt>

<span data-ttu-id="bad74-115">*pwszCapiProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bad74-115">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bad74-116">Puntatore a una stringa con terminazione null per il nome CSP.</span><span class="sxs-lookup"><span data-stu-id="bad74-116">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="bad74-117">*dwProviderType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bad74-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bad74-118">Valore **DWORD** che rappresenta il tipo di provider di crittografia.</span><span class="sxs-lookup"><span data-stu-id="bad74-118">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="bad74-119">Per ulteriori informazioni, vedere [tipi di provider di crittografia](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="bad74-119">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="bad74-120">*pwszPvkFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bad74-120">*pwszPvkFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bad74-121">Puntatore a una stringa con terminazione null che contiene il nome di un file di chiave privata.</span><span class="sxs-lookup"><span data-stu-id="bad74-121">A pointer to a null-terminated string that contains the name of a private key file.</span></span>

</dd> <dt>

<span data-ttu-id="bad74-122">*pwszKeyContainerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bad74-122">*pwszKeyContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bad74-123">Puntatore a una stringa con terminazione null per il nome del contenitore di chiavi private.</span><span class="sxs-lookup"><span data-stu-id="bad74-123">A pointer to a null-terminated string for the private key container name.</span></span>

</dd> <dt>

<span data-ttu-id="bad74-124">*pdwKeySpec* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bad74-124">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bad74-125">Puntatore a un valore **DWORD** per il tipo di chiave del contenitore restituito con *phCryptProv* e *ppwszTmpContainer*.</span><span class="sxs-lookup"><span data-stu-id="bad74-125">A pointer to a **DWORD** value for the type of key of the container returned with *phCryptProv* and *ppwszTmpContainer*.</span></span>

</dd> <dt>

<span data-ttu-id="bad74-126">*ppwszTmpContainer* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bad74-126">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bad74-127">Indirizzo di un puntatore a una stringa con terminazione null per il nome del contenitore di chiavi temporaneo.</span><span class="sxs-lookup"><span data-stu-id="bad74-127">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="bad74-128">La funzione **PvkGetCryptProv** fornisce e inizializza il contenitore temporaneo.</span><span class="sxs-lookup"><span data-stu-id="bad74-128">The **PvkGetCryptProv** function provides and initializes the temporary container.</span></span> <span data-ttu-id="bad74-129">Quando si chiama **PvkGetCryptProv**, l'indirizzo deve puntare a un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="bad74-129">When calling **PvkGetCryptProv**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="bad74-130">*phCryptProv* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bad74-130">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bad74-131">Puntatore a un handle per il CSP.</span><span class="sxs-lookup"><span data-stu-id="bad74-131">A pointer to a handle for the CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bad74-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bad74-132">Return value</span></span>

<span data-ttu-id="bad74-133">Se il metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bad74-133">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="bad74-134">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="bad74-134">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="bad74-135">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="bad74-135">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bad74-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="bad74-136">Remarks</span></span>

<span data-ttu-id="bad74-137">La funzione **PvkGetCryptProv** tenta prima di tutto di ottenere l'handle del provider dal nome del contenitore di chiavi specificato dal parametro *pwszKeyContainerName* .</span><span class="sxs-lookup"><span data-stu-id="bad74-137">The **PvkGetCryptProv** function first tries to get the provider handle from the key container name specified by the *pwszKeyContainerName* parameter.</span></span> <span data-ttu-id="bad74-138">Se si passa **null** per il parametro *pwszKeyContainerName* , **PvkGetCryptProv** tenta di ottenere il provider dal file di chiave privata specificato nel parametro *pwszPvkFile* .</span><span class="sxs-lookup"><span data-stu-id="bad74-138">If you pass **NULL** for the *pwszKeyContainerName* parameter, **PvkGetCryptProv** tries to get the provider from the private key file specified in the *pwszPvkFile* parameter.</span></span>

<span data-ttu-id="bad74-139">Al termine dell'utilizzo del CSP, liberare l'handle del provider e il contenitore di chiavi temporaneo chiamando la funzione [**PvkFreeCryptProv**](pvkfreecryptprov.md) .</span><span class="sxs-lookup"><span data-stu-id="bad74-139">When you have finished using the CSP, free the provider handle and temporary key container by calling the [**PvkFreeCryptProv**](pvkfreecryptprov.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bad74-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bad74-140">Requirements</span></span>



| <span data-ttu-id="bad74-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bad74-141">Requirement</span></span> | <span data-ttu-id="bad74-142">Valore</span><span class="sxs-lookup"><span data-stu-id="bad74-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bad74-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bad74-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bad74-144">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bad74-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bad74-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bad74-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bad74-146">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bad74-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bad74-147">DLL</span><span class="sxs-lookup"><span data-stu-id="bad74-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bad74-148"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bad74-148"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 

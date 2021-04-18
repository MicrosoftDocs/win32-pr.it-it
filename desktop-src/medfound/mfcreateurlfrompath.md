---
description: Converte un percorso Microsoft MS-DOS in un URL canonico.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: MFCreateURLFromPath (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: e43c2d7df299792d8b5be99226e9cfdbd11976a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308411"
---
# <a name="mfcreateurlfrompath-function"></a><span data-ttu-id="ace95-103">MFCreateURLFromPath (funzione)</span><span class="sxs-lookup"><span data-stu-id="ace95-103">MFCreateURLFromPath function</span></span>

<span data-ttu-id="ace95-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="ace95-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="ace95-105">Al contrario, le applicazioni devono chiamare [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]</span><span class="sxs-lookup"><span data-stu-id="ace95-105">Instead, Applications should call [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]</span></span>

<span data-ttu-id="ace95-106">Converte un percorso Microsoft MS-DOS in un URL canonico.</span><span class="sxs-lookup"><span data-stu-id="ace95-106">Converts a Microsoft MS-DOS path to a canonicalized URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace95-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ace95-107">Syntax</span></span>


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a><span data-ttu-id="ace95-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ace95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace95-109">*pwszFilePath* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ace95-109">*pwszFilePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ace95-110">Stringa con terminazione null che contiene il percorso.</span><span class="sxs-lookup"><span data-stu-id="ace95-110">A null-terminated string that contains the path.</span></span> <span data-ttu-id="ace95-111">La lunghezza massima della stringa è la **\_ \_ \_ lunghezza URL Internet Max**.</span><span class="sxs-lookup"><span data-stu-id="ace95-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="ace95-112">*ppwszFileURL* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ace95-112">*ppwszFileURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ace95-113">Riceve una stringa con terminazione null che contiene l'URL.</span><span class="sxs-lookup"><span data-stu-id="ace95-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="ace95-114">Il chiamante deve liberare la stringa chiamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="ace95-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace95-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ace95-115">Return value</span></span>

<span data-ttu-id="ace95-116">La funzione restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ace95-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="ace95-117">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ace95-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ace95-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ace95-118">Return code</span></span>                                                                             | <span data-ttu-id="ace95-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ace95-119">Description</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ace95-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ace95-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ace95-121">La stringa specificata nel parametro *pwszFilePath* è già in formato URL.</span><span class="sxs-lookup"><span data-stu-id="ace95-121">The string given in the *pwszFilePath* parameter is already in URL format.</span></span> <span data-ttu-id="ace95-122">In questo caso, *pszFilePath* viene semplicemente copiato in *ppszFileURL* senza modifiche.</span><span class="sxs-lookup"><span data-stu-id="ace95-122">In this case, *pszFilePath* is simply copied to *ppszFileURL* without modification.</span></span><br/> |
| <dl> <span data-ttu-id="ace95-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ace95-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ace95-124">Funzione completata.</span><span class="sxs-lookup"><span data-stu-id="ace95-124">The function succeeded.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="ace95-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ace95-125">Remarks</span></span>

<span data-ttu-id="ace95-126">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="ace95-126">This function has no associated import library.</span></span> <span data-ttu-id="ace95-127">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Mfplat.dll.</span><span class="sxs-lookup"><span data-stu-id="ace95-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ace95-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ace95-128">Requirements</span></span>



| <span data-ttu-id="ace95-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ace95-129">Requirement</span></span> | <span data-ttu-id="ace95-130">Valore</span><span class="sxs-lookup"><span data-stu-id="ace95-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ace95-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ace95-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ace95-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ace95-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ace95-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ace95-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ace95-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ace95-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ace95-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ace95-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ace95-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ace95-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ace95-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ace95-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace95-138">Funzioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ace95-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 

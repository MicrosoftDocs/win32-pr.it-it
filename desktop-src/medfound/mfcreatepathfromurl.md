---
description: Converte un URL di file in un percorso Microsoft MS-DOS.
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: MFCreatePathFromURL (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreatePathFromURL
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: c1838a3b09dc5375588d562aa503d555a186e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308410"
---
# <a name="mfcreatepathfromurl-function"></a><span data-ttu-id="f128f-103">MFCreatePathFromURL (funzione)</span><span class="sxs-lookup"><span data-stu-id="f128f-103">MFCreatePathFromURL function</span></span>

<span data-ttu-id="f128f-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="f128f-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="f128f-105">Al contrario, le applicazioni devono chiamare [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]</span><span class="sxs-lookup"><span data-stu-id="f128f-105">Instead, applications should call [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]</span></span>

<span data-ttu-id="f128f-106">Converte un URL di file in un percorso Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="f128f-106">Converts a file URL to a Microsoft MS-DOS path.</span></span>

## <a name="syntax"></a><span data-ttu-id="f128f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f128f-107">Syntax</span></span>


```C++
HRESULT MFCreatePathFromURL(
  _In_opt_ LPCWSTR pwszFileURL,
  _Out_    LPWSTR  *ppwszFilePath
);
```



## <a name="parameters"></a><span data-ttu-id="f128f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f128f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f128f-109">*pwszFileURL* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f128f-109">*pwszFileURL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f128f-110">Stringa con terminazione null che contiene l'URL.</span><span class="sxs-lookup"><span data-stu-id="f128f-110">A null-terminated string that contains the URL.</span></span> <span data-ttu-id="f128f-111">La lunghezza massima della stringa è la **\_ \_ \_ lunghezza URL Internet Max**.</span><span class="sxs-lookup"><span data-stu-id="f128f-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="f128f-112">*ppwszFilePath* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f128f-112">*ppwszFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f128f-113">Riceve una stringa con terminazione null che contiene l'URL.</span><span class="sxs-lookup"><span data-stu-id="f128f-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="f128f-114">Il chiamante deve liberare la stringa chiamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="f128f-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f128f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f128f-115">Return value</span></span>

<span data-ttu-id="f128f-116">La funzione restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f128f-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="f128f-117">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f128f-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f128f-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f128f-118">Return code</span></span>                                                                                  | <span data-ttu-id="f128f-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f128f-119">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f128f-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f128f-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f128f-121">Funzione completata.</span><span class="sxs-lookup"><span data-stu-id="f128f-121">The function succeeded.</span></span> <br/>                                                                         |
| <dl> <span data-ttu-id="f128f-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f128f-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f128f-123">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="f128f-123">Invalid argument.</span></span> <span data-ttu-id="f128f-124">La stringa specificata nel parametro *pwszFileURL* non può essere convertita in un percorso.</span><span class="sxs-lookup"><span data-stu-id="f128f-124">The string given in the *pwszFileURL* parameter cannot be converted to a path.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f128f-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="f128f-125">Remarks</span></span>

<span data-ttu-id="f128f-126">A questa funzione non è associata alcuna libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="f128f-126">This function has no associated import library.</span></span> <span data-ttu-id="f128f-127">Per chiamare questa funzione, è necessario usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire il collegamento dinamico a Mfplat.dll.</span><span class="sxs-lookup"><span data-stu-id="f128f-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="f128f-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f128f-128">Requirements</span></span>



| <span data-ttu-id="f128f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f128f-129">Requirement</span></span> | <span data-ttu-id="f128f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f128f-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f128f-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f128f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f128f-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f128f-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f128f-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f128f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f128f-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f128f-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f128f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f128f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f128f-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f128f-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f128f-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f128f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f128f-138">Funzioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f128f-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 

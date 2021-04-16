---
title: Funzione TF_InvalidAssemblyListCacheIfExist
description: La \_ funzione TF InvalidAssemblyListCacheIfExist invalida la cache di descrizione del processore di input del testo.
ms.assetid: a0f61b25-598c-417c-8679-7523c041f9ef
keywords:
- Framework servizi di testo TF_InvalidAssemblyListCacheIfExist funzione
topic_type:
- apiref
api_name:
- TF_InvalidAssemblyListCacheIfExist
api_location:
- msctf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dd28ab2247fae28af1c5f322832aebe071fab4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517571"
---
# <a name="tf_invalidassemblylistcacheifexist-function"></a><span data-ttu-id="63492-104">\_Funzione TF InvalidAssemblyListCacheIfExist</span><span class="sxs-lookup"><span data-stu-id="63492-104">TF\_InvalidAssemblyListCacheIfExist function</span></span>

<span data-ttu-id="63492-105">La funzione **tf \_ InvalidAssemblyListCacheIfExist** invalida la cache di descrizione del processore di input del testo.</span><span class="sxs-lookup"><span data-stu-id="63492-105">The **TF\_InvalidAssemblyListCacheIfExist** function invalidates the text input processor's description cache.</span></span> <span data-ttu-id="63492-106">Non è necessario chiamare questa funzione se il programma di installazione del processore di input richiede il riavvio o l'accesso.</span><span class="sxs-lookup"><span data-stu-id="63492-106">It is not necessary to call this function if the input processor setup program requires you to restart or log on.</span></span> <span data-ttu-id="63492-107">La cache è valida fino a quando l'utente non si disconnette.</span><span class="sxs-lookup"><span data-stu-id="63492-107">The cache is valid until the user logs off.</span></span>

## <a name="syntax"></a><span data-ttu-id="63492-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63492-108">Syntax</span></span>


```C++
HRESULT TF_InvalidAssemblyListCacheIfExist(void);
```



## <a name="parameters"></a><span data-ttu-id="63492-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="63492-109">Parameters</span></span>

<span data-ttu-id="63492-110">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="63492-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="63492-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63492-111">Return value</span></span>

<span data-ttu-id="63492-112">Questa funzione può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="63492-112">This function can return one of these values.</span></span>



| <span data-ttu-id="63492-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="63492-113">Return code</span></span>                                                                            | <span data-ttu-id="63492-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63492-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="63492-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63492-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="63492-116">La funzione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="63492-116">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="63492-117"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="63492-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="63492-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="63492-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="63492-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="63492-119">Examples</span></span>

<span data-ttu-id="63492-120">Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="63492-120">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="63492-121">Nell'esempio seguente viene illustrato come ottenere un puntatore a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="63492-121">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="63492-122">L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta.</span><span class="sxs-lookup"><span data-stu-id="63492-122">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="63492-123">Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="63492-123">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *pTF_InvalidAssemblyListCacheIfExist )(void);

HMODULE hMSCTF = LoadLibrary(TEXT("msctf.dll"));

if(hMSCTF == NULL)
{
    //Error loading module -- fail as securely as possible 
}

else
{
    pTF_InvalidAssemblyListCacheIfExist pfnInvalidAssemblyListCacheIfExist;
    
    pfnInvalidAssemblyListCacheIfExist = (pTF_InvalidAssemblyListCacheIfExist )GetProcAddress(hMSCTF, "TF_InvalidAssemblyListCacheIfExist");

    if(pfnInvalidAssemblyListCacheIfExist)
    {
        (*pfnInvalidAssemblyListCacheIfExist)();
       
    }

    FreeLibrary(hMSCTF);
}
```



## <a name="requirements"></a><span data-ttu-id="63492-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63492-124">Requirements</span></span>



| <span data-ttu-id="63492-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="63492-125">Requirement</span></span> | <span data-ttu-id="63492-126">Valore</span><span class="sxs-lookup"><span data-stu-id="63492-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="63492-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63492-127">Minimum supported client</span></span><br/> | <span data-ttu-id="63492-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="63492-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="63492-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63492-129">Minimum supported server</span></span><br/> | <span data-ttu-id="63492-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="63492-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="63492-131">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="63492-131">Redistributable</span></span><br/>          | <span data-ttu-id="63492-132">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="63492-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="63492-133">DLL</span><span class="sxs-lookup"><span data-stu-id="63492-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63492-134"><dt>Msctf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63492-134"><dt>Msctf.dll</dt></span></span> </dl> |



 


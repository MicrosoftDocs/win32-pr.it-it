---
description: Chiama la funzione GetLastError e converte il codice restituito in un valore HRESULT.
ms.assetid: 7b8eab85-212b-44bc-9d1b-60587652380d
title: SignError (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignError
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 7a405bef4666721e485e8b5ad6905209b2244bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049549"
---
# <a name="signerror-function"></a><span data-ttu-id="b73de-103">SignError (funzione)</span><span class="sxs-lookup"><span data-stu-id="b73de-103">SignError function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b73de-104">Questa API è deprecata.</span><span class="sxs-lookup"><span data-stu-id="b73de-104">This API is deprecated.</span></span> <span data-ttu-id="b73de-105">Microsoft può rimuovere questa API nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="b73de-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="b73de-106">La funzione **SignError** chiama la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) e converte il codice restituito in un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b73de-106">The **SignError** function calls the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function and converts the return code to an **HRESULT**.</span></span>

> [!Note]  
> <span data-ttu-id="b73de-107">A questa funzione non è associato alcun file di intestazione o libreria di importazione.</span><span class="sxs-lookup"><span data-stu-id="b73de-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="b73de-108">Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="b73de-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b73de-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b73de-109">Syntax</span></span>


```C++
HRESULT WINAPI SignError(void);
```



## <a name="parameters"></a><span data-ttu-id="b73de-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b73de-110">Parameters</span></span>

<span data-ttu-id="b73de-111">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="b73de-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b73de-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b73de-112">Return value</span></span>

<span data-ttu-id="b73de-113">Se il metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b73de-113">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="b73de-114">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="b73de-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="b73de-115">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="b73de-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b73de-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b73de-116">Requirements</span></span>



| <span data-ttu-id="b73de-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b73de-117">Requirement</span></span> | <span data-ttu-id="b73de-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b73de-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b73de-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b73de-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b73de-120">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b73de-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b73de-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b73de-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b73de-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b73de-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b73de-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b73de-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b73de-124"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b73de-124"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 

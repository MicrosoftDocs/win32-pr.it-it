---
description: Utilizzato da un provider del servizio di crittografia (CSP) per verificare la firma di una DLL.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: Puntatore a funzione CRYPT_VERIFY_IMAGE (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_VERIFY_IMAGE
- CRYPT_VERIFY_IMAGE_A
- CRYPT_VERIFY_IMAGE_W
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: e95414d09a7869aa4a2ef512fcff2765ba4491bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312808"
---
# <a name="crypt_verify_image-function-pointer"></a><span data-ttu-id="1e2ee-103">\_Puntatore alla \_ funzione di verifica immagine Crypt</span><span class="sxs-lookup"><span data-stu-id="1e2ee-103">CRYPT\_VERIFY\_IMAGE function pointer</span></span>

<span data-ttu-id="1e2ee-104">La funzione di callback **FuncVerifyImage** viene utilizzata da un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) per verificare la firma di una dll.</span><span class="sxs-lookup"><span data-stu-id="1e2ee-104">The **FuncVerifyImage** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to verify the signature of a DLL.</span></span>

<span data-ttu-id="1e2ee-105">Tutte le DLL ausiliarie in cui un CSP effettua chiamate di funzione devono essere firmate nello stesso modo (e con la stessa chiave) della DLL CSP primaria.</span><span class="sxs-lookup"><span data-stu-id="1e2ee-105">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="1e2ee-106">Per garantire la firma, le DLL ausiliarie devono essere caricate in modo dinamico tramite la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="1e2ee-106">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="1e2ee-107">Ma prima del caricamento della DLL, è necessario verificare la firma della DLL.</span><span class="sxs-lookup"><span data-stu-id="1e2ee-107">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="1e2ee-108">Il CSP esegue questa verifica chiamando la funzione **FuncVerifyImage** , come illustrato nell'esempio riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="1e2ee-108">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e2ee-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e2ee-109">Syntax</span></span>


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a><span data-ttu-id="1e2ee-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e2ee-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e2ee-111">*lpszImage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e2ee-111">*lpszImage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e2ee-112">Indirizzo di una stringa con terminazione null che contiene il percorso e il nome file della DLL per cui verificare la firma.</span><span class="sxs-lookup"><span data-stu-id="1e2ee-112">The address of a null-terminated string that contains the path and file name of the DLL to verify the signature for.</span></span>

</dd> <dt>

<span data-ttu-id="1e2ee-113">*pbSigData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e2ee-113">*pbSigData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e2ee-114">Indirizzo di un buffer contenente la firma.</span><span class="sxs-lookup"><span data-stu-id="1e2ee-114">The address of a buffer that contains the signature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e2ee-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e2ee-115">Return value</span></span>

<span data-ttu-id="1e2ee-116">Restituisce **true** se la funzione ha esito positivo, **false** in caso di esito negativo.</span><span class="sxs-lookup"><span data-stu-id="1e2ee-116">Returns **TRUE** if the function succeeds, **FALSE** if it fails.</span></span>

## <a name="examples"></a><span data-ttu-id="1e2ee-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="1e2ee-117">Examples</span></span>

<span data-ttu-id="1e2ee-118">Nell'esempio seguente viene illustrato come utilizzare la funzione di callback **FuncVerifyImage** per verificare la firma di una dll prima che venga caricata da un CSP.</span><span class="sxs-lookup"><span data-stu-id="1e2ee-118">The following example shows how to use the **FuncVerifyImage** callback function to verify the signature of a DLL before it is loaded by a CSP.</span></span>


```C++
BOOL (FARPROC *ProvVerifyImage)(LPCSTR lpszImage, BYTE *pSigData);


//  "ProvVerifyImage" has been set to "pVTable->FuncVerifyImage"
//  within the CPAcquireContext function.

//  bSignature is a previously assigned BYTE array that contains the
//  signature that is stored in the C:\Winnt40\System32\signature.sig
//  file. During development, this file is created with the 
//  Sign.exe tool.
...


//  Verify the signature in the
//  C:\Winnt40\System32\Signature.dll file.
if(RCRYPT_FAILED(ProvVerifyImage
    ("c:\\winnt40\\system32\\signature.dll",
        bSignature)) {
    SetLastError(NTE_BAD_SIGNATURE);
    return CRYPT_FAILED;
}

//  Load the DLL with the LoadLibrary function, then acquire pointers 
//  to the functions with the GetProcAddress function.
//...
```



## <a name="requirements"></a><span data-ttu-id="1e2ee-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e2ee-119">Requirements</span></span>



| <span data-ttu-id="1e2ee-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e2ee-120">Requirement</span></span> | <span data-ttu-id="1e2ee-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1e2ee-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2ee-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e2ee-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1e2ee-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1e2ee-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e2ee-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e2ee-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1e2ee-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1e2ee-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1e2ee-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e2ee-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e2ee-127"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e2ee-127"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e2ee-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e2ee-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e2ee-129">**CPAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="1e2ee-129">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="1e2ee-130">**VTableProvStruc**</span><span class="sxs-lookup"><span data-stu-id="1e2ee-130">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 

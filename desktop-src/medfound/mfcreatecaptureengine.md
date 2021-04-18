---
description: Crea un'istanza del motore di acquisizione.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: MFCreateCaptureEngine (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: a2ff0dbf46ca464c11570c8fe78e0b3dbebe3248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308414"
---
# <a name="mfcreatecaptureengine-function"></a><span data-ttu-id="244bc-103">MFCreateCaptureEngine (funzione)</span><span class="sxs-lookup"><span data-stu-id="244bc-103">MFCreateCaptureEngine function</span></span>

<span data-ttu-id="244bc-104">\[MFCreateCaptureEngine non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="244bc-104">\[MFCreateCaptureEngine is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="244bc-105">\]</span><span class="sxs-lookup"><span data-stu-id="244bc-105">\]</span></span>

<span data-ttu-id="244bc-106">Crea un'istanza del motore di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="244bc-106">Creates an instance of the capture engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="244bc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="244bc-107">Syntax</span></span>


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a><span data-ttu-id="244bc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="244bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="244bc-109">*ppCaptureEngine* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="244bc-109">*ppCaptureEngine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="244bc-110">Riceve un puntatore all'interfaccia [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) .</span><span class="sxs-lookup"><span data-stu-id="244bc-110">Receives a pointer to the [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) interface.</span></span> <span data-ttu-id="244bc-111">Il chiamante deve rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="244bc-111">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="244bc-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="244bc-112">Return value</span></span>

<span data-ttu-id="244bc-113">Se la funzione ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="244bc-113">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="244bc-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="244bc-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="244bc-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="244bc-115">Remarks</span></span>

<span data-ttu-id="244bc-116">Questa funzione non dispone di librerie di importazione associate e non è dichiarata in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="244bc-116">This function has no associated import library and is not declared in a public header file.</span></span> <span data-ttu-id="244bc-117">È necessario utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a MFCaptureEngine.dll.</span><span class="sxs-lookup"><span data-stu-id="244bc-117">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to MFCaptureEngine.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="244bc-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="244bc-118">Requirements</span></span>



| <span data-ttu-id="244bc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="244bc-119">Requirement</span></span> | <span data-ttu-id="244bc-120">Valore</span><span class="sxs-lookup"><span data-stu-id="244bc-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="244bc-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="244bc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="244bc-122">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="244bc-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="244bc-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="244bc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="244bc-124">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="244bc-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="244bc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="244bc-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="244bc-126"><dt>MFCaptureEngine.dll</dt></span><span class="sxs-lookup"><span data-stu-id="244bc-126"><dt>MFCaptureEngine.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="244bc-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="244bc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="244bc-128">Funzioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="244bc-128">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 

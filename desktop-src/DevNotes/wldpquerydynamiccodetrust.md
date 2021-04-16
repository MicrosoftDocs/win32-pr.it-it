---
description: Recupera un valore che determina se il codice dinamico del CRL .NET in memoria o su disco è considerato attendibile dai criteri di Device Guard.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: Funzione WldpQueryDynamicCodeTrust (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 1b9b3cc30f5a02ae86fd8a30043a9ab417ec1ac7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523466"
---
# <a name="wldpquerydynamiccodetrust-function"></a><span data-ttu-id="74617-103">WldpQueryDynamicCodeTrust (funzione)</span><span class="sxs-lookup"><span data-stu-id="74617-103">WldpQueryDynamicCodeTrust function</span></span>

<span data-ttu-id="74617-104">Recupera un valore che determina se il codice dinamico del CRL .NET in memoria o su disco è considerato attendibile dai criteri di Device Guard.</span><span class="sxs-lookup"><span data-stu-id="74617-104">Retrieves a value that determines if the specified in-memory or on-disk .NET CRL dynamic code is trusted by Device Guard policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="74617-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74617-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a><span data-ttu-id="74617-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74617-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74617-107">*fileHandle*</span><span class="sxs-lookup"><span data-stu-id="74617-107">*fileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="74617-108">Handle per il file di codice dinamico su disco da verificare.</span><span class="sxs-lookup"><span data-stu-id="74617-108">Handle to the on-disk dynamic code file to check.</span></span> <span data-ttu-id="74617-109">Se *filehandle* è diverso da **null**, *baseImage* deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="74617-109">If *fileHandle* is non-**NULL**, *baseImage* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="74617-110">*baseImage*</span><span class="sxs-lookup"><span data-stu-id="74617-110">*baseImage*</span></span> 
</dt> <dd>

<span data-ttu-id="74617-111">Puntatore al file PE in memoria da controllare.</span><span class="sxs-lookup"><span data-stu-id="74617-111">Pointer to the in-memory PE file to check.</span></span> <span data-ttu-id="74617-112">Se *baseImage* è diverso da **null**, *filehandle* deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="74617-112">If *baseImage* is non-**NULL**, *FileHandle* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="74617-113">*ImageSize*</span><span class="sxs-lookup"><span data-stu-id="74617-113">*ImageSize*</span></span> 
</dt> <dd>

<span data-ttu-id="74617-114">Quando *baseImage* è diverso da **null**, indica le dimensioni del buffer a cui punta *baseImage* .</span><span class="sxs-lookup"><span data-stu-id="74617-114">When *baseImage* is non-**NULL**, indicates the buffer size that *baseImage* points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74617-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74617-115">Return value</span></span>

<span data-ttu-id="74617-116">Questo metodo restituisce **\_ OK** se l'esito è positivo o un codice di errore; in caso contrario,.</span><span class="sxs-lookup"><span data-stu-id="74617-116">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="74617-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74617-117">Requirements</span></span>



| <span data-ttu-id="74617-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="74617-118">Requirement</span></span> | <span data-ttu-id="74617-119">Valore</span><span class="sxs-lookup"><span data-stu-id="74617-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="74617-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74617-120">Minimum supported client</span></span><br/> | <span data-ttu-id="74617-121">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="74617-121">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="74617-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74617-122">Minimum supported server</span></span><br/> | <span data-ttu-id="74617-123">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="74617-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="74617-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74617-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="74617-125"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="74617-125"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="74617-126">DLL</span><span class="sxs-lookup"><span data-stu-id="74617-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74617-127"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74617-127"><dt>Wldp.dll</dt></span></span> </dl> |



 

 





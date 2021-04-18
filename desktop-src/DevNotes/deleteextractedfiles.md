---
description: La funzione DeleteExtractedFiles Elimina i file estratti dalla funzione Extract.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: DeleteExtractedFiles (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 4ab032864e59d8e7379fe347d241874d9336e431
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327451"
---
# <a name="deleteextractedfiles-function"></a><span data-ttu-id="cbd06-103">DeleteExtractedFiles (funzione)</span><span class="sxs-lookup"><span data-stu-id="cbd06-103">DeleteExtractedFiles function</span></span>

<span data-ttu-id="cbd06-104">\[Questa funzione non è più supportata, pertanto non è possibile garantirne il comportamento.\]</span><span class="sxs-lookup"><span data-stu-id="cbd06-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="cbd06-105">La funzione **DeleteExtractedFiles** Elimina i file estratti dalla funzione [**Extract**](extract.md) .</span><span class="sxs-lookup"><span data-stu-id="cbd06-105">The **DeleteExtractedFiles** function deletes the files that were extracted by the [**Extract**](extract.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbd06-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cbd06-106">Syntax</span></span>


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a><span data-ttu-id="cbd06-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cbd06-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbd06-108">*ps*</span><span class="sxs-lookup"><span data-stu-id="cbd06-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="cbd06-109">Puntatore a una struttura di [**sessione**](session.md) che contiene informazioni sulla sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="cbd06-109">A pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

<span data-ttu-id="cbd06-110">Questa funzione libera la memoria nel membro **pFileList** della struttura e imposta **pFileList** su **null**.</span><span class="sxs-lookup"><span data-stu-id="cbd06-110">This function frees the memory in the **pFileList** member of this structure and sets **pFileList** to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbd06-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cbd06-111">Return value</span></span>

<span data-ttu-id="cbd06-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="cbd06-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbd06-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbd06-113">Remarks</span></span>

<span data-ttu-id="cbd06-114">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="cbd06-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbd06-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbd06-115">Requirements</span></span>



| <span data-ttu-id="cbd06-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbd06-116">Requirement</span></span> | <span data-ttu-id="cbd06-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cbd06-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd06-118">DLL</span><span class="sxs-lookup"><span data-stu-id="cbd06-118">DLL</span></span><br/> | <dl> <span data-ttu-id="cbd06-119"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbd06-119"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbd06-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbd06-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd06-121">**Estrarre**</span><span class="sxs-lookup"><span data-stu-id="cbd06-121">**Extract**</span></span>](extract.md)
</dt> <dt>

[<span data-ttu-id="cbd06-122">**SESSIONE**</span><span class="sxs-lookup"><span data-stu-id="cbd06-122">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 

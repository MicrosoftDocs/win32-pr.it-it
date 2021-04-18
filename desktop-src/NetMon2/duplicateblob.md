---
description: La funzione DuplicateBlob copia un BLOB specifico.
ms.assetid: d2478f53-328c-4799-890c-7849ce1f22e9
title: Funzione DuplicateBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DuplicateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: df0fc00f0bd51e89da432e6f3b0143ce6092cedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315464"
---
# <a name="duplicateblob-function"></a><span data-ttu-id="33675-103">DuplicateBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="33675-103">DuplicateBlob function</span></span>

<span data-ttu-id="33675-104">La funzione **DuplicateBlob** copia un blob specifico.</span><span class="sxs-lookup"><span data-stu-id="33675-104">The **DuplicateBlob** function copies a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="33675-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33675-105">Syntax</span></span>


```C++
DWORD DuplicateBlob(
  _In_  HBLOB hSrcBlob,
  _Out_ HBLOB *hBlobThatWillBeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="33675-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="33675-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33675-107">*hSrcBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33675-107">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33675-108">Handle per il BLOB copiato.</span><span class="sxs-lookup"><span data-stu-id="33675-108">Handle to the BLOB that is copied.</span></span>

</dd> <dt>

<span data-ttu-id="33675-109">*hBlobThatWillBeCreated* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="33675-109">*hBlobThatWillBeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33675-110">Handle per il BLOB duplicato.</span><span class="sxs-lookup"><span data-stu-id="33675-110">Handle to the duplicate BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33675-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33675-111">Return value</span></span>

<span data-ttu-id="33675-112">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="33675-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="33675-113">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.</span><span class="sxs-lookup"><span data-stu-id="33675-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="33675-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33675-114">Requirements</span></span>



| <span data-ttu-id="33675-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="33675-115">Requirement</span></span> | <span data-ttu-id="33675-116">Valore</span><span class="sxs-lookup"><span data-stu-id="33675-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33675-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33675-117">Minimum supported client</span></span><br/> | <span data-ttu-id="33675-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33675-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="33675-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33675-119">Minimum supported server</span></span><br/> | <span data-ttu-id="33675-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33675-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="33675-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33675-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="33675-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="33675-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="33675-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="33675-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="33675-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33675-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="33675-125">DLL</span><span class="sxs-lookup"><span data-stu-id="33675-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33675-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33675-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33675-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33675-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33675-128">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="33675-128">CreateBlob</span></span>](createblob.md)
</dt> <dt>

[<span data-ttu-id="33675-129">DestroyBlob</span><span class="sxs-lookup"><span data-stu-id="33675-129">DestroyBlob</span></span>](destroyblob.md)
</dt> </dl>

 

 





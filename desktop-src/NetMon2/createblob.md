---
description: La funzione CreateBlob crea un BLOB vuoto.
ms.assetid: fa31855b-af85-4ab5-b434-e54111731d8f
title: Funzione CreateBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: f2abb32afd68dd321a520c1d56c217e801fa9101
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756887"
---
# <a name="createblob-function"></a><span data-ttu-id="df3ef-103">CreateBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="df3ef-103">CreateBlob function</span></span>

<span data-ttu-id="df3ef-104">La funzione **CreateBlob** crea un BLOB vuoto.</span><span class="sxs-lookup"><span data-stu-id="df3ef-104">The **CreateBlob** function creates an empty BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="df3ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df3ef-105">Syntax</span></span>


```C++
DWORD CreateBlob(
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="df3ef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="df3ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df3ef-107">*phBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="df3ef-107">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df3ef-108">Puntatore alla variabile in cui viene restituito il puntatore al nuovo BLOB.</span><span class="sxs-lookup"><span data-stu-id="df3ef-108">Pointer to the variable where the pointer to the new BLOB is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df3ef-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df3ef-109">Return value</span></span>

<span data-ttu-id="df3ef-110">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="df3ef-110">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="df3ef-111">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.</span><span class="sxs-lookup"><span data-stu-id="df3ef-111">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="df3ef-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df3ef-112">Requirements</span></span>



| <span data-ttu-id="df3ef-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="df3ef-113">Requirement</span></span> | <span data-ttu-id="df3ef-114">Valore</span><span class="sxs-lookup"><span data-stu-id="df3ef-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df3ef-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df3ef-115">Minimum supported client</span></span><br/> | <span data-ttu-id="df3ef-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df3ef-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="df3ef-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df3ef-117">Minimum supported server</span></span><br/> | <span data-ttu-id="df3ef-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df3ef-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="df3ef-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df3ef-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="df3ef-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="df3ef-120"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="df3ef-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="df3ef-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="df3ef-122"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df3ef-122"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="df3ef-123">DLL</span><span class="sxs-lookup"><span data-stu-id="df3ef-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df3ef-124"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df3ef-124"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df3ef-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df3ef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df3ef-126">DestroyBlob</span><span class="sxs-lookup"><span data-stu-id="df3ef-126">DestroyBlob</span></span>](destroyblob.md)
</dt> </dl>

 

 





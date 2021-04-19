---
description: La funzione DestroyBlob libera tutta la memoria associata al BLOB e quindi Elimina il BLOB.
ms.assetid: 46cde0b7-1b59-426e-b19b-3c73af3d461a
title: Funzione DestroyBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e90630981c16f38d601d4e06d04f9326174ef721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317751"
---
# <a name="destroyblob-function"></a><span data-ttu-id="3c53e-103">DestroyBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="3c53e-103">DestroyBlob function</span></span>

<span data-ttu-id="3c53e-104">La funzione **DestroyBlob** libera tutta la memoria associata al BLOB e quindi Elimina il BLOB.</span><span class="sxs-lookup"><span data-stu-id="3c53e-104">The **DestroyBlob** function frees all memory associated with the BLOB and then destroys the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c53e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c53e-105">Syntax</span></span>


```C++
DWORD DestroyBlob(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="3c53e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c53e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c53e-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c53e-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c53e-108">Handle per il BLOB che viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="3c53e-108">Handle to the to the BLOB that is destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c53e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c53e-109">Return value</span></span>

<span data-ttu-id="3c53e-110">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3c53e-110">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3c53e-111">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.</span><span class="sxs-lookup"><span data-stu-id="3c53e-111">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c53e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c53e-112">Requirements</span></span>



| <span data-ttu-id="3c53e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c53e-113">Requirement</span></span> | <span data-ttu-id="3c53e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="3c53e-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c53e-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c53e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3c53e-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c53e-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3c53e-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c53e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3c53e-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c53e-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c53e-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c53e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c53e-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c53e-120"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3c53e-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="3c53e-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c53e-122"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c53e-122"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c53e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3c53e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c53e-124"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c53e-124"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c53e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c53e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c53e-126">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="3c53e-126">CreateBlob</span></span>](createblob.md)
</dt> </dl>

 

 





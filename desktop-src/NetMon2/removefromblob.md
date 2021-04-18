---
description: La funzione RemoveFromBlob elimina qualsiasi livello di voce del BLOB (proprietario, categoria o tag).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: Funzione RemoveFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RemoveFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a23e4e7e6e6d5c85b1284f8aaba49c1f8eae728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306555"
---
# <a name="removefromblob-function"></a><span data-ttu-id="24f55-103">RemoveFromBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="24f55-103">RemoveFromBlob function</span></span>

<span data-ttu-id="24f55-104">La funzione **RemoveFromBlob** elimina qualsiasi livello di voce del BLOB (**proprietario**, **categoria** o **tag**).</span><span class="sxs-lookup"><span data-stu-id="24f55-104">The **RemoveFromBlob** function deletes any level of BLOB entry (**Owner**, **Category**, or **Tag**).</span></span>

## <a name="syntax"></a><span data-ttu-id="24f55-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24f55-105">Syntax</span></span>


```C++
DWORD RemoveFromBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName
);
```



## <a name="parameters"></a><span data-ttu-id="24f55-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="24f55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24f55-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24f55-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f55-108">Handle per il BLOB da cui viene eliminata una voce.</span><span class="sxs-lookup"><span data-stu-id="24f55-108">Handle to the BLOB from which an entry is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="24f55-109">*pOwnerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24f55-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f55-110">Puntatore al nome del **proprietario** .</span><span class="sxs-lookup"><span data-stu-id="24f55-110">Pointer to the **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="24f55-111">*pCategoryName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24f55-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f55-112">Puntatore al nome della **categoria** .</span><span class="sxs-lookup"><span data-stu-id="24f55-112">Pointer to the **Category** name.</span></span> <span data-ttu-id="24f55-113">Un valore di parametro **null** indica che il chiamante sta provando a eliminare le informazioni sul **proprietario** specificate e tutte le relative voci figlio.</span><span class="sxs-lookup"><span data-stu-id="24f55-113">A **NULL** parameter value indicates the caller is attempting to delete the given **Owner** information and all of its child entries.</span></span> <span data-ttu-id="24f55-114">Si noti che se il valore del parametro *pCategoryName* è **null**, anche il parametro *pTagName* deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="24f55-114">Note that if the *pCategoryName* parameter value is **NULL**, the *pTagName* parameter must also be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="24f55-115">*pTagName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24f55-115">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24f55-116">Puntatore al nome del **tag** .</span><span class="sxs-lookup"><span data-stu-id="24f55-116">Pointer to the **Tag** name.</span></span> <span data-ttu-id="24f55-117">Un valore _PTagName_ **null** indica che il chiamante sta provando a eliminare la **categoria** specificata e tutte le relative voci figlio.</span><span class="sxs-lookup"><span data-stu-id="24f55-117">A **NULL**_pTagName_ value indicates the caller is attempting to delete the given **Category** and all of its child entries.</span></span> <span data-ttu-id="24f55-118">Se il valore del parametro non è **null**, il chiamante chiede che vengano eliminate solo le voci di **tag** specificate.</span><span class="sxs-lookup"><span data-stu-id="24f55-118">If the parameter value is not **NULL**, the caller is asking that only that the specified **Tag** entries be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24f55-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24f55-119">Return value</span></span>

<span data-ttu-id="24f55-120">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="24f55-120">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="24f55-121">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="24f55-121">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="24f55-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24f55-122">Requirements</span></span>



| <span data-ttu-id="24f55-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="24f55-123">Requirement</span></span> | <span data-ttu-id="24f55-124">Valore</span><span class="sxs-lookup"><span data-stu-id="24f55-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24f55-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24f55-125">Minimum supported client</span></span><br/> | <span data-ttu-id="24f55-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24f55-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="24f55-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24f55-127">Minimum supported server</span></span><br/> | <span data-ttu-id="24f55-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24f55-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24f55-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24f55-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="24f55-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="24f55-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="24f55-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="24f55-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="24f55-132"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24f55-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="24f55-133">DLL</span><span class="sxs-lookup"><span data-stu-id="24f55-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24f55-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24f55-134"><dt>Npptools.dll</dt></span></span> </dl> |



 

 





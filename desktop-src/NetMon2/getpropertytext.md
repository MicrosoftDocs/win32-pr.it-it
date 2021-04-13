---
description: La funzione GetPropertyText restituisce un puntatore al testo della proprietà.
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: Funzione GetPropertyText (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 10dbabf32840d2ae5f965687a6261b8bec27a1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342751"
---
# <a name="getpropertytext-function"></a><span data-ttu-id="adf7a-103">GetPropertyText (funzione)</span><span class="sxs-lookup"><span data-stu-id="adf7a-103">GetPropertyText function</span></span>

<span data-ttu-id="adf7a-104">La funzione **GetPropertyText** restituisce un puntatore al testo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="adf7a-104">The **GetPropertyText** function returns a pointer to the property text.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf7a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="adf7a-105">Syntax</span></span>


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="adf7a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="adf7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf7a-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adf7a-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adf7a-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="adf7a-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="adf7a-109">*lpPI* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adf7a-109">*lpPI* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adf7a-110">Puntatore a un'istanza della proprietà.</span><span class="sxs-lookup"><span data-stu-id="adf7a-110">Pointer to a property instance.</span></span>

</dd> <dt>

<span data-ttu-id="adf7a-111">*szBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adf7a-111">*szBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adf7a-112">Puntatore alla stringa di testo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="adf7a-112">Pointer to the property text string.</span></span>

</dd> <dt>

<span data-ttu-id="adf7a-113">*BufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adf7a-113">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adf7a-114">Dimensioni del buffer della stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="adf7a-114">Size of the text string buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adf7a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="adf7a-115">Return value</span></span>

<span data-ttu-id="adf7a-116">Se la funzione ha esito positivo, il valore restituito è un puntatore al testo della proprietà.</span><span class="sxs-lookup"><span data-stu-id="adf7a-116">If the function is successful, the return value is a pointer to the property text.</span></span>

<span data-ttu-id="adf7a-117">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="adf7a-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="adf7a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="adf7a-118">Remarks</span></span>

<span data-ttu-id="adf7a-119">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetPropertyText** .</span><span class="sxs-lookup"><span data-stu-id="adf7a-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyText** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="adf7a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="adf7a-120">Requirements</span></span>



| <span data-ttu-id="adf7a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="adf7a-121">Requirement</span></span> | <span data-ttu-id="adf7a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="adf7a-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="adf7a-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adf7a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="adf7a-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="adf7a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="adf7a-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adf7a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="adf7a-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="adf7a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="adf7a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="adf7a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="adf7a-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="adf7a-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="adf7a-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="adf7a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="adf7a-130"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="adf7a-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="adf7a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="adf7a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adf7a-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adf7a-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





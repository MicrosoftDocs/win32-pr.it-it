---
description: La funzione ParserTemporaryLockFrame blocca un frame quando immette un parser e sblocca il frame quando la funzione esce dal parser.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: Funzione ParserTemporaryLockFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserTemporaryLockFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 48fa646e709982d88093e0cbeb5e60375643351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317101"
---
# <a name="parsertemporarylockframe-function"></a><span data-ttu-id="06b34-103">ParserTemporaryLockFrame (funzione)</span><span class="sxs-lookup"><span data-stu-id="06b34-103">ParserTemporaryLockFrame function</span></span>

<span data-ttu-id="06b34-104">La funzione **ParserTemporaryLockFrame** blocca un frame quando immette un parser e sblocca il frame quando la funzione esce dal parser.</span><span class="sxs-lookup"><span data-stu-id="06b34-104">The **ParserTemporaryLockFrame** function locks a frame when it enters a parser and unlocks the frame when the function exits the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="06b34-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06b34-105">Syntax</span></span>


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="06b34-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="06b34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06b34-107">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06b34-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b34-108">Handle per il frame a cui punta il parser.</span><span class="sxs-lookup"><span data-stu-id="06b34-108">Handle to the frame that the parser points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06b34-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06b34-109">Return value</span></span>

<span data-ttu-id="06b34-110">Se la funzione ha esito positivo, il valore restituito è un puntatore al primo byte di dati nel frame.</span><span class="sxs-lookup"><span data-stu-id="06b34-110">If the function is successful, the return value is a pointer to the first byte of data in the frame.</span></span>

<span data-ttu-id="06b34-111">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="06b34-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="06b34-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="06b34-112">Remarks</span></span>

<span data-ttu-id="06b34-113">I parser non devono chiamare la funzione **LockFrame** .</span><span class="sxs-lookup"><span data-stu-id="06b34-113">Parsers should not call the **LockFrame** function.</span></span> <span data-ttu-id="06b34-114">Se un parser acquisisce un blocco e quindi genera un errore o viene restituito senza sbloccare il frame, il parser lascia il sistema in uno stato in cui non può modificare i protocolli né tagliare o copiare frame.</span><span class="sxs-lookup"><span data-stu-id="06b34-114">If a parser takes a lock and then generates a fault or returns without unlocking the frame, the parser leaves the system in a state where it cannot change protocols or cut or copy frames.</span></span> <span data-ttu-id="06b34-115">I parser devono usare la funzione **ParserTemporaryLockFrame** , che concede un blocco solo durante il contesto della voce della funzione nel parser.</span><span class="sxs-lookup"><span data-stu-id="06b34-115">Parsers should use the **ParserTemporaryLockFrame** function, which grants a lock only during the context of the function entry into the parser.</span></span> <span data-ttu-id="06b34-116">All'uscita dal parser, viene rilasciato il blocco del frame.</span><span class="sxs-lookup"><span data-stu-id="06b34-116">On exit from the parser, the lock for that frame is released.</span></span> <span data-ttu-id="06b34-117">Di conseguenza, il puntatore sarà valido solo dopo la restituzione del parser dalla chiamata alla funzione **AttachProperties** o **RecognizeFrame** .</span><span class="sxs-lookup"><span data-stu-id="06b34-117">As a result, the pointer will be valid only after the parser returns from the call to the **AttachProperties** or **RecognizeFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="06b34-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06b34-118">Requirements</span></span>



| <span data-ttu-id="06b34-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="06b34-119">Requirement</span></span> | <span data-ttu-id="06b34-120">Valore</span><span class="sxs-lookup"><span data-stu-id="06b34-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="06b34-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06b34-121">Minimum supported client</span></span><br/> | <span data-ttu-id="06b34-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="06b34-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="06b34-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06b34-123">Minimum supported server</span></span><br/> | <span data-ttu-id="06b34-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="06b34-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="06b34-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06b34-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="06b34-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="06b34-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="06b34-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="06b34-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="06b34-128"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06b34-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="06b34-129">DLL</span><span class="sxs-lookup"><span data-stu-id="06b34-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06b34-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06b34-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





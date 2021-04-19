---
description: Visualizza una finestra di messaggio con la stringa specificata, il nome del file di origine e il numero di riga. L'utente può ignorare il messaggio, immettere il debugger o chiudere l'applicazione. Ignorato nelle compilazioni al dettaglio.
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: Macro DbgBreak (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 099344a295de2657b40218b993ab9c4cb6411353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332705"
---
# <a name="dbgbreak-macro"></a><span data-ttu-id="65ce3-105">DbgBreak (macro)</span><span class="sxs-lookup"><span data-stu-id="65ce3-105">DbgBreak macro</span></span>

<span data-ttu-id="65ce3-106">Visualizza una finestra di messaggio con la stringa specificata, il nome del file di origine e il numero di riga.</span><span class="sxs-lookup"><span data-stu-id="65ce3-106">Displays a message box with the specified string, the name of the source file, and the line number.</span></span> <span data-ttu-id="65ce3-107">L'utente può ignorare il messaggio, immettere il debugger o chiudere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="65ce3-107">The user can ignore the message, enter the debugger, or quit the application.</span></span> <span data-ttu-id="65ce3-108">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="65ce3-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ce3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65ce3-109">Syntax</span></span>


```C++
void DbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="65ce3-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="65ce3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ce3-111">*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="65ce3-111">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="65ce3-112">Stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="65ce3-112">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65ce3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65ce3-113">Return value</span></span>

<span data-ttu-id="65ce3-114">Questa macro non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="65ce3-114">This macro does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="65ce3-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="65ce3-115">Examples</span></span>


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a><span data-ttu-id="65ce3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65ce3-116">Requirements</span></span>



| <span data-ttu-id="65ce3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="65ce3-117">Requirement</span></span> | <span data-ttu-id="65ce3-118">Valore</span><span class="sxs-lookup"><span data-stu-id="65ce3-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ce3-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65ce3-119">Header</span></span><br/> | <dl> <span data-ttu-id="65ce3-120"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65ce3-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ce3-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65ce3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ce3-122">Macro di asserzione e punti di interruzione</span><span class="sxs-lookup"><span data-stu-id="65ce3-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 





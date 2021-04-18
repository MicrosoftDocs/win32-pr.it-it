---
description: La funzione GetCaptureCommentFromFilename estrae il commento di acquisizione da un file di acquisizione.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: Funzione GetCaptureCommentFromFilename (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureCommentFromFilename
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9dbfb086ccc27ad2f4c35018c3384a4b81ef0528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305916"
---
# <a name="getcapturecommentfromfilename-function"></a><span data-ttu-id="c2544-103">GetCaptureCommentFromFilename (funzione)</span><span class="sxs-lookup"><span data-stu-id="c2544-103">GetCaptureCommentFromFilename function</span></span>

<span data-ttu-id="c2544-104">La funzione **GetCaptureCommentFromFilename** estrae il commento di acquisizione da un [*file di acquisizione*](c.md).</span><span class="sxs-lookup"><span data-stu-id="c2544-104">The **GetCaptureCommentFromFilename** function extracts the capture comment from a [*capture file*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2544-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2544-105">Syntax</span></span>


```C++
DWORD  WINAPI GetCaptureCommentFromFilename(
  _In_ LPSTR lpFilename,
  _In_ LPSTR lpComment,
  _In_ DWORD BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="c2544-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2544-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2544-107">*lpFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2544-107">*lpFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2544-108">Puntatore al nome del file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c2544-108">Pointer to the name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="c2544-109">*lpComment* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2544-109">*lpComment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2544-110">Puntatore a una stringa preallocata per il commento.</span><span class="sxs-lookup"><span data-stu-id="c2544-110">Pointer to a pre-allocated string for the comment.</span></span>

</dd> <dt>

<span data-ttu-id="c2544-111">*BufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2544-111">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2544-112">Dimensione della stringa.</span><span class="sxs-lookup"><span data-stu-id="c2544-112">Size of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2544-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2544-113">Return value</span></span>

<span data-ttu-id="c2544-114">Se la funzione ha esito positivo, ovvero se il commento viene trovato e copiato o se non è presente alcun commento nel file di acquisizione, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c2544-114">If the function is successful (that is, if the comment is found and copied, or there is no comment in the capture file), the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c2544-115">Se la funzione ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="c2544-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="c2544-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c2544-116">Return code</span></span>                                                                                                 | <span data-ttu-id="c2544-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2544-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2544-118"><dt>**\_errore di \_ lettura del file NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2544-118"><dt>**NMERR\_FILE\_READ\_ERROR**</dt></span></span> </dl>     | <span data-ttu-id="c2544-119">Impossibile leggere il commento di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c2544-119">The capture comment cannot be read.</span></span><br/>                               |
| <dl> <span data-ttu-id="c2544-120"><dt>**\_formato di \_ file non valido NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2544-120"><dt>**NMERR\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="c2544-121">Il frame di commento non è un formato di file valido.</span><span class="sxs-lookup"><span data-stu-id="c2544-121">The Comment frame is not a valid file format.</span></span><br/>                     |
| <dl> <span data-ttu-id="c2544-122"><dt>**il \_ file NMERR non è stato \_ \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="c2544-122"><dt>**NMERR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>      | <span data-ttu-id="c2544-123">Impossibile trovare il file specificato dal parametro *lpFileName* .</span><span class="sxs-lookup"><span data-stu-id="c2544-123">The file specified by the *lpFilename* parameter cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="c2544-124"><dt>**\_parametro NMERR non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2544-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="c2544-125">Uno dei parametri non è stato specificato correttamente.</span><span class="sxs-lookup"><span data-stu-id="c2544-125">One of the parameters is specified incorrectly.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="c2544-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2544-126">Remarks</span></span>

<span data-ttu-id="c2544-127">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetCaptureCommentFromFilename** .</span><span class="sxs-lookup"><span data-stu-id="c2544-127">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureCommentFromFilename** function.</span></span>

<span data-ttu-id="c2544-128">Per recuperare il commento di un'acquisizione in tempo reale, chiamare la funzione [GetCaptureComment](getcapturecomment.md) .</span><span class="sxs-lookup"><span data-stu-id="c2544-128">To retrieve the comment of a real-time capture, call the [GetCaptureComment](getcapturecomment.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2544-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2544-129">Requirements</span></span>



| <span data-ttu-id="c2544-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2544-130">Requirement</span></span> | <span data-ttu-id="c2544-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c2544-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c2544-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2544-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c2544-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c2544-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c2544-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2544-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c2544-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c2544-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c2544-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2544-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2544-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2544-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c2544-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="c2544-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2544-139"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2544-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c2544-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c2544-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2544-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2544-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2544-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2544-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2544-143">GetCaptureComment</span><span class="sxs-lookup"><span data-stu-id="c2544-143">GetCaptureComment</span></span>](getcapturecomment.md)
</dt> </dl>

 

 





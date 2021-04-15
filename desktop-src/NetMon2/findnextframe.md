---
description: Trova il frame successivo nel contesto di acquisizione corrente che corrisponde al filtro.
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: Funzione FindNextFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2e303f7f9031ad451ad19be8bc8cbcd3abae3f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525152"
---
# <a name="findnextframe-function"></a><span data-ttu-id="14ebe-103">FindNextFrame (funzione)</span><span class="sxs-lookup"><span data-stu-id="14ebe-103">FindNextFrame function</span></span>

<span data-ttu-id="14ebe-104">La funzione **FindNextFrame** trova il frame successivo nel contesto di acquisizione corrente che corrisponde al filtro.</span><span class="sxs-lookup"><span data-stu-id="14ebe-104">The **FindNextFrame** function finds the next frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ebe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14ebe-105">Syntax</span></span>


```C++
HFRAME WINAPI FindNextFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     HighestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="14ebe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="14ebe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14ebe-107">*hCurrentFrame*</span><span class="sxs-lookup"><span data-stu-id="14ebe-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="14ebe-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="14ebe-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="14ebe-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="14ebe-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="14ebe-110">Nome del protocollo, ad esempio TCP.</span><span class="sxs-lookup"><span data-stu-id="14ebe-110">The protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="14ebe-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="14ebe-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="14ebe-112">Indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="14ebe-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="14ebe-113">*SourceAddress*</span><span class="sxs-lookup"><span data-stu-id="14ebe-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="14ebe-114">Indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="14ebe-114">The source address.</span></span>

</dd> <dt>

<span data-ttu-id="14ebe-115">*ProtocolOffset*</span><span class="sxs-lookup"><span data-stu-id="14ebe-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="14ebe-116">Puntatore a una **parola** che riceverà l'offset del protocollo.</span><span class="sxs-lookup"><span data-stu-id="14ebe-116">A pointer to a **WORD** that will receive the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="14ebe-117">*OriginalFrameNumber*</span><span class="sxs-lookup"><span data-stu-id="14ebe-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="14ebe-118">Punto iniziale della ricerca.</span><span class="sxs-lookup"><span data-stu-id="14ebe-118">The starting point of the search.</span></span> <span data-ttu-id="14ebe-119">Per impostazione predefinita, questa funzione Cerca i frame 1.000 dal punto di partenza del *OriginalFrameNumber* .</span><span class="sxs-lookup"><span data-stu-id="14ebe-119">By default, this function searches forward 1,000 frames from the *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="14ebe-120">Per modificare la distanza di avanzamento della ricerca, aggiungere questa riga al file Nmapi.ini, che si trova nella \\ directory Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="14ebe-120">To change the search-forward distance, add this line to the Nmapi.ini file, located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="14ebe-121">MAXLOOKBACK =<new lookforward distance></span><span class="sxs-lookup"><span data-stu-id="14ebe-121">MAXLOOKBACK=<new lookforward distance></span></span>

</dd> <dt>

<span data-ttu-id="14ebe-122">*HighestFrame*</span><span class="sxs-lookup"><span data-stu-id="14ebe-122">*HighestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="14ebe-123">Numero di frame più elevato nell'acquisizione in cui viene eseguita la ricerca.</span><span class="sxs-lookup"><span data-stu-id="14ebe-123">The highest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14ebe-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14ebe-124">Return value</span></span>

<span data-ttu-id="14ebe-125">Se la funzione ha esito positivo, il valore restituito è un handle per il frame successivo.</span><span class="sxs-lookup"><span data-stu-id="14ebe-125">If the function is successful, the return value is a handle to the next frame.</span></span>

<span data-ttu-id="14ebe-126">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="14ebe-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="14ebe-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="14ebe-127">Remarks</span></span>

<span data-ttu-id="14ebe-128">Il filtro di acquisizione viene definito principalmente dal parametro *ProtocolName* , che è l'unico input di filtro necessario; è possibile aggiungere i dati *DestinationAddress* e *sourceAddress* per aumentare la velocità di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="14ebe-128">The capture filter is defined primarily by the *ProtocolName* parameter, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* data to increase the capture speed.</span></span>

<span data-ttu-id="14ebe-129">Il puntatore *ProtocolOffset* viene restituito al parser chiamante, che aggiunge la **parola** al puntatore restituito bloccando il frame (con [ParserTemporaryLockFrame](parsertemporarylockframe.md)) per ottenere l' **LPBYTE** del protocollo cercato.</span><span class="sxs-lookup"><span data-stu-id="14ebe-129">The *ProtocolOffset* pointer is returned to the calling parser, which adds the **WORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the **LPBYTE** of the protocol searched for.</span></span> <span data-ttu-id="14ebe-130">Al ritorno, il HFRAME che ha superato il filtro viene assegnato al parser.</span><span class="sxs-lookup"><span data-stu-id="14ebe-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="14ebe-131">Se il parser rileva che questo frame non è quello cercato, il parser può restituire il HFRAME alla funzione **FindNextFrame** per ottenere il frame successivo.</span><span class="sxs-lookup"><span data-stu-id="14ebe-131">If the parser finds that this frame is not the one sought, the parser can hand the HFRAME back to the **FindNextFrame** function to get the next frame.</span></span> <span data-ttu-id="14ebe-132">Gli indirizzi di origine e di destinazione non sono obbligatori e possono essere passati come **null**.</span><span class="sxs-lookup"><span data-stu-id="14ebe-132">The source and destination addresses are not required and can be passed as **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="14ebe-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14ebe-133">Requirements</span></span>



| <span data-ttu-id="14ebe-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="14ebe-134">Requirement</span></span> | <span data-ttu-id="14ebe-135">Valore</span><span class="sxs-lookup"><span data-stu-id="14ebe-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="14ebe-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14ebe-136">Minimum supported client</span></span><br/> | <span data-ttu-id="14ebe-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14ebe-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="14ebe-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14ebe-138">Minimum supported server</span></span><br/> | <span data-ttu-id="14ebe-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14ebe-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="14ebe-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14ebe-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="14ebe-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="14ebe-141"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="14ebe-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="14ebe-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="14ebe-143"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14ebe-143"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="14ebe-144">DLL</span><span class="sxs-lookup"><span data-stu-id="14ebe-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14ebe-145"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14ebe-145"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





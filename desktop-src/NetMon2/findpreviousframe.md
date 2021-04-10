---
description: La funzione FindPreviousFrame trova il frame precedente nel contesto di acquisizione corrente che corrisponde al filtro.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: Funzione FindPreviousFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPreviousFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: deabf10702ca41c23101c5f60c9459e094e567fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966477"
---
# <a name="findpreviousframe-function"></a><span data-ttu-id="bf0cc-103">FindPreviousFrame (funzione)</span><span class="sxs-lookup"><span data-stu-id="bf0cc-103">FindPreviousFrame function</span></span>

<span data-ttu-id="bf0cc-104">La funzione **FindPreviousFrame** trova il frame precedente nel contesto di acquisizione corrente che corrisponde al filtro.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-104">The **FindPreviousFrame** function finds the previous frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf0cc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf0cc-105">Syntax</span></span>


```C++
HFRAME WINAPI FindPreviousFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     LowestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="bf0cc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf0cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf0cc-107">*hCurrentFrame*</span><span class="sxs-lookup"><span data-stu-id="bf0cc-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0cc-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="bf0cc-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="bf0cc-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0cc-110">Nome del protocollo, ad esempio TCP.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-110">Protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="bf0cc-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="bf0cc-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0cc-112">Indirizzo di destinazione del frame cercato.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-112">Destination address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="bf0cc-113">*SourceAddress*</span><span class="sxs-lookup"><span data-stu-id="bf0cc-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0cc-114">Indirizzo di origine del frame cercato.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-114">Source address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="bf0cc-115">*ProtocolOffset*</span><span class="sxs-lookup"><span data-stu-id="bf0cc-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0cc-116">Puntatore a una **parola** che riceve l'offset del protocollo.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-116">Pointer to a **WORD** that receives the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="bf0cc-117">*OriginalFrameNumber*</span><span class="sxs-lookup"><span data-stu-id="bf0cc-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0cc-118">Punto iniziale della ricerca.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-118">Starting point of the search.</span></span> <span data-ttu-id="bf0cc-119">Per impostazione predefinita, questa funzione esegue la ricerca all'indietro dei frame 1.000 dal punto di partenza del *OriginalFrameNumber* .</span><span class="sxs-lookup"><span data-stu-id="bf0cc-119">By default, this function searches backward 1,000 frames from *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="bf0cc-120">È possibile modificare la distanza di ricerca aggiungendo questa riga al file Nmapi.ini, che si trova nella \\ directory Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-120">You can change the search-back distance by adding this line to the Nmapi.ini file, which is located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="bf0cc-121">MAXLOOKBACK =<new lookback distance></span><span class="sxs-lookup"><span data-stu-id="bf0cc-121">MAXLOOKBACK=<new lookback distance></span></span>

</dd> <dt>

<span data-ttu-id="bf0cc-122">*LowestFrame*</span><span class="sxs-lookup"><span data-stu-id="bf0cc-122">*LowestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="bf0cc-123">Numero di frame più basso nell'acquisizione in cui viene eseguita la ricerca.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-123">Lowest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf0cc-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf0cc-124">Return value</span></span>

<span data-ttu-id="bf0cc-125">Se la funzione ha esito positivo, il valore restituito è un handle per il frame precedente.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-125">If the function is successful, the return value is a handle to the previous frame.</span></span>

<span data-ttu-id="bf0cc-126">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf0cc-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf0cc-127">Remarks</span></span>

<span data-ttu-id="bf0cc-128">Il filtro di acquisizione è definito principalmente da *ProtocolName*, che è l'unico input di filtro necessario; è possibile aggiungere informazioni su *DestinationAddress* e *sourceAddress* per aumentare la velocità di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-128">The capture filter is defined primarily by *ProtocolName*, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* information to increase the capture speed.</span></span>

<span data-ttu-id="bf0cc-129">*ProtocolOffset* viene restituito al parser chiamante, che aggiunge questo **DWORD** al puntatore restituito bloccando il frame (con [PARSERTEMPORARYLOCKFRAME](parsertemporarylockframe.md)) per ottenere il LPBYTE del protocollo di cui viene eseguita la ricerca.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-129">*ProtocolOffset* is returned to the calling parser, which adds this **DWORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the LPBYTE of the protocol that is being searched for.</span></span> <span data-ttu-id="bf0cc-130">Al ritorno, il HFRAME che ha superato il filtro viene assegnato al parser.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="bf0cc-131">Se il parser rileva che il frame non è quello cercato, il parser può restituire questo HFRAME alla funzione **FindPreviousFrame** per recuperare il frame successivo.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-131">If the parser finds that the frame is not the one that is being sought, the parser can hand this HFRAME back to the **FindPreviousFrame** function to retrieve the next frame.</span></span> <span data-ttu-id="bf0cc-132">Gli indirizzi di origine e di destinazione, che non sono obbligatori, possono essere passati come **null**.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-132">The source and destination addresses, which are not required, can be passed in as **NULL**.</span></span> <span data-ttu-id="bf0cc-133">Se utilizzati, questi indirizzi possono essere di tipo indirizzo \_ \_ IP e così via, non solo i tipi Mac.</span><span class="sxs-lookup"><span data-stu-id="bf0cc-133">When used, these addresses can be of type ADDRESS\_TYPE\_IP, and so on, not just MAC types.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf0cc-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf0cc-134">Requirements</span></span>



| <span data-ttu-id="bf0cc-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf0cc-135">Requirement</span></span> | <span data-ttu-id="bf0cc-136">Valore</span><span class="sxs-lookup"><span data-stu-id="bf0cc-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bf0cc-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf0cc-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bf0cc-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bf0cc-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bf0cc-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf0cc-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bf0cc-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bf0cc-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bf0cc-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf0cc-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf0cc-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf0cc-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="bf0cc-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="bf0cc-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf0cc-144"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf0cc-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="bf0cc-145">DLL</span><span class="sxs-lookup"><span data-stu-id="bf0cc-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf0cc-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf0cc-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





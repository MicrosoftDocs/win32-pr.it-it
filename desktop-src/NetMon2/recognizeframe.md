---
description: La funzione di esportazione RecognizeFrame indica se una porzione di dati viene riconosciuta come protocollo rilevato dal parser. La funzione di esportazione RecognizeFrame deve essere implementata per ogni parser supportato dalla DLL del parser.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: Funzione di callback RecognizeFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizeFrame
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: e2660629cecfa279377794749714102077fb6979
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319406"
---
# <a name="recognizeframe-callback-function"></a><span data-ttu-id="f1566-104">Funzione di callback RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="f1566-104">RecognizeFrame callback function</span></span>

<span data-ttu-id="f1566-105">La funzione di esportazione **RecognizeFrame** indica se una porzione di dati viene riconosciuta come protocollo rilevato dal parser.</span><span class="sxs-lookup"><span data-stu-id="f1566-105">The **RecognizeFrame** export function indicates whether a piece of data is recognized as the protocol that the parser detects.</span></span> <span data-ttu-id="f1566-106">La funzione di esportazione **RecognizeFrame** deve essere implementata per ogni parser supportato dalla dll del parser.</span><span class="sxs-lookup"><span data-stu-id="f1566-106">The **RecognizeFrame** export function must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1566-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1566-107">Syntax</span></span>


```C++
LPBYTE RecognizeFrame(
  _In_    HFRAME      hFrame,
  _In_    LPBYTE      lpFrame,
  _In_    LPBYTE      lpProtocol,
  _In_    DWORD       MacType,
  _In_    DWORD       BytesLeft,
  _In_    HPROTOCOL   hPreviousProtocol,
  _In_    DWORD       nPreviousProtocolOffset,
  _Out_   LPDWORD     ProtocolStatusCode,
  _Out_   LPHPROTOCOL phNextProtocol,
  _Inout_ PDWORD_PTR  lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="f1566-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1566-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1566-109">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1566-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1566-110">Handle per il frame che contiene i dati.</span><span class="sxs-lookup"><span data-stu-id="f1566-110">Handle to the frame that contains the data.</span></span>

</dd> <dt>

<span data-ttu-id="f1566-111">*lpFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1566-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1566-112">Puntatore al primo byte di un frame.</span><span class="sxs-lookup"><span data-stu-id="f1566-112">Pointer to the first byte of a frame.</span></span> <span data-ttu-id="f1566-113">Il puntatore fornisce un modo per visualizzare i dati riconosciuti da altri parser.</span><span class="sxs-lookup"><span data-stu-id="f1566-113">The pointer provides a way to view data that other parsers recognize.</span></span>

</dd> <dt>

<span data-ttu-id="f1566-114">*lpProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1566-114">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1566-115">Puntatore all'inizio dei dati non recuperati.</span><span class="sxs-lookup"><span data-stu-id="f1566-115">Pointer to the start of the unclaimed data.</span></span> <span data-ttu-id="f1566-116">In genere, i dati non reclamati si trovano al centro di un frame perché un parser precedente ha richiesto i dati prima del parser.</span><span class="sxs-lookup"><span data-stu-id="f1566-116">Typically, the unclaimed data is located in the middle of a frame because a previous parser has claimed data before this parser.</span></span> <span data-ttu-id="f1566-117">Il parser deve prima testare i dati non recuperati.</span><span class="sxs-lookup"><span data-stu-id="f1566-117">The parser must test the unclaimed data first.</span></span>

</dd> <dt>

<span data-ttu-id="f1566-118">*MacType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1566-118">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1566-119">Valore MAC del primo protocollo in un frame.</span><span class="sxs-lookup"><span data-stu-id="f1566-119">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="f1566-120">In genere, il valore *MacType* viene usato quando il parser deve identificare il primo protocollo in un frame.</span><span class="sxs-lookup"><span data-stu-id="f1566-120">Typically, the *MacType* value is used when the parser must identify the first protocol in a frame.</span></span> <span data-ttu-id="f1566-121">Il valore di *MacType* può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="f1566-121">The *MacType* value can be one of the following:</span></span>



| <span data-ttu-id="f1566-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f1566-122">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="f1566-123">Significato</span><span class="sxs-lookup"><span data-stu-id="f1566-123">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="f1566-124"><dt>**\_Ethernet di tipo Mac \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f1566-124"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="f1566-125">802.3</span><span class="sxs-lookup"><span data-stu-id="f1566-125">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="f1566-126"><dt>**\_Tokenring di tipo Mac \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f1566-126"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="f1566-127">802.5</span><span class="sxs-lookup"><span data-stu-id="f1566-127">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="f1566-128"><dt>**\_FDDI di tipo Mac \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f1566-128"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="f1566-129">ANSI X3T 9.5</span><span class="sxs-lookup"><span data-stu-id="f1566-129">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="f1566-130">*BytesLeft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1566-130">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1566-131">Il numero rimanente di byte da una posizione in un frame alla fine del frame.</span><span class="sxs-lookup"><span data-stu-id="f1566-131">The remaining number of bytes from a location in a frame to the end of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="f1566-132">*hPreviousProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1566-132">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1566-133">Handle del protocollo precedente.</span><span class="sxs-lookup"><span data-stu-id="f1566-133">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="f1566-134">*nPreviousProtocolOffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1566-134">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1566-135">Offset dell'inizio del protocollo precedente del frame.</span><span class="sxs-lookup"><span data-stu-id="f1566-135">Offset of the previous protocol   beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="f1566-136">*ProtocolStatusCode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f1566-136">*ProtocolStatusCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1566-137">Indicatore di stato del protocollo.</span><span class="sxs-lookup"><span data-stu-id="f1566-137">Protocol status indicator.</span></span> <span data-ttu-id="f1566-138">La DLL del parser deve impostare uno dei seguenti codici di stato.</span><span class="sxs-lookup"><span data-stu-id="f1566-138">The parser DLL must set one of the following status codes.</span></span>



| <span data-ttu-id="f1566-139">Valore</span><span class="sxs-lookup"><span data-stu-id="f1566-139">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="f1566-140">Significato</span><span class="sxs-lookup"><span data-stu-id="f1566-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <span data-ttu-id="f1566-141"><dt>**stato del protocollo \_ \_ riconosciuto**</dt></span><span class="sxs-lookup"><span data-stu-id="f1566-141"><dt>**PROTOCOL\_STATUS\_RECOGNIZED**</dt></span></span> </dl>              | <span data-ttu-id="f1566-142">Il parser riconosce i dati, ma non sa quale protocollo segue.</span><span class="sxs-lookup"><span data-stu-id="f1566-142">The parser recognizes the data but does not know which protocol follows.</span></span> <span data-ttu-id="f1566-143">Dopo aver impostato il codice, restituire un puntatore ai dati non attestati rimanenti che seguono il protocollo riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f1566-143">After setting the code, return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="f1566-144">Network Monitor usa il [*set*](f.md) di protocolli seguente per continuare l'analisi.</span><span class="sxs-lookup"><span data-stu-id="f1566-144">Network Monitor uses the [*follow set*](f.md) of the protocol to continue parsing.</span></span> <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <span data-ttu-id="f1566-145"><dt>**\_stato protocollo \_ non \_ riconosciuto**</dt></span><span class="sxs-lookup"><span data-stu-id="f1566-145"><dt>**PROTOCOL\_STATUS\_NOT\_RECOGNIZED**</dt></span></span> </dl> | <span data-ttu-id="f1566-146">Il parser non riconosce i dati.</span><span class="sxs-lookup"><span data-stu-id="f1566-146">The parser does not recognize the data.</span></span> <span data-ttu-id="f1566-147">Dopo aver impostato questo codice, restituire il puntatore all'inizio dei dati utilizzando il puntatore passato dal parametro *lpProtocol* alla DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="f1566-147">After setting this code, return the pointer to the beginning of the data   using the pointer that the *lpProtocol* parameter passes to the parser DLL.</span></span> <span data-ttu-id="f1566-148">Network Monitor usa il *set seguente* del protocollo precedente per continuare l'analisi.</span><span class="sxs-lookup"><span data-stu-id="f1566-148">Network Monitor uses the *follow set* of the previous protocol to continue parsing.</span></span> <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <span data-ttu-id="f1566-149"><dt>**stato del protocollo \_ \_ richiesto**</dt></span><span class="sxs-lookup"><span data-stu-id="f1566-149"><dt>**PROTOCOL\_STATUS\_CLAIMED**</dt></span></span> </dl>                       | <span data-ttu-id="f1566-150">Il parser riconosce i dati e dichiara i dati rimanenti.</span><span class="sxs-lookup"><span data-stu-id="f1566-150">The parser recognizes the data and claims the remaining data.</span></span> <span data-ttu-id="f1566-151">Dopo aver impostato il codice, restituire **null** per Network Monitor per terminare l'analisi di un frame.</span><span class="sxs-lookup"><span data-stu-id="f1566-151">After setting the code, return **NULL** for Network Monitor to terminate parsing a frame.</span></span> <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <span data-ttu-id="f1566-152"><dt>**\_protocollo stato protocollo \_ successivo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f1566-152"><dt>**PROTOCOL\_STATUS\_NEXT\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="f1566-153">Il parser riconosce i dati e sa quale protocollo segue.</span><span class="sxs-lookup"><span data-stu-id="f1566-153">The parser recognizes the data and knows which protocol follows.</span></span> <span data-ttu-id="f1566-154">Dopo aver impostato il codice, impostare il parametro *phNextProtocol* e restituire un puntatore ai dati non attestati rimanenti che seguono il protocollo riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f1566-154">After setting the code, set the *phNextProtocol* parameter, and return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="f1566-155">Network Monitor continua ad analizzare il frame.</span><span class="sxs-lookup"><span data-stu-id="f1566-155">Network Monitor continues parsing the frame.</span></span> <br/>                               |



 

</dd> <dt>

<span data-ttu-id="f1566-156">*phNextProtocol* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f1566-156">*phNextProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1566-157">Puntatore all'handle del protocollo successivo.</span><span class="sxs-lookup"><span data-stu-id="f1566-157">Pointer to the handle of the next protocol.</span></span> <span data-ttu-id="f1566-158">Questo parametro viene impostato quando un protocollo identifica il protocollo che segue un protocollo.</span><span class="sxs-lookup"><span data-stu-id="f1566-158">This parameter is set when a protocol identifies the protocol that follows a protocol.</span></span> <span data-ttu-id="f1566-159">Per ottenere l'handle del protocollo successivo, chiamare la funzione [GetProtocolFromTable](getprotocolfromtable.md) .</span><span class="sxs-lookup"><span data-stu-id="f1566-159">To obtain the handle of the next protocol, call the [GetProtocolFromTable](getprotocolfromtable.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f1566-160">*lpInstData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f1566-160">*lpInstData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1566-161">In input, puntatore ai dati dell'istanza del protocollo precedente.</span><span class="sxs-lookup"><span data-stu-id="f1566-161">On input, a pointer to the instance data from the previous protocol.</span></span>

<span data-ttu-id="f1566-162">Nell'output, un puntatore ai dati dell'istanza per il protocollo corrente.</span><span class="sxs-lookup"><span data-stu-id="f1566-162">On output, a pointer to the instance data for the current protocol.</span></span> <span data-ttu-id="f1566-163">I dati dell'istanza non possono essere più lunghi di un \_ ptr DWORD di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="f1566-163">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1566-164">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1566-164">Return value</span></span>

<span data-ttu-id="f1566-165">Se la funzione ha esito positivo, il valore restituito è un puntatore al primo byte dopo i dati del parser riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="f1566-165">If the function is successful, the return value is a pointer to the first byte after the recognized parser data.</span></span> <span data-ttu-id="f1566-166">Se il parser reclama tutti i dati rimanenti, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="f1566-166">If the parser claims all the remaining data, the return value is **NULL**.</span></span>

<span data-ttu-id="f1566-167">Se la funzione ha esito negativo, il valore restituito è un puntatore iniziale passato dal parametro *lpProtocol* .</span><span class="sxs-lookup"><span data-stu-id="f1566-167">If the function is unsuccessful, the return value is an initial pointer that the *lpProtocol* parameter passes-in.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1566-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1566-168">Remarks</span></span>

<span data-ttu-id="f1566-169">La funzione **RecognizeFrame** determina se il parser riconosce i dati non elaborati a partire dal puntatore *lpProtocol* .</span><span class="sxs-lookup"><span data-stu-id="f1566-169">The **RecognizeFrame** function determines whether the parser recognizes the raw data   starting at the *lpProtocol* pointer.</span></span>

-   <span data-ttu-id="f1566-170">Se il protocollo riconosce i dati, la funzione **RecognizeFrame** restituisce un puntatore ai dati rimanenti oppure restituisce **null** se il protocollo corrente è l'ultimo protocollo in un frame.</span><span class="sxs-lookup"><span data-stu-id="f1566-170">If the protocol recognizes the data, the **RecognizeFrame** function returns a pointer to the remaining data, or returns **NULL** if the current protocol is the last protocol in a frame.</span></span>
-   <span data-ttu-id="f1566-171">Se il protocollo non riconosce i dati, la funzione **RecognizeFrame** restituisce il puntatore passato alla DLL del parser nel parametro *lpProtocol* .</span><span class="sxs-lookup"><span data-stu-id="f1566-171">If the protocol does not recognize the data, the **RecognizeFrame** function returns the pointer passed to the parser DLL in the *lpProtocol* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="f1566-172">È possibile chiamare *RecognizeFrame* prima di chiamare la funzione [*Register*](register-parser.md) per registrare le proprietà del protocollo.</span><span class="sxs-lookup"><span data-stu-id="f1566-172">*RecognizeFrame* can be called before the [*Register*](register-parser.md) function is called to register the protocol properties.</span></span> <span data-ttu-id="f1566-173">Per questo motivo, l'implementazione della funzione *RecognizeFrame* non si basa su alcuna proprietà o struttura creata o inizializzata durante l'implementazione della funzione di **Registro** del protocollo.</span><span class="sxs-lookup"><span data-stu-id="f1566-173">For that reason, the implementation of the *RecognizeFrame* function does not rely on any properties or structures that are created or initialized during the implementation of the protocol **Register** function.</span></span>

 

<span data-ttu-id="f1566-174">**Set di continuità e set di seguito**</span><span class="sxs-lookup"><span data-stu-id="f1566-174">**Handoff Set and Follow Set**</span></span>

<span data-ttu-id="f1566-175">Un parser può usare un set di continuità o un set di istruzioni per identificare per Network Monitor il protocollo che segue i dati riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="f1566-175">A parser can use a handoff set or follow set to identify for Network Monitor the protocol that follows recognized data.</span></span>

-   <span data-ttu-id="f1566-176">Se le informazioni sono disponibili nei dati riconosciuti, il parser usa il set di continuità per ottenere un handle per il protocollo successivo, quindi passa tale handle a Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="f1566-176">If information is available in recognized data, the parser uses its handoff set to obtain a handle to the next protocol, and then passes that handle to Network Monitor.</span></span>
-   <span data-ttu-id="f1566-177">Se le informazioni non sono disponibili, il parser non passa un handle e Network Monitor usa il set di parser seguente per determinare il protocollo che segue.</span><span class="sxs-lookup"><span data-stu-id="f1566-177">If information is not available, the parser does not pass a handle, and Network Monitor uses the parser follow set to determine which protocol follows.</span></span>

<span data-ttu-id="f1566-178">**Passaggio di informazioni tra protocolli**</span><span class="sxs-lookup"><span data-stu-id="f1566-178">**Passing information between protocols**</span></span>

<span data-ttu-id="f1566-179">Usare il parametro *lpInstData* per passare le informazioni tra i protocolli.</span><span class="sxs-lookup"><span data-stu-id="f1566-179">Use the *lpInstData* parameter to pass information between protocols.</span></span> <span data-ttu-id="f1566-180">In input è possibile recuperare le informazioni dal protocollo precedente.</span><span class="sxs-lookup"><span data-stu-id="f1566-180">On input, you can retrieve the information from the previous protocol.</span></span> <span data-ttu-id="f1566-181">Nell'output è possibile passare informazioni al protocollo successivo.</span><span class="sxs-lookup"><span data-stu-id="f1566-181">On output, you can pass information to the next protocol.</span></span>

<span data-ttu-id="f1566-182">I dati dell'istanza possono essere dati di lunghezza minore o uguale a un \_ ptr DWORD o un puntatore ai dati, ad esempio dati di frame non elaborati, che non devono essere allocati o liberati dal parser.</span><span class="sxs-lookup"><span data-stu-id="f1566-182">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>



| <span data-ttu-id="f1566-183">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="f1566-183">For Information on</span></span>                                        | <span data-ttu-id="f1566-184">Vedere</span><span class="sxs-lookup"><span data-stu-id="f1566-184">See</span></span>                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1566-185">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="f1566-185">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="f1566-186">Parser</span><span class="sxs-lookup"><span data-stu-id="f1566-186">Parsers</span></span>](parsers.md)                                                                                                    |
| <span data-ttu-id="f1566-187">I punti di ingresso inclusi nella DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="f1566-187">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="f1566-188">Architettura DLL parser</span><span class="sxs-lookup"><span data-stu-id="f1566-188">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                                                                    |
| <span data-ttu-id="f1566-189">L'implementazione di **RecognizeFrame**  include un esempio.</span><span class="sxs-lookup"><span data-stu-id="f1566-189">How to implement **RecognizeFrame**  includes an example.</span></span> | [<span data-ttu-id="f1566-190">Implementazione di RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="f1566-190">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)                                                            |
| <span data-ttu-id="f1566-191">Come specificare un set di continuità e seguire il set.</span><span class="sxs-lookup"><span data-stu-id="f1566-191">How to specify a handoff set and follow set.</span></span>              | <span data-ttu-id="f1566-192">[Specifica di un set di continuità](specifying-a-handoff-set.md)che[specifica un set di seguito](specifying-a-follow-set.md)</span><span class="sxs-lookup"><span data-stu-id="f1566-192">[Specifying a Handoff Set](specifying-a-handoff-set.md)[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f1566-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1566-193">Requirements</span></span>



| <span data-ttu-id="f1566-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1566-194">Requirement</span></span> | <span data-ttu-id="f1566-195">Valore</span><span class="sxs-lookup"><span data-stu-id="f1566-195">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f1566-196">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1566-196">Minimum supported client</span></span><br/> | <span data-ttu-id="f1566-197">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1566-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f1566-198">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1566-198">Minimum supported server</span></span><br/> | <span data-ttu-id="f1566-199">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1566-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f1566-200">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1566-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1566-201"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1566-201"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1566-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1566-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1566-203">GetProtocolFromTable</span><span class="sxs-lookup"><span data-stu-id="f1566-203">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> </dl>

 

 





---
description: Recupera l'indirizzo di destinazione di un frame.
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: Funzione GetFrameDestAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: afec32f0e0fc66ccd5a1d78cc9769b0e742f1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966473"
---
# <a name="getframedestaddress-function"></a><span data-ttu-id="45180-103">GetFrameDestAddress (funzione)</span><span class="sxs-lookup"><span data-stu-id="45180-103">GetFrameDestAddress function</span></span>

<span data-ttu-id="45180-104">La funzione **GetFrameDestAddress** recupera l'indirizzo di destinazione di un frame.</span><span class="sxs-lookup"><span data-stu-id="45180-104">The **GetFrameDestAddress** function retrieves the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="45180-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45180-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDestAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="45180-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="45180-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45180-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="45180-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="45180-108">Handle del frame a cui ottenere un puntatore.</span><span class="sxs-lookup"><span data-stu-id="45180-108">A handle of the frame to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="45180-109">*lpAddress*</span><span class="sxs-lookup"><span data-stu-id="45180-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="45180-110">Buffer restituito che archivia l'indirizzo di destinazione del frame.</span><span class="sxs-lookup"><span data-stu-id="45180-110">A return buffer that stores the frame destination address.</span></span>

</dd> <dt>

<span data-ttu-id="45180-111">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="45180-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="45180-112">Tipo di indirizzo, ad esempio indirizzo IP del tipo di indirizzo \_ \_ Ethernet o indirizzo \_ \_ IP.</span><span class="sxs-lookup"><span data-stu-id="45180-112">A type of address, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="45180-113">*Flag*</span><span class="sxs-lookup"><span data-stu-id="45180-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="45180-114">Flag utilizzati per modificare i dati dell'indirizzo di destinazione restituiti.</span><span class="sxs-lookup"><span data-stu-id="45180-114">The flags used to modify returned destination address data.</span></span>



| <span data-ttu-id="45180-115">Valore</span><span class="sxs-lookup"><span data-stu-id="45180-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="45180-116">Significato</span><span class="sxs-lookup"><span data-stu-id="45180-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="45180-117"><dt>**ADDRESSTYPE i \_ flag \_ normalizzati**</dt></span><span class="sxs-lookup"><span data-stu-id="45180-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="45180-118">Annulla il routing e i bit del gruppo.</span><span class="sxs-lookup"><span data-stu-id="45180-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="45180-119"><dt>**ADDRESSTYPE \_ flag di \_ bit \_ inverso**</dt></span><span class="sxs-lookup"><span data-stu-id="45180-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="45180-120">Converte gli indirizzi di rete dell'anello di token al normale.</span><span class="sxs-lookup"><span data-stu-id="45180-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45180-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45180-121">Return value</span></span>

<span data-ttu-id="45180-122">Se la funzione ha esito positivo, il valore *lpAddress* è valido e il valore restituito è BHERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="45180-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="45180-123">Se la funzione ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="45180-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="45180-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="45180-124">Return code</span></span>                                                                                                | <span data-ttu-id="45180-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45180-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45180-126"><dt>**il \_ protocollo BHERR non è stato \_ \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="45180-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="45180-127">Il protocollo specificato nel parametro *addressType* non è valido per il frame.</span><span class="sxs-lookup"><span data-stu-id="45180-127">The specified protocol in the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="45180-128"><dt>**\_HFRAME BHERR non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="45180-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="45180-129">Il valore *hFrame* non è valido.</span><span class="sxs-lookup"><span data-stu-id="45180-129">The *hFrame* value is invalid.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="45180-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="45180-130">Remarks</span></span>

<span data-ttu-id="45180-131">Il tipo di indirizzo trova il tipo di indirizzo **\_ \_ \_ più alto** è consentito.</span><span class="sxs-lookup"><span data-stu-id="45180-131">The **ADDRESS\_TYPE\_FIND\_HIGHEST** address type is allowed.</span></span> <span data-ttu-id="45180-132">Quando viene usato questo tipo di indirizzo, la funzione Cerca l'indirizzo IP IPX, XNS, IP o VINES prima di restituire l'indirizzo ETHERNET, TOKENRING o FDDI.</span><span class="sxs-lookup"><span data-stu-id="45180-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="45180-133">Questo approccio è utile per i protocolli e gli ambienti in cui è possibile multiplexare due schede di rete in un unico indirizzo del server.</span><span class="sxs-lookup"><span data-stu-id="45180-133">This approach is useful for protocols and in environments where two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="45180-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45180-134">Requirements</span></span>



| <span data-ttu-id="45180-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="45180-135">Requirement</span></span> | <span data-ttu-id="45180-136">Valore</span><span class="sxs-lookup"><span data-stu-id="45180-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="45180-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45180-137">Minimum supported client</span></span><br/> | <span data-ttu-id="45180-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="45180-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="45180-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45180-139">Minimum supported server</span></span><br/> | <span data-ttu-id="45180-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="45180-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="45180-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45180-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="45180-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="45180-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="45180-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="45180-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="45180-144"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45180-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="45180-145">DLL</span><span class="sxs-lookup"><span data-stu-id="45180-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45180-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45180-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





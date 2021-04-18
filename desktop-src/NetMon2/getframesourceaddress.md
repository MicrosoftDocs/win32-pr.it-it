---
description: Recupera l'indirizzo di origine di un frame.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: Funzione GetFrameSourceAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6939e5875c4d2f6f41ae33574c7a7240697042ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305902"
---
# <a name="getframesourceaddress-function"></a><span data-ttu-id="63523-103">GetFrameSourceAddress (funzione)</span><span class="sxs-lookup"><span data-stu-id="63523-103">GetFrameSourceAddress function</span></span>

<span data-ttu-id="63523-104">La funzione **GetFrameSourceAddress** recupera l'indirizzo di origine di un frame.</span><span class="sxs-lookup"><span data-stu-id="63523-104">The **GetFrameSourceAddress** function retrieves the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="63523-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63523-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSourceAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="63523-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="63523-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63523-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="63523-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="63523-108">Handle per il frame per il quale ottenere un puntatore.</span><span class="sxs-lookup"><span data-stu-id="63523-108">A handle to the frame for which to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="63523-109">*lpAddress*</span><span class="sxs-lookup"><span data-stu-id="63523-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="63523-110">Buffer restituito che archivia l'indirizzo di origine del frame.</span><span class="sxs-lookup"><span data-stu-id="63523-110">A return buffer that stores the frame source address.</span></span>

</dd> <dt>

<span data-ttu-id="63523-111">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="63523-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="63523-112">Tipo di indirizzo cercato, ad esempio indirizzo IP del tipo di indirizzo \_ \_ Ethernet o indirizzo \_ \_ IP.</span><span class="sxs-lookup"><span data-stu-id="63523-112">The type of address searched for, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="63523-113">*Flag*</span><span class="sxs-lookup"><span data-stu-id="63523-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="63523-114">Flag utilizzati per modificare i dati dell'indirizzo di origine restituiti.</span><span class="sxs-lookup"><span data-stu-id="63523-114">The flags used to modify returned source address data.</span></span>



| <span data-ttu-id="63523-115">Valore</span><span class="sxs-lookup"><span data-stu-id="63523-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="63523-116">Significato</span><span class="sxs-lookup"><span data-stu-id="63523-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="63523-117"><dt>**ADDRESSTYPE i \_ flag \_ normalizzati**</dt></span><span class="sxs-lookup"><span data-stu-id="63523-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="63523-118">Annulla il routing e i bit del gruppo.</span><span class="sxs-lookup"><span data-stu-id="63523-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="63523-119"><dt>**ADDRESSTYPE \_ flag di \_ bit \_ inverso**</dt></span><span class="sxs-lookup"><span data-stu-id="63523-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="63523-120">Converte gli indirizzi di rete dell'anello di token al normale.</span><span class="sxs-lookup"><span data-stu-id="63523-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63523-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63523-121">Return value</span></span>

<span data-ttu-id="63523-122">Se la funzione ha esito positivo, il valore *lpAddress* è valido e il valore restituito è BHERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="63523-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="63523-123">Se la funzione ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="63523-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="63523-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="63523-124">Return code</span></span>                                                                                                | <span data-ttu-id="63523-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63523-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63523-126"><dt>**il \_ protocollo BHERR non è stato \_ \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="63523-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="63523-127">Il protocollo specificato dal parametro *addressType* non è valido per il frame.</span><span class="sxs-lookup"><span data-stu-id="63523-127">The protocol specified by the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="63523-128"><dt>**\_HFRAME BHERR non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63523-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="63523-129">Il valore del parametro *hFrame* non è valido.</span><span class="sxs-lookup"><span data-stu-id="63523-129">The *hFrame* parameter value is invalid.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="63523-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="63523-130">Remarks</span></span>

<span data-ttu-id="63523-131">È consentito un tipo di indirizzo di **\_ tipo indirizzo \_ \_ maggiore** .</span><span class="sxs-lookup"><span data-stu-id="63523-131">An address type of **ADDRESS\_TYPE\_FIND\_HIGHEST** is allowed.</span></span> <span data-ttu-id="63523-132">Quando viene usato questo tipo di indirizzo, la funzione Cerca l'indirizzo IP IPX, XNS, IP o VINES prima di restituire l'indirizzo ETHERNET, TOKENRING o FDDI.</span><span class="sxs-lookup"><span data-stu-id="63523-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="63523-133">Questo approccio è utile per i protocolli e gli ambienti in cui è possibile multiplexare due schede di rete in un unico indirizzo del server.</span><span class="sxs-lookup"><span data-stu-id="63523-133">This approach is useful for protocols and environments in which two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="63523-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63523-134">Requirements</span></span>



| <span data-ttu-id="63523-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="63523-135">Requirement</span></span> | <span data-ttu-id="63523-136">Valore</span><span class="sxs-lookup"><span data-stu-id="63523-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="63523-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63523-137">Minimum supported client</span></span><br/> | <span data-ttu-id="63523-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="63523-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="63523-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63523-139">Minimum supported server</span></span><br/> | <span data-ttu-id="63523-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="63523-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="63523-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63523-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="63523-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="63523-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="63523-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="63523-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="63523-144"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63523-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="63523-145">DLL</span><span class="sxs-lookup"><span data-stu-id="63523-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63523-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63523-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





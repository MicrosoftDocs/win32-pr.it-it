---
description: Restituisce l'offset di un protocollo specificato nel frame.
ms.assetid: bfe5f477-c9de-4bb9-99e5-b8db895b0ae6
title: Funzione GetProtocolStartOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ff760c4a61cb39ba897351d706c39d240389bf49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305896"
---
# <a name="getprotocolstartoffset-function"></a><span data-ttu-id="b339e-103">GetProtocolStartOffset (funzione)</span><span class="sxs-lookup"><span data-stu-id="b339e-103">GetProtocolStartOffset function</span></span>

<span data-ttu-id="b339e-104">La funzione **GetProtocolStartOffset** restituisce l'offset di un protocollo specificato nel frame.</span><span class="sxs-lookup"><span data-stu-id="b339e-104">The **GetProtocolStartOffset** function returns the offset of a specified protocol in the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="b339e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b339e-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffset(
   HFRAME hFrame,
   LPSTR  ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="b339e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b339e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b339e-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="b339e-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="b339e-108">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="b339e-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="b339e-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="b339e-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="b339e-110">Nome del protocollo, ad esempio TCP.</span><span class="sxs-lookup"><span data-stu-id="b339e-110">The Protocol name, such as TCP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b339e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b339e-111">Return value</span></span>

<span data-ttu-id="b339e-112">Se la funzione ha esito positivo, il valore restituito è un offset **DWORD** all'inizio del protocollo in cui viene eseguita la ricerca di un valore restituito pari a zero indica che il protocollo è il primo protocollo nel frame.</span><span class="sxs-lookup"><span data-stu-id="b339e-112">If the function is successful, the return value is a **DWORD** offset to the beginning of the protocol being searched for   a return value of zero indicates the protocol is the first protocol in the frame.</span></span>

<span data-ttu-id="b339e-113">Se la funzione ha esito negativo, il protocollo non si trova nel frame, il valore restituito è-1.</span><span class="sxs-lookup"><span data-stu-id="b339e-113">If the function is unsuccessful, the protocol is not in the frame, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="b339e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b339e-114">Remarks</span></span>

<span data-ttu-id="b339e-115">Quando viene fornito l'handle a un frame, questa funzione restituisce l'offset a un protocollo specificato nel frame.</span><span class="sxs-lookup"><span data-stu-id="b339e-115">When given the handle to a frame, this function returns the offset to a specified protocol in the frame.</span></span> <span data-ttu-id="b339e-116">Per determinare, ad esempio, se il frame è un frame DNS, il parser DNS richiede l'indirizzo di porta del protocollo TCP.</span><span class="sxs-lookup"><span data-stu-id="b339e-116">For example, to determine whether the frame is a DNS frame, the DNS parser requires the port address of the TCP protocol.</span></span> <span data-ttu-id="b339e-117">Il parser DNS chiamerà questa funzione con TCP come valore *ProtocolName* .</span><span class="sxs-lookup"><span data-stu-id="b339e-117">The DNS parser would call this function with TCP as the *ProtocolName* value.</span></span> <span data-ttu-id="b339e-118">Se il frame viene riconosciuto dal protocollo TCP, viene restituito l'offset delle **parole** dall'inizio del frame all'inizio del frame TCP.</span><span class="sxs-lookup"><span data-stu-id="b339e-118">If the frame is recognized by the TCP protocol, the **WORD** offset from the beginning of the frame to the beginning of the TCP frame is returned.</span></span> <span data-ttu-id="b339e-119">Se non è presente alcun protocollo TCP, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="b339e-119">If there is no TCP protocol, the return value is zero.</span></span>

<span data-ttu-id="b339e-120">Questa funzione trova l'inizio di un protocollo in un frame.</span><span class="sxs-lookup"><span data-stu-id="b339e-120">This function finds the beginning of a protocol in a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="b339e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b339e-121">Requirements</span></span>



| <span data-ttu-id="b339e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b339e-122">Requirement</span></span> | <span data-ttu-id="b339e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b339e-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b339e-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b339e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b339e-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b339e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b339e-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b339e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b339e-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b339e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b339e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b339e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b339e-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b339e-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b339e-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="b339e-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b339e-131"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b339e-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b339e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b339e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b339e-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b339e-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





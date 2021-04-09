---
description: La funzione GetProtocolFromTable restituisce un handle a un protocollo&\# 8212; in base a una tabella e a un valore di continuità specificati.
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: Funzione GetProtocolFromTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 498892fc2cc5ada2e177b8fb3f70f40a1ef10dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966461"
---
# <a name="getprotocolfromtable-function"></a><span data-ttu-id="2cac0-103">GetProtocolFromTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="2cac0-103">GetProtocolFromTable function</span></span>

<span data-ttu-id="2cac0-104">La funzione **GetProtocolFromTable** restituisce un handle a un protocollo basato su una tabella e un valore di continuità specificati.</span><span class="sxs-lookup"><span data-stu-id="2cac0-104">The **GetProtocolFromTable** function returns a handle to a protocol based on a given handoff table and value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cac0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cac0-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromTable(
  _In_  LPHANDOFFTABLE hTable,
  _In_  DWORD          ItemToFind,
  _Out_ PDWORD_PTR     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="2cac0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2cac0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cac0-107">*hTable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2cac0-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cac0-108">Handle per una tabella con continuità.</span><span class="sxs-lookup"><span data-stu-id="2cac0-108">Handle to a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="2cac0-109">*ItemToFind* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2cac0-109">*ItemToFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cac0-110">Valore utilizzato per individuare il protocollo in una tabella con continuità.</span><span class="sxs-lookup"><span data-stu-id="2cac0-110">Value used to locate the protocol in a handoff table.</span></span> <span data-ttu-id="2cac0-111">Il valore deve essere disponibile nei dati del protocollo.</span><span class="sxs-lookup"><span data-stu-id="2cac0-111">The value must be available in the protocol data.</span></span>

</dd> <dt>

<span data-ttu-id="2cac0-112">*lpInstData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2cac0-112">*lpInstData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cac0-113">Se disponibile nella tabella uniforme, i dati dell'istanza per il protocollo successivo.</span><span class="sxs-lookup"><span data-stu-id="2cac0-113">If available in the handoff table, instance data for the next protocol.</span></span> <span data-ttu-id="2cac0-114">I dati dell'istanza non possono essere più lunghi di un \_ ptr DWORD di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="2cac0-114">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cac0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2cac0-115">Return value</span></span>

<span data-ttu-id="2cac0-116">Se la funzione ha esito positivo, il valore restituito è un handle del protocollo.</span><span class="sxs-lookup"><span data-stu-id="2cac0-116">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="2cac0-117">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="2cac0-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cac0-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cac0-118">Remarks</span></span>

<span data-ttu-id="2cac0-119">Quando si implementa la funzione di esportazione [RecognizeFrame](recognizeframe.md) , viene utilizzata la funzione **GetProtocolFromTable** per ottenere un handle per il protocollo successivo.</span><span class="sxs-lookup"><span data-stu-id="2cac0-119">When implementing the [RecognizeFrame](recognizeframe.md) export function, the **GetProtocolFromTable** function is used to obtain a handle to the next protocol.</span></span> <span data-ttu-id="2cac0-120">La funzione **GetProtocolFromTable** viene chiamata per recuperare un handle dal protocollo successivo se il protocollo identifica il protocollo che segue.</span><span class="sxs-lookup"><span data-stu-id="2cac0-120">The **GetProtocolFromTable** function is called to retrieve a handle from the next protocol if the protocol identifies which protocol follows.</span></span>

<span data-ttu-id="2cac0-121">**Dati dell'istanza**</span><span class="sxs-lookup"><span data-stu-id="2cac0-121">**Instance data**</span></span>

<span data-ttu-id="2cac0-122">I dati dell'istanza possono essere dati di lunghezza minore o uguale a un \_ ptr DWORD o un puntatore ai dati, ad esempio dati di frame non elaborati, che non devono essere allocati o liberati dal parser.</span><span class="sxs-lookup"><span data-stu-id="2cac0-122">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cac0-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cac0-123">Requirements</span></span>



| <span data-ttu-id="2cac0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cac0-124">Requirement</span></span> | <span data-ttu-id="2cac0-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2cac0-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2cac0-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cac0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2cac0-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2cac0-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2cac0-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cac0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2cac0-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2cac0-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2cac0-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2cac0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cac0-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cac0-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2cac0-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="2cac0-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="2cac0-133"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cac0-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2cac0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2cac0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cac0-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cac0-135"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cac0-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cac0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cac0-137">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="2cac0-137">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 





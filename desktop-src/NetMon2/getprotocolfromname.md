---
description: La funzione GetProtocolFromName restituisce un handle per un protocollo di un nome specificato.
ms.assetid: 18f5a9a7-4245-479d-a0da-2ede362a60b8
title: Funzione GetProtocolFromName (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e104c066be2a5465083c7983aaefebd46f548b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750074"
---
# <a name="getprotocolfromname-function"></a><span data-ttu-id="9dbbd-103">GetProtocolFromName (funzione)</span><span class="sxs-lookup"><span data-stu-id="9dbbd-103">GetProtocolFromName function</span></span>

<span data-ttu-id="9dbbd-104">La funzione **GetProtocolFromName** restituisce un handle per un protocollo di un nome specificato.</span><span class="sxs-lookup"><span data-stu-id="9dbbd-104">The **GetProtocolFromName** function returns a handle to a protocol of a given name.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dbbd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9dbbd-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromName(
  _In_ LPSTR ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="9dbbd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9dbbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dbbd-107">*ProtocolName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dbbd-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dbbd-108">Nome del protocollo (ad esempio, IP).</span><span class="sxs-lookup"><span data-stu-id="9dbbd-108">Protocol name (for example, IP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dbbd-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9dbbd-109">Return value</span></span>

<span data-ttu-id="9dbbd-110">Se la funzione ha esito positivo, il valore restituito è un handle del protocollo.</span><span class="sxs-lookup"><span data-stu-id="9dbbd-110">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="9dbbd-111">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="9dbbd-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dbbd-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9dbbd-112">Remarks</span></span>

<span data-ttu-id="9dbbd-113">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetProtocolFromName** .</span><span class="sxs-lookup"><span data-stu-id="9dbbd-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolFromName** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dbbd-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9dbbd-114">Requirements</span></span>



| <span data-ttu-id="9dbbd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dbbd-115">Requirement</span></span> | <span data-ttu-id="9dbbd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9dbbd-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9dbbd-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dbbd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9dbbd-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9dbbd-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9dbbd-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dbbd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9dbbd-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9dbbd-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9dbbd-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9dbbd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dbbd-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dbbd-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9dbbd-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="9dbbd-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9dbbd-124"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9dbbd-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9dbbd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9dbbd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dbbd-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dbbd-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





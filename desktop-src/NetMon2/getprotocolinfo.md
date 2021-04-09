---
description: La funzione GetProtocolInfo restituisce un puntatore a un valore di informazioni sul protocollo.
ms.assetid: 1ba47889-b2ed-47ba-94f9-1b781af6d01f
title: Funzione GetProtocolInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2ec9fb58957c2e0fd64bc1c5878892fe6542af8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966460"
---
# <a name="getprotocolinfo-function"></a><span data-ttu-id="093b2-103">GetProtocolInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="093b2-103">GetProtocolInfo function</span></span>

<span data-ttu-id="093b2-104">La funzione **GetProtocolInfo** restituisce un puntatore a un valore di informazioni sul protocollo.</span><span class="sxs-lookup"><span data-stu-id="093b2-104">The **GetProtocolInfo** function returns a pointer to a protocol information value.</span></span>

## <a name="syntax"></a><span data-ttu-id="093b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="093b2-105">Syntax</span></span>


```C++
LPPROTOCOLINFO WINAPI GetProtocolInfo(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="093b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="093b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="093b2-107">*hProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="093b2-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="093b2-108">Handle per un protocollo.</span><span class="sxs-lookup"><span data-stu-id="093b2-108">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="093b2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="093b2-109">Return value</span></span>

<span data-ttu-id="093b2-110">Se la funzione ha esito positivo, il valore restituito è un puntatore al valore delle informazioni sul protocollo.</span><span class="sxs-lookup"><span data-stu-id="093b2-110">If the function is successful, the return value is a pointer to the protocol information value.</span></span>

<span data-ttu-id="093b2-111">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="093b2-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="093b2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="093b2-112">Remarks</span></span>

<span data-ttu-id="093b2-113">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetProtocolInfo** .</span><span class="sxs-lookup"><span data-stu-id="093b2-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="093b2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="093b2-114">Requirements</span></span>



| <span data-ttu-id="093b2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="093b2-115">Requirement</span></span> | <span data-ttu-id="093b2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="093b2-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="093b2-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="093b2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="093b2-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="093b2-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="093b2-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="093b2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="093b2-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="093b2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="093b2-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="093b2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="093b2-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="093b2-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="093b2-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="093b2-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="093b2-124"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="093b2-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="093b2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="093b2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="093b2-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="093b2-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





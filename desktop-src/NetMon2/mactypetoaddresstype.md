---
description: La funzione MacTypeToAddressType converte un tipo MAC specificato in un tipo di indirizzo.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: Funzione MacTypeToAddressType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879502"
---
# <a name="mactypetoaddresstype-function"></a><span data-ttu-id="7364f-103">MacTypeToAddressType (funzione)</span><span class="sxs-lookup"><span data-stu-id="7364f-103">MacTypeToAddressType function</span></span>

<span data-ttu-id="7364f-104">La funzione **MacTypeToAddressType** converte un tipo Mac specificato in un tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="7364f-104">The **MacTypeToAddressType** function converts a given MAC type to an address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7364f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7364f-105">Syntax</span></span>


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a><span data-ttu-id="7364f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7364f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7364f-107">*MacType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7364f-107">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7364f-108">Tipo MAC da convertire.</span><span class="sxs-lookup"><span data-stu-id="7364f-108">MAC type to be converted.</span></span> <span data-ttu-id="7364f-109">Specificare uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="7364f-109">Specify one of the following values:</span></span>

<span data-ttu-id="7364f-110">tipo \_ Mac \_ Ethernet Mac \_ digitare \_ Tokenring Mac \_ tipo \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="7364f-110">MAC\_TYPE\_ETHERNET MAC\_TYPE\_TOKENRING MAC\_TYPE\_FDDI</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7364f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7364f-111">Return value</span></span>

<span data-ttu-id="7364f-112">Se la funzione ha esito positivo, il valore restituito è uno dei seguenti tipi di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="7364f-112">If the function is successful, the return value is one of the following address types.</span></span>

<span data-ttu-id="7364f-113">tipo di indirizzo Ethernet tipo indirizzo Tokenring tipo di indirizzo \_ \_ \_ \_ \_ \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="7364f-113">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI</span></span>

<span data-ttu-id="7364f-114">Se la funzione ha esito negativo, il tipo MAC è sconosciuto, il valore restituito è-1.</span><span class="sxs-lookup"><span data-stu-id="7364f-114">If the function is unsuccessful, the MAC type is unknown, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="7364f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7364f-115">Remarks</span></span>

<span data-ttu-id="7364f-116">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **MacTypeToAddressType** .</span><span class="sxs-lookup"><span data-stu-id="7364f-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **MacTypeToAddressType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7364f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7364f-117">Requirements</span></span>



| <span data-ttu-id="7364f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7364f-118">Requirement</span></span> | <span data-ttu-id="7364f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7364f-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7364f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7364f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7364f-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7364f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7364f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7364f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7364f-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7364f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7364f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7364f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7364f-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7364f-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7364f-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="7364f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="7364f-127"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7364f-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7364f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7364f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7364f-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7364f-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





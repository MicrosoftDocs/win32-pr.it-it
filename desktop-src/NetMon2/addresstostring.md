---
description: La funzione AddressToString converte un indirizzo in una stringa.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: Funzione AddressToString (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddressToString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0c7c659a05167055b18c36e5c6c36465538af483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131995"
---
# <a name="addresstostring-function"></a><span data-ttu-id="982f5-103">AddressToString (funzione)</span><span class="sxs-lookup"><span data-stu-id="982f5-103">AddressToString function</span></span>

<span data-ttu-id="982f5-104">La funzione **AddressToString** converte un indirizzo in una stringa.</span><span class="sxs-lookup"><span data-stu-id="982f5-104">The **AddressToString** function converts an address into a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="982f5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="982f5-105">Syntax</span></span>


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="982f5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="982f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="982f5-107">*stringa* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="982f5-107">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="982f5-108">Stringa in cui viene convertito l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="982f5-108">String that the address is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="982f5-109">*lpAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="982f5-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="982f5-110">Indirizzo stampato.</span><span class="sxs-lookup"><span data-stu-id="982f5-110">The address that is printed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="982f5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="982f5-111">Return value</span></span>

<span data-ttu-id="982f5-112">Il valore restituito è un puntatore alla stringa convertita.</span><span class="sxs-lookup"><span data-stu-id="982f5-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="982f5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="982f5-113">Requirements</span></span>



| <span data-ttu-id="982f5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="982f5-114">Requirement</span></span> | <span data-ttu-id="982f5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="982f5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="982f5-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="982f5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="982f5-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="982f5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="982f5-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="982f5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="982f5-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="982f5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="982f5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="982f5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="982f5-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="982f5-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="982f5-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="982f5-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="982f5-123"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="982f5-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="982f5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="982f5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="982f5-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="982f5-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 





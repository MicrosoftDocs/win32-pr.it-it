---
description: La funzione StringToAddress converte una stringa in un indirizzo.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: Funzione StringToAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 70a9e6b42359a2f73fba55194c9b6e6e21ffa9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310478"
---
# <a name="stringtoaddress-function"></a><span data-ttu-id="19366-103">StringToAddress (funzione)</span><span class="sxs-lookup"><span data-stu-id="19366-103">StringToAddress function</span></span>

<span data-ttu-id="19366-104">La funzione **StringToAddress** converte una stringa in un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="19366-104">The **StringToAddress** function converts a string to an address.</span></span>

## <a name="syntax"></a><span data-ttu-id="19366-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19366-105">Syntax</span></span>


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a><span data-ttu-id="19366-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="19366-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19366-107">*lpAddress* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19366-107">*lpAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19366-108">Puntatore all'indirizzo in cui la stringa viene convertita.</span><span class="sxs-lookup"><span data-stu-id="19366-108">Pointer to the address the string is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="19366-109">*stringa* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="19366-109">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19366-110">Stringa convertita in un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="19366-110">String that is converted to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19366-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19366-111">Return value</span></span>

<span data-ttu-id="19366-112">Il valore restituito è un puntatore alla stringa convertita.</span><span class="sxs-lookup"><span data-stu-id="19366-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="19366-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19366-113">Requirements</span></span>



| <span data-ttu-id="19366-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="19366-114">Requirement</span></span> | <span data-ttu-id="19366-115">Valore</span><span class="sxs-lookup"><span data-stu-id="19366-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19366-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19366-116">Minimum supported client</span></span><br/> | <span data-ttu-id="19366-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="19366-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="19366-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19366-118">Minimum supported server</span></span><br/> | <span data-ttu-id="19366-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="19366-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19366-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19366-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="19366-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="19366-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="19366-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="19366-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="19366-123"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19366-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="19366-124">DLL</span><span class="sxs-lookup"><span data-stu-id="19366-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19366-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19366-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 





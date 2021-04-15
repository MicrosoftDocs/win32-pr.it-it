---
description: Restituisce una stringa che si trova in una posizione specificata all'interno di un BLOB.
ms.assetid: 5930a30b-f0ed-4d5b-a0ba-6cead55c2fcd
title: Funzione GetStringFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 475600fb6128b5dbbaf9333f8c550351831f0a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484324"
---
# <a name="getstringfromblob-function"></a><span data-ttu-id="b7af9-103">GetStringFromBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="b7af9-103">GetStringFromBlob function</span></span>

<span data-ttu-id="b7af9-104">La funzione **GetStringFromBlob** restituisce una stringa che si trova in una posizione specificata all'interno di un BLOB.</span><span class="sxs-lookup"><span data-stu-id="b7af9-104">The **GetStringFromBlob** function returns a string located at a given position within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7af9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7af9-105">Syntax</span></span>


```C++
DWORD GetStringFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_ const char  **ppString
);
```



## <a name="parameters"></a><span data-ttu-id="b7af9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7af9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7af9-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7af9-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7af9-108">Handle per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="b7af9-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="b7af9-109">*pOwnerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7af9-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7af9-110">Sezione del **proprietario** del BLOB in cui si trova la stringa.</span><span class="sxs-lookup"><span data-stu-id="b7af9-110">A BLOB **Owner** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="b7af9-111">*pCategoryName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7af9-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7af9-112">Sezione di **categoria** BLOB in cui si trova la stringa.</span><span class="sxs-lookup"><span data-stu-id="b7af9-112">A BLOB **Category** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="b7af9-113">*pTagName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7af9-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7af9-114">**Tag** della stringa richiesta.</span><span class="sxs-lookup"><span data-stu-id="b7af9-114">The **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="b7af9-115">*ppString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b7af9-115">*ppString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7af9-116">Puntatore a una variabile che punta alla stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="b7af9-116">A pointer to a variable that points to the returned string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7af9-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7af9-117">Return value</span></span>

<span data-ttu-id="b7af9-118">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b7af9-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b7af9-119">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="b7af9-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

<span data-ttu-id="b7af9-120">Se il **proprietario**, la **categoria** o i dati del **tag** specificati non esiste, la funzione restituisce la **voce del BLOB NMERR non \_ \_ \_ \_ \_ esiste**.</span><span class="sxs-lookup"><span data-stu-id="b7af9-120">If the specified **Owner**, **Category**, or **Tag** data does not exist, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7af9-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7af9-121">Requirements</span></span>



| <span data-ttu-id="b7af9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7af9-122">Requirement</span></span> | <span data-ttu-id="b7af9-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b7af9-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7af9-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7af9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b7af9-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b7af9-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b7af9-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7af9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b7af9-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b7af9-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b7af9-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7af9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7af9-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7af9-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="b7af9-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="b7af9-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7af9-131"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7af9-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="b7af9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b7af9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7af9-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7af9-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7af9-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7af9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7af9-135">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="b7af9-135">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="b7af9-136">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="b7af9-136">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="b7af9-137">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="b7af9-137">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="b7af9-138">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="b7af9-138">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="b7af9-139">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="b7af9-139">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="b7af9-140">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="b7af9-140">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="b7af9-141">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="b7af9-141">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="b7af9-142">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="b7af9-142">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="b7af9-143">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="b7af9-143">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="b7af9-144">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="b7af9-144">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 





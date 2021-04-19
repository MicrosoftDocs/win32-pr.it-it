---
description: La funzione GetNetworkInfoFromBlob recupera le informazioni di rete da un BLOB specificato.
ms.assetid: 217c33f4-e548-4072-9edd-ded61e6cd743
title: Funzione GetNetworkInfoFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNetworkInfoFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2f8b15dce010febdc952c2527a9f4ad31054fa3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319949"
---
# <a name="getnetworkinfofromblob-function"></a><span data-ttu-id="21850-103">GetNetworkInfoFromBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="21850-103">GetNetworkInfoFromBlob function</span></span>

<span data-ttu-id="21850-104">La funzione **GetNetworkInfoFromBlob** recupera le informazioni di rete da un blob specificato.</span><span class="sxs-lookup"><span data-stu-id="21850-104">The **GetNetworkInfoFromBlob** function retrieves network information from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="21850-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21850-105">Syntax</span></span>


```C++
DWORD GetNetworkInfoFromBlob(
  _In_    HBLOB         hBlob,
  _Inout_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="21850-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="21850-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21850-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21850-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21850-108">Handle per un BLOB.</span><span class="sxs-lookup"><span data-stu-id="21850-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="21850-109">*lpNetworkInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="21850-109">*lpNetworkInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="21850-110">Puntatore alla struttura [NETWORKINFO](networkinfo.md) allocata dall'utente compilata.</span><span class="sxs-lookup"><span data-stu-id="21850-110">A pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that is filled in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21850-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21850-111">Return value</span></span>

<span data-ttu-id="21850-112">Se la funzione **GetNetworkInfoFromBlob** ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="21850-112">If the **GetNetworkInfoFromBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="21850-113">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.</span><span class="sxs-lookup"><span data-stu-id="21850-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="21850-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="21850-114">Remarks</span></span>

<span data-ttu-id="21850-115">Le informazioni di rete vengono archiviate nella sezione BLOB **networkInfo** della categoria BLOB NPP **owner** .</span><span class="sxs-lookup"><span data-stu-id="21850-115">The network information is stored in the BLOB **NetworkInfo** section of the BLOB NPP **Owner** category.</span></span>

## <a name="requirements"></a><span data-ttu-id="21850-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21850-116">Requirements</span></span>



| <span data-ttu-id="21850-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="21850-117">Requirement</span></span> | <span data-ttu-id="21850-118">Valore</span><span class="sxs-lookup"><span data-stu-id="21850-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21850-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21850-119">Minimum supported client</span></span><br/> | <span data-ttu-id="21850-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="21850-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="21850-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21850-121">Minimum supported server</span></span><br/> | <span data-ttu-id="21850-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="21850-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="21850-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21850-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="21850-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="21850-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="21850-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="21850-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="21850-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21850-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="21850-127">DLL</span><span class="sxs-lookup"><span data-stu-id="21850-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21850-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21850-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21850-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21850-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21850-130">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="21850-130">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="21850-131">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="21850-131">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="21850-132">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="21850-132">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="21850-133">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="21850-133">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="21850-134">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="21850-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="21850-135">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="21850-135">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="21850-136">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="21850-136">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="21850-137">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="21850-137">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="21850-138">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="21850-138">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="21850-139">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="21850-139">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 





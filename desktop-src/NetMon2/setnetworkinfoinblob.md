---
description: La funzione SetNetworkInfoInBlob compila la struttura NETWORKINFO nel BLOB.
ms.assetid: 1a511c26-2fa7-4fe4-a5a9-23188c59bc34
title: Funzione SetNetworkInfoInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNetworkInfoInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a0019bfaf802b5d4dc80d73e75affa3c50d95de1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314749"
---
# <a name="setnetworkinfoinblob-function"></a><span data-ttu-id="3ab29-103">SetNetworkInfoInBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="3ab29-103">SetNetworkInfoInBlob function</span></span>

<span data-ttu-id="3ab29-104">La funzione **SetNetworkInfoInBlob** compila la struttura **NETWORKINFO** nel BLOB.</span><span class="sxs-lookup"><span data-stu-id="3ab29-104">The **SetNetworkInfoInBlob** function fills in the **NETWORKINFO** structure in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ab29-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ab29-105">Syntax</span></span>


```C++
DWORD SetNetworkInfoInBlob(
  _In_ HBLOB         hBlob,
  _In_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3ab29-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ab29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ab29-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ab29-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ab29-108">Handle per un BLOB.</span><span class="sxs-lookup"><span data-stu-id="3ab29-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="3ab29-109">*lpNetworkInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ab29-109">*lpNetworkInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ab29-110">Puntatore alla struttura [NETWORKINFO](networkinfo.md) allocata dall'utente che la funzione compila.</span><span class="sxs-lookup"><span data-stu-id="3ab29-110">Pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that the function fills in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ab29-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ab29-111">Return value</span></span>

<span data-ttu-id="3ab29-112">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3ab29-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3ab29-113">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="3ab29-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ab29-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ab29-114">Requirements</span></span>



| <span data-ttu-id="3ab29-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ab29-115">Requirement</span></span> | <span data-ttu-id="3ab29-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3ab29-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab29-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ab29-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3ab29-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3ab29-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3ab29-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ab29-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3ab29-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3ab29-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ab29-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ab29-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ab29-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ab29-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3ab29-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="3ab29-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ab29-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ab29-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3ab29-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3ab29-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ab29-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ab29-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ab29-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ab29-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ab29-128">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="3ab29-128">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="3ab29-129">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="3ab29-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="3ab29-130">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="3ab29-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="3ab29-131">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="3ab29-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="3ab29-132">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="3ab29-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="3ab29-133">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="3ab29-133">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="3ab29-134">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="3ab29-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="3ab29-135">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="3ab29-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="3ab29-136">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="3ab29-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 





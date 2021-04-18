---
description: La funzione SetClassIDInBlob imposta il valore dell'identificatore di classe denominato di un BLOB.
ms.assetid: d17dd48b-2e35-4c57-ba33-688180910b63
title: Funzione SetClassIDInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetClassIDInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b617c39767038bac51d749a640ebcf2301e0c63f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310488"
---
# <a name="setclassidinblob-function"></a><span data-ttu-id="01557-103">SetClassIDInBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="01557-103">SetClassIDInBlob function</span></span>

<span data-ttu-id="01557-104">La funzione **SetClassIDInBlob** imposta il valore dell'identificatore di classe denominato di un BLOB.</span><span class="sxs-lookup"><span data-stu-id="01557-104">The **SetClassIDInBlob** function sets the named class identifier value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="01557-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01557-105">Syntax</span></span>


```C++
DWORD SetClassIDInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="01557-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="01557-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01557-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01557-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01557-108">Handle per un BLOB.</span><span class="sxs-lookup"><span data-stu-id="01557-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="01557-109">*pOwnerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01557-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01557-110">Puntatore al nome del **proprietario** del BLOB impostato.</span><span class="sxs-lookup"><span data-stu-id="01557-110">Pointer to the BLOB **Owner** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="01557-111">*pCategoryName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01557-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01557-112">Puntatore al nome della **categoria** BLOB impostato.</span><span class="sxs-lookup"><span data-stu-id="01557-112">Pointer to the BLOB **Category** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="01557-113">*pTagName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01557-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01557-114">Puntatore al nome del **tag** BLOB impostato.</span><span class="sxs-lookup"><span data-stu-id="01557-114">Pointer to the BLOB **Tag** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="01557-115">*pClsID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01557-115">*pClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01557-116">Puntatore all'identificatore di classe del BLOB impostato.</span><span class="sxs-lookup"><span data-stu-id="01557-116">Pointer to the class identifier of the BLOB that is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01557-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01557-117">Return value</span></span>

<span data-ttu-id="01557-118">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="01557-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="01557-119">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="01557-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="01557-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01557-120">Requirements</span></span>



| <span data-ttu-id="01557-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="01557-121">Requirement</span></span> | <span data-ttu-id="01557-122">Valore</span><span class="sxs-lookup"><span data-stu-id="01557-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01557-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01557-123">Minimum supported client</span></span><br/> | <span data-ttu-id="01557-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01557-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="01557-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01557-125">Minimum supported server</span></span><br/> | <span data-ttu-id="01557-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01557-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="01557-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01557-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="01557-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="01557-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="01557-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="01557-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="01557-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01557-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="01557-131">DLL</span><span class="sxs-lookup"><span data-stu-id="01557-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01557-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01557-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01557-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01557-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01557-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="01557-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="01557-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="01557-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="01557-136">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="01557-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="01557-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="01557-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="01557-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="01557-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="01557-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="01557-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="01557-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="01557-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="01557-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="01557-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="01557-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="01557-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 





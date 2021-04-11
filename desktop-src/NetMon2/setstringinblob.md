---
description: Imposta una stringa in una posizione specificata all'interno di un BLOB.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: Funzione SetStringInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetStringInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 37278b9111818957e6d5fb3032f1bf33ad3a6ec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226236"
---
# <a name="setstringinblob-function"></a><span data-ttu-id="41937-103">SetStringInBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="41937-103">SetStringInBlob function</span></span>

<span data-ttu-id="41937-104">La funzione **SetStringInBlob** imposta una stringa in una posizione specificata all'interno di un BLOB.</span><span class="sxs-lookup"><span data-stu-id="41937-104">The **SetStringInBlob** function sets a string at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="41937-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41937-105">Syntax</span></span>


```C++
DWORD SetStringInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const char  *pString
);
```



## <a name="parameters"></a><span data-ttu-id="41937-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41937-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41937-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41937-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41937-108">Handle per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="41937-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="41937-109">*pOwnerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41937-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41937-110">Puntatore alla sezione **owner** del BLOB, in cui è impostata la stringa.</span><span class="sxs-lookup"><span data-stu-id="41937-110">A pointer to the **Owner** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="41937-111">*pCategoryName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41937-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41937-112">Puntatore alla sezione **Category** del BLOB, in cui è impostata la stringa.</span><span class="sxs-lookup"><span data-stu-id="41937-112">A pointer to the **Category** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="41937-113">*pTagName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41937-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41937-114">Puntatore al **tag** della stringa richiesta.</span><span class="sxs-lookup"><span data-stu-id="41937-114">A pointer to the **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="41937-115">*pString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41937-115">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41937-116">Puntatore alla variabile in cui verrà restituito un puntatore alla stringa.</span><span class="sxs-lookup"><span data-stu-id="41937-116">A pointer to the variable where a pointer to the string will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41937-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41937-117">Return value</span></span>

<span data-ttu-id="41937-118">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="41937-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="41937-119">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica il problema.</span><span class="sxs-lookup"><span data-stu-id="41937-119">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="41937-120">Se il **proprietario**, la **categoria** o le informazioni sui **tag** specificati non esistono, il valore restituito è NMERR la voce del \_ BLOB non \_ \_ \_ \_ esiste.</span><span class="sxs-lookup"><span data-stu-id="41937-120">If the specified **Owner**, **Category**, or **Tag** information does not exist, the return value is NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST.</span></span>

## <a name="requirements"></a><span data-ttu-id="41937-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41937-121">Requirements</span></span>



| <span data-ttu-id="41937-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="41937-122">Requirement</span></span> | <span data-ttu-id="41937-123">Valore</span><span class="sxs-lookup"><span data-stu-id="41937-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41937-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41937-124">Minimum supported client</span></span><br/> | <span data-ttu-id="41937-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41937-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="41937-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41937-126">Minimum supported server</span></span><br/> | <span data-ttu-id="41937-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="41937-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="41937-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41937-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="41937-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="41937-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="41937-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="41937-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="41937-131"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41937-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="41937-132">DLL</span><span class="sxs-lookup"><span data-stu-id="41937-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41937-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41937-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41937-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41937-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41937-135">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="41937-135">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="41937-136">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="41937-136">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="41937-137">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="41937-137">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="41937-138">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="41937-138">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="41937-139">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="41937-139">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="41937-140">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="41937-140">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="41937-141">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="41937-141">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="41937-142">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="41937-142">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="41937-143">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="41937-143">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> </dl>

 

 





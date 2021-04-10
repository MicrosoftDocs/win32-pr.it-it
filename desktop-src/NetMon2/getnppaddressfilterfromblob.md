---
description: La funzione GetNPPAddressFilterFromBlob compila il filtro degli indirizzi specificato con le informazioni archiviate nel BLOB.
ms.assetid: b34e0e52-1b2a-4d61-b60c-f1b19ff8ff38
title: Funzione GetNPPAddressFilterFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPAddressFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 944821620123d63f654e286a77018232c79981e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968389"
---
# <a name="getnppaddressfilterfromblob-function"></a><span data-ttu-id="bcc6c-103">GetNPPAddressFilterFromBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="bcc6c-103">GetNPPAddressFilterFromBlob function</span></span>

<span data-ttu-id="bcc6c-104">La funzione **GetNPPAddressFilterFromBlob** compila il filtro degli indirizzi specificato con le informazioni archiviate nel BLOB.</span><span class="sxs-lookup"><span data-stu-id="bcc6c-104">The **GetNPPAddressFilterFromBlob** function fills in the given address filter with information stored in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcc6c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcc6c-105">Syntax</span></span>


```C++
DWORD GetNPPAddressFilterFromBlob(
  _In_    HBLOB          hBlob,
  _Inout_ LPADDRESSTABLE pAddressTable,
  _Out_   HBLOB          hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="bcc6c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcc6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcc6c-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bcc6c-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcc6c-108">Handle per un BLOB.</span><span class="sxs-lookup"><span data-stu-id="bcc6c-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="bcc6c-109">*pAddressTable* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="bcc6c-109">*pAddressTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcc6c-110">Puntatore alla tabella degli indirizzi allocati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="bcc6c-110">Pointer to the user-allocated address table.</span></span>

</dd> <dt>

<span data-ttu-id="bcc6c-111">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bcc6c-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcc6c-112">Handle per un BLOB di errori che specifica il punto in cui si è verificato l'errore (se presente) nel BLOB originale.</span><span class="sxs-lookup"><span data-stu-id="bcc6c-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcc6c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcc6c-113">Return value</span></span>

<span data-ttu-id="bcc6c-114">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bcc6c-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bcc6c-115">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.</span><span class="sxs-lookup"><span data-stu-id="bcc6c-115">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcc6c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="bcc6c-116">Remarks</span></span>

<span data-ttu-id="bcc6c-117">Le informazioni relative all'indirizzo sono archiviate nella sezione **config** della categoria del **proprietario** dell'area di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="bcc6c-117">The address information is stored in the **Config** section of the BLOB NPP **Owner** category.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcc6c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcc6c-118">Requirements</span></span>



| <span data-ttu-id="bcc6c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcc6c-119">Requirement</span></span> | <span data-ttu-id="bcc6c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="bcc6c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcc6c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcc6c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bcc6c-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bcc6c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bcc6c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcc6c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bcc6c-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bcc6c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bcc6c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bcc6c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcc6c-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcc6c-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="bcc6c-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="bcc6c-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="bcc6c-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcc6c-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="bcc6c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="bcc6c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcc6c-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcc6c-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcc6c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcc6c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcc6c-132">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="bcc6c-132">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="bcc6c-133">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="bcc6c-133">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="bcc6c-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="bcc6c-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="bcc6c-135">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="bcc6c-135">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="bcc6c-136">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="bcc6c-136">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="bcc6c-137">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="bcc6c-137">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="bcc6c-138">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="bcc6c-138">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="bcc6c-139">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="bcc6c-139">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="bcc6c-140">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="bcc6c-140">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="bcc6c-141">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="bcc6c-141">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 





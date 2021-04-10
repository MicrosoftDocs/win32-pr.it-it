---
description: USA chiamate sequenziali per recuperare tutte le stringhe all'interno di intervalli specificati.
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: Funzione GetStringsFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringsFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 25fbc149a663ef68d1588218937568401f414ef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966459"
---
# <a name="getstringsfromblob-function"></a><span data-ttu-id="b5262-103">GetStringsFromBlob (funzione)</span><span class="sxs-lookup"><span data-stu-id="b5262-103">GetStringsFromBlob function</span></span>

<span data-ttu-id="b5262-104">La funzione **GetStringsFromBlob** USA chiamate sequenziali per recuperare tutte le stringhe all'interno degli intervalli specificati.</span><span class="sxs-lookup"><span data-stu-id="b5262-104">The **GetStringsFromBlob** function uses sequential calls to retrieve all of the strings within specified ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5262-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5262-105">Syntax</span></span>


```C++
DWORD GetStringsFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pRequestedOwnerName,
  _In_  const char  *pRequestedCategoryName,
  _In_  const char  *pRequestedTagName,
  _Out_ const char  **ppReturnedOwnerName,
  _Out_ const char  **ppReturnedCategoryName,
  _Out_ const char  **ppReturnedTagName,
  _Out_ const char  **ppReturnedString,
  _Out_       DWORD *pRestartKey
);
```



## <a name="parameters"></a><span data-ttu-id="b5262-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5262-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5262-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5262-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5262-108">Handle per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="b5262-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="b5262-109">*pRequestedOwnerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5262-109">*pRequestedOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5262-110">Puntatore alla sezione del proprietario da cui ottenere la stringa.</span><span class="sxs-lookup"><span data-stu-id="b5262-110">A pointer to the Owner section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="b5262-111">*pRequestedCategoryName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5262-111">*pRequestedCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5262-112">Puntatore alla sezione della categoria da cui ottenere la stringa.</span><span class="sxs-lookup"><span data-stu-id="b5262-112">A pointer to the Category section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="b5262-113">*pRequestedTagName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5262-113">*pRequestedTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5262-114">Puntatore al tag per la stringa richiesta.</span><span class="sxs-lookup"><span data-stu-id="b5262-114">A pointer to the tag for the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="b5262-115">*ppReturnedOwnerName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5262-115">*ppReturnedOwnerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5262-116">Puntatore alla variabile che punta alla posizione in cui verrà restituito il nome del **proprietario** .</span><span class="sxs-lookup"><span data-stu-id="b5262-116">A pointer to the variable that points to where the **Owner** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="b5262-117">*ppReturnedCategoryName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5262-117">*ppReturnedCategoryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5262-118">Puntatore alla variabile che punta alla posizione in cui verrà restituito il nome della **categoria** .</span><span class="sxs-lookup"><span data-stu-id="b5262-118">A pointer to the variable that points to where the **Category** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="b5262-119">*ppReturnedTagName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5262-119">*ppReturnedTagName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5262-120">Puntatore alla variabile che punta alla posizione in cui verrà restituito il nome del **tag** .</span><span class="sxs-lookup"><span data-stu-id="b5262-120">A pointer to the variable that points to where the **Tag** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="b5262-121">*ppReturnedString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5262-121">*ppReturnedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5262-122">Puntatore alla variabile che punta alla posizione in cui verrà restituito il nome della stringa.</span><span class="sxs-lookup"><span data-stu-id="b5262-122">A pointer to the variable that points to where the string name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="b5262-123">*pRestartKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b5262-123">*pRestartKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5262-124">Puntatore alla variabile in cui verrà specificata e restituita la chiave di riavvio.</span><span class="sxs-lookup"><span data-stu-id="b5262-124">A pointer to the variable where the restart key will be specified and returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5262-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5262-125">Return value</span></span>

<span data-ttu-id="b5262-126">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b5262-126">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b5262-127">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica il problema.</span><span class="sxs-lookup"><span data-stu-id="b5262-127">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="b5262-128">Se una combinazione specificata di informazioni su **proprietario**, **categoria** e **tag** non esiste, il valore restituito è NMERR la voce del **BLOB non \_ \_ \_ \_ \_ esiste**.</span><span class="sxs-lookup"><span data-stu-id="b5262-128">If a specified combination of **Owner**, **Category**, and **Tag** information does not exist, the return value is **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

<span data-ttu-id="b5262-129">Quando il BLOB viene attraversato completamente entro i limiti specificati inizialmente, la funzione restituisce la **voce del \_ BLOB NMERR non \_ \_ \_ \_ esiste** e il parametro *pRestartKey* punta a zero.</span><span class="sxs-lookup"><span data-stu-id="b5262-129">When the BLOB is traversed completely within the bounds initially specified, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**, and the *pRestartKey* parameter points to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5262-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5262-130">Remarks</span></span>

<span data-ttu-id="b5262-131">Nella chiamata iniziale alla funzione **GetStringsFromBlob** , il parametro *pRestartKey* punta a una variabile che contiene il valore zero.</span><span class="sxs-lookup"><span data-stu-id="b5262-131">On the initial call to the **GetStringsFromBlob** function, the *pRestartKey* parameter points to a variable that contains the value zero.</span></span> <span data-ttu-id="b5262-132">I parametri preesistenti possono essere utilizzati solo quando la *chiave di riavvio* è zero.</span><span class="sxs-lookup"><span data-stu-id="b5262-132">The *pRequested* parameters can be used only when the restart key is zero.</span></span> <span data-ttu-id="b5262-133">Nelle chiamate successive, quando *pRestartKey* ha valori diversi da zero, i parametri *precercati* vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="b5262-133">In subsequent calls, when *pRestartKey* has nonzero values, the *pRequested* parameters are ignored.</span></span> <span data-ttu-id="b5262-134">Nella chiamata iniziale, all può puntare a **null**, che imposta la query in modo che restituisca tutte le voci nel BLOB, una per ogni chiamata successiva.</span><span class="sxs-lookup"><span data-stu-id="b5262-134">On the initial call, all may point to **NULL**, which sets up the query to return every entry in the BLOB, one per subsequent call.</span></span>

<span data-ttu-id="b5262-135">La specifica di un proprietario limita le stringhe restituite solo a tale proprietario.</span><span class="sxs-lookup"><span data-stu-id="b5262-135">Specifying an owner limits the strings returned to just that owner.</span></span> <span data-ttu-id="b5262-136">Una limitazione simile è vera per le categorie e i tag, con l'avvertenza aggiuntiva che se viene specificata una categoria, è necessario specificare anche un proprietario e se viene specificato un tag, è necessario specificare una categoria (e quindi un proprietario).</span><span class="sxs-lookup"><span data-stu-id="b5262-136">A similar limitation is true for categories and tags, with the additional caveat that if a category is specified, an owner must also be specified and if a tag is specified, a category (and therefore an owner) must be specified.</span></span>

<span data-ttu-id="b5262-137">Quando viene restituita la chiamata iniziale a **GetStringsFromBlob** , *pRestartKey* punta a un nuovo valore, che deve essere specificato nella chiamata successiva alla funzione per ottenere il valore successivo.</span><span class="sxs-lookup"><span data-stu-id="b5262-137">When the initial call to **GetStringsFromBlob** returns, *pRestartKey* points to a new value, which should be specified on the next call to the function to get the next value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5262-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5262-138">Requirements</span></span>



| <span data-ttu-id="b5262-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5262-139">Requirement</span></span> | <span data-ttu-id="b5262-140">Valore</span><span class="sxs-lookup"><span data-stu-id="b5262-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5262-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5262-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b5262-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b5262-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b5262-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5262-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b5262-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b5262-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5262-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5262-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5262-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5262-146"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="b5262-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5262-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5262-148"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5262-148"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5262-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b5262-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5262-150"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5262-150"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5262-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5262-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5262-152">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="b5262-152">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="b5262-153">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="b5262-153">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="b5262-154">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="b5262-154">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="b5262-155">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="b5262-155">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="b5262-156">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="b5262-156">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="b5262-157">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="b5262-157">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="b5262-158">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="b5262-158">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="b5262-159">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="b5262-159">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="b5262-160">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="b5262-160">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="b5262-161">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="b5262-161">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> </dl>

 

 





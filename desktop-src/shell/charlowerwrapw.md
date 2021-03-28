---
description: Converte una stringa di caratteri Unicode o un singolo carattere in caratteri minuscoli.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: CharLowerWrapW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharLowerWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 3911e0366d30f3eb9420391f9d06867ded73530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525399"
---
# <a name="charlowerwrapw-function"></a><span data-ttu-id="6e127-103">CharLowerWrapW (funzione)</span><span class="sxs-lookup"><span data-stu-id="6e127-103">CharLowerWrapW function</span></span>

<span data-ttu-id="6e127-104">\[**CharLowerWrapW** è disponibile per l'utilizzo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6e127-104">\[**CharLowerWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="6e127-105">Potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6e127-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="6e127-106">È consigliabile usare [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) al suo posto.\]</span><span class="sxs-lookup"><span data-stu-id="6e127-106">You should use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in its place.\]</span></span>

<span data-ttu-id="6e127-107">Converte una stringa di caratteri Unicode o un singolo carattere in caratteri minuscoli.</span><span class="sxs-lookup"><span data-stu-id="6e127-107">Converts a Unicode character string or a single character to lowercase.</span></span> <span data-ttu-id="6e127-108">Se l'operando è una stringa di caratteri, la funzione converte i caratteri sul posto.</span><span class="sxs-lookup"><span data-stu-id="6e127-108">If the operand is a character string, the function converts the characters in place.</span></span>

> [!Note]  
> <span data-ttu-id="6e127-109">**CharLowerWrapW** è un wrapper per la funzione **CharLowerW** .</span><span class="sxs-lookup"><span data-stu-id="6e127-109">**CharLowerWrapW** is a wrapper for the **CharLowerW** function.</span></span> <span data-ttu-id="6e127-110">Per ulteriori note sull'utilizzo, vedere la pagina [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) .</span><span class="sxs-lookup"><span data-stu-id="6e127-110">See the [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6e127-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e127-111">Syntax</span></span>


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a><span data-ttu-id="6e127-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e127-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e127-113">*PCH* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6e127-113">*pch* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e127-114">Tipo: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="6e127-114">Type: **LPWSTR**</span></span>

<span data-ttu-id="6e127-115">Puntatore a una stringa Unicode con terminazione null o a un singolo carattere.</span><span class="sxs-lookup"><span data-stu-id="6e127-115">A pointer to a null-terminated Unicode string or a single character.</span></span> <span data-ttu-id="6e127-116">Se la parola più significativa di questo parametro è zero, la parola di ordine inferiore deve contenere solo un singolo carattere da convertire.</span><span class="sxs-lookup"><span data-stu-id="6e127-116">If the high-order word of this parameter is zero, the low-order word must contain only a single character to be converted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e127-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e127-117">Return value</span></span>

<span data-ttu-id="6e127-118">Tipo: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="6e127-118">Type: **LPWSTR**</span></span>

<span data-ttu-id="6e127-119">Se *PCH* è una stringa di caratteri, la funzione restituisce un puntatore alla stringa convertita.</span><span class="sxs-lookup"><span data-stu-id="6e127-119">If *pch* is a character string, the function returns a pointer to the converted string.</span></span> <span data-ttu-id="6e127-120">Poiché la stringa viene convertita sul posto, il valore restituito è uguale a *PCH*.</span><span class="sxs-lookup"><span data-stu-id="6e127-120">Since the string is converted in place, the return value is equal to *pch*.</span></span>

<span data-ttu-id="6e127-121">Se *PCH* è un singolo carattere, il valore restituito è un valore a 32 bit la cui parola più elevata è zero e la parola di ordine inferiore contiene il carattere convertito.</span><span class="sxs-lookup"><span data-stu-id="6e127-121">If *pch* is a single character, the return value is a 32-bit value whose high-order word is zero, and low-order word contains the converted character.</span></span>

<span data-ttu-id="6e127-122">Non è presente alcuna indicazione di esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="6e127-122">There is no indication of success or failure.</span></span> <span data-ttu-id="6e127-123">L'errore è raro.</span><span class="sxs-lookup"><span data-stu-id="6e127-123">Failure is rare.</span></span> <span data-ttu-id="6e127-124">Non sono disponibili informazioni estese sull'errore per questa funzione. non chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="6e127-124">There is no extended error information for this function; do not call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="6e127-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e127-125">Remarks</span></span>

<span data-ttu-id="6e127-126">Il metodo preferito consiste nell'usare [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) insieme a Microsoft Layer for Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="6e127-126">The preferred method is to use [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="6e127-127">**CharLowerWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 38.</span><span class="sxs-lookup"><span data-stu-id="6e127-127">**CharLowerWrapW** must be called directly from Shlwapi.dll, using ordinal 38.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e127-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e127-128">Requirements</span></span>



| <span data-ttu-id="6e127-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e127-129">Requirement</span></span> | <span data-ttu-id="6e127-130">Valore</span><span class="sxs-lookup"><span data-stu-id="6e127-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e127-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e127-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6e127-132">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6e127-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e127-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e127-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6e127-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e127-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6e127-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6e127-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e127-136"><dt>Shlwapi.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="6e127-136"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e127-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e127-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e127-138">**CharLower**</span><span class="sxs-lookup"><span data-stu-id="6e127-138">**CharLower**</span></span>](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 

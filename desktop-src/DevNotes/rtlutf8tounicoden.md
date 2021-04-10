---
description: Converte la stringa di origine specificata in una stringa Unicode, usando la tabella codici UTF-8 (Unicode Transformation Format) a 8 bit.
ms.assetid: 2871a81b-74f9-462e-9e5c-c59d06bb6841
title: Funzione RtlUTF8ToUnicodeN (WDM. h)
ms.topic: reference
ms.date: 02/21/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUTF8ToUnicodeN
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b3de7192a9a26d367fc0b6ad231fbc046514ec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225593"
---
# <a name="rtlutf8tounicoden-function"></a><span data-ttu-id="c2b36-103">RtlUTF8ToUnicodeN (funzione)</span><span class="sxs-lookup"><span data-stu-id="c2b36-103">RtlUTF8ToUnicodeN function</span></span>

<span data-ttu-id="c2b36-104">Converte la stringa di origine specificata in una stringa Unicode, usando la tabella codici UTF-8 (Unicode Transformation Format) a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="c2b36-104">Translates the specified source string into a Unicode string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2b36-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2b36-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUTF8ToUnicodeN(
  _Out_     PWSTR  UnicodeStringDestination,
  _In_      ULONG  UnicodeStringMaxByteCount,
  _Out_opt_ PULONG UnicodeStringActualByteCount,
  _In_      PCCH   UTF8StringSource,
  _In_      ULONG  UTF8StringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="c2b36-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2b36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2b36-107">*UnicodeStringDestination* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c2b36-107">*UnicodeStringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2b36-108">Puntatore a un buffer allocato dal chiamante che riceve la stringa tradotta.</span><span class="sxs-lookup"><span data-stu-id="c2b36-108">A pointer to a caller-allocated buffer that receives the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="c2b36-109">*UnicodeStringMaxByteCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2b36-109">*UnicodeStringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2b36-110">Numero massimo di byte da scrivere in *UnicodeStringDestination*.</span><span class="sxs-lookup"><span data-stu-id="c2b36-110">Maximum number of bytes to be written at *UnicodeStringDestination*.</span></span> <span data-ttu-id="c2b36-111">Se questo valore fa sì che la stringa tradotta venga troncata, **RtlUTF8ToUnicodeN** restituisce uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="c2b36-111">If this value causes the translated string to be truncated, **RtlUTF8ToUnicodeN** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="c2b36-112">*UnicodeStringActualByteCount* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c2b36-112">*UnicodeStringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2b36-113">Puntatore a una variabile allocata dal chiamante che riceve la lunghezza, in byte, della stringa tradotta.</span><span class="sxs-lookup"><span data-stu-id="c2b36-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="c2b36-114">Questo parametro è facoltativo e può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="c2b36-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="c2b36-115">Se la stringa viene troncata, il numero restituito conteggia il conteggio effettivo delle stringhe troncate.</span><span class="sxs-lookup"><span data-stu-id="c2b36-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="c2b36-116">*UTF8StringSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2b36-116">*UTF8StringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2b36-117">Puntatore alla stringa da tradurre.</span><span class="sxs-lookup"><span data-stu-id="c2b36-117">A pointer to the string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="c2b36-118">*UTF8StringByteCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2b36-118">*UTF8StringByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2b36-119">Dimensione, in byte, della stringa in corrispondenza di *UTF8StringSource*.</span><span class="sxs-lookup"><span data-stu-id="c2b36-119">Size, in bytes, of the string at *UTF8StringSource*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2b36-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2b36-120">Return value</span></span>

<span data-ttu-id="c2b36-121">**RtlUTF8ToUnicodeN** restituisce uno dei valori NTSTATUS seguenti:</span><span class="sxs-lookup"><span data-stu-id="c2b36-121">**RtlUTF8ToUnicodeN** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="c2b36-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c2b36-122">Return code</span></span>                                                                                                  | <span data-ttu-id="c2b36-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2b36-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2b36-124"><dt>**STATO \_ riuscito**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b36-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="c2b36-125">La stringa è stata convertita in Unicode.</span><span class="sxs-lookup"><span data-stu-id="c2b36-125">The string was converted to Unicode.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="c2b36-126"><dt>**STATO \_ \_ non \_ mappato**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b36-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="c2b36-127">È stato rilevato e sostituito un carattere di input non valido.</span><span class="sxs-lookup"><span data-stu-id="c2b36-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="c2b36-128">Questo stato è considerato uno stato di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c2b36-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="c2b36-129"><dt>**STATO \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b36-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="c2b36-130">Entrambi i puntatori a *UnicodeStringDestination* e *UnicodeStringActualByteCount* sono **null**.</span><span class="sxs-lookup"><span data-stu-id="c2b36-130">Both pointers to *UnicodeStringDestination* and *UnicodeStringActualByteCount* were **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="c2b36-131"><dt>**STATO \_ parametro non valido \_ \_ 4**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b36-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="c2b36-132">*UTF8StringSource* è **null**.</span><span class="sxs-lookup"><span data-stu-id="c2b36-132">The *UTF8StringSource* was **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="c2b36-133"><dt>**BUFFER di stato \_ \_ troppo \_ piccolo**</dt></span><span class="sxs-lookup"><span data-stu-id="c2b36-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="c2b36-134">*UnicodeStringDestination* troncato.</span><span class="sxs-lookup"><span data-stu-id="c2b36-134">*UnicodeStringDestination* was truncated.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="c2b36-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2b36-135">Remarks</span></span>

<span data-ttu-id="c2b36-136">Anche se *UnicodeStringActualByteCount* è facoltativo e può essere **null**, i chiamanti devono fornire lo spazio di archiviazione, perché la lunghezza ricevuta può essere usata per determinare se la conversione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="c2b36-136">Although *UnicodeStringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span>

<span data-ttu-id="c2b36-137">Se l'output viene troncato e viene rilevato un carattere di input non valido, la funzione restituisce un errore di buffer di stato \_ \_ troppo \_ piccolo.</span><span class="sxs-lookup"><span data-stu-id="c2b36-137">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="c2b36-138">Se *UnicodeStringDestination* è impostato su **null** , la funzione restituirà il numero di byte richiesto per ospitare la stringa tradotta senza troncamenti in *UnicodeStringActualByteCount*.</span><span class="sxs-lookup"><span data-stu-id="c2b36-138">If the *UnicodeStringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UnicodeStringActualByteCount*.</span></span>

<span data-ttu-id="c2b36-139">**RtlUTF8ToUnicodeN** non modifica la stringa di origine a meno che i puntatori *UnicodeStringDestination* e *UTF8StringSource* non siano equivalenti.</span><span class="sxs-lookup"><span data-stu-id="c2b36-139">**RtlUTF8ToUnicodeN** does not modify the source string unless the *UnicodeStringDestination* and *UTF8StringSource* pointers are equivalent.</span></span> <span data-ttu-id="c2b36-140">La stringa Unicode restituita non è con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="c2b36-140">The returned Unicode string is not null-terminated.</span></span>

<span data-ttu-id="c2b36-141">I chiamanti di **RtlUTF8ToUnicodeN** devono essere in esecuzione a livello IRQL < livello di invio \_ .</span><span class="sxs-lookup"><span data-stu-id="c2b36-141">Callers of **RtlUTF8ToUnicodeN** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2b36-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2b36-142">Requirements</span></span>



| <span data-ttu-id="c2b36-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2b36-143">Requirement</span></span> | <span data-ttu-id="c2b36-144">Valore</span><span class="sxs-lookup"><span data-stu-id="c2b36-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c2b36-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2b36-145">Minimum supported client</span></span><br/> | <span data-ttu-id="c2b36-146">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c2b36-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c2b36-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2b36-147">Minimum supported server</span></span><br/> | <span data-ttu-id="c2b36-148">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2b36-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c2b36-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2b36-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2b36-150"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2b36-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="c2b36-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c2b36-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2b36-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2b36-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2b36-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2b36-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b36-154">**RtlUnicodeToUTF8N**</span><span class="sxs-lookup"><span data-stu-id="c2b36-154">**RtlUnicodeToUTF8N**</span></span>](rtlunicodetoutf8n.md)
</dt> </dl>

 

 





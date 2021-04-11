---
description: Converte la stringa Unicode specificata in una nuova stringa di caratteri utilizzando la tabella codici UTF-8 (Unicode Transformation Format) a 8 bit.
ms.assetid: ecd63eee-bf86-42b5-93d8-3c7871aa6324
title: Funzione RtlUnicodeToUTF8N (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlUnicodeToUTF8N
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 46153dd152ed5a45a65de50ca214fbb24a6dc2ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126399"
---
# <a name="rtlunicodetoutf8n-function"></a><span data-ttu-id="ee8de-103">RtlUnicodeToUTF8N (funzione)</span><span class="sxs-lookup"><span data-stu-id="ee8de-103">RtlUnicodeToUTF8N function</span></span>

<span data-ttu-id="ee8de-104">Converte la stringa Unicode specificata in una nuova stringa di caratteri utilizzando la tabella codici UTF-8 (Unicode Transformation Format) a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="ee8de-104">Translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee8de-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee8de-105">Syntax</span></span>


```C++
NTSTATUS WINAPI RtlUnicodeToUTF8N(
  _Out_     PCHAR  UTF8StringDestination,
  _In_      ULONG  UTF8StringMaxByteCount,
  _Out_opt_ PULONG UTF8StringActualByteCount,
  _In_      PCWSTR UnicodeStringSource,
  _In_      ULONG  UnicodeStringByteCount
);
```



## <a name="parameters"></a><span data-ttu-id="ee8de-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee8de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee8de-107">*UTF8StringDestination* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ee8de-107">*UTF8StringDestination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee8de-108">Puntatore a un buffer allocato dal chiamante per ricevere la stringa tradotta.</span><span class="sxs-lookup"><span data-stu-id="ee8de-108">A pointer to a caller-allocated buffer to receive the translated string.</span></span>

</dd> <dt>

<span data-ttu-id="ee8de-109">*UTF8StringMaxByteCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee8de-109">*UTF8StringMaxByteCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee8de-110">Numero massimo di byte da scrivere in *UTF8StringDestination*.</span><span class="sxs-lookup"><span data-stu-id="ee8de-110">Maximum number of bytes to be written to *UTF8StringDestination*.</span></span> <span data-ttu-id="ee8de-111">Se questo valore fa sì che la stringa tradotta venga troncata, **RtlUnicodeToUTF8N** restituisce uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="ee8de-111">If this value causes the translated string to be truncated, **RtlUnicodeToUTF8N** returns an error status.</span></span>

</dd> <dt>

<span data-ttu-id="ee8de-112">*UTF8StringActualByteCount* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ee8de-112">*UTF8StringActualByteCount* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ee8de-113">Puntatore a una variabile allocata dal chiamante che riceve la lunghezza, in byte, della stringa tradotta.</span><span class="sxs-lookup"><span data-stu-id="ee8de-113">A pointer to a caller-allocated variable that receives the length, in bytes, of the translated string.</span></span> <span data-ttu-id="ee8de-114">Questo parametro è facoltativo e può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="ee8de-114">This parameter is optional and can be **NULL**.</span></span> <span data-ttu-id="ee8de-115">Se la stringa viene troncata, il numero restituito conteggia il conteggio effettivo delle stringhe troncate.</span><span class="sxs-lookup"><span data-stu-id="ee8de-115">If the string is truncated then the returned number counts the actual truncated string count.</span></span>

</dd> <dt>

<span data-ttu-id="ee8de-116">*UnicodeStringSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee8de-116">*UnicodeStringSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee8de-117">Puntatore alla stringa di origine Unicode da tradurre.</span><span class="sxs-lookup"><span data-stu-id="ee8de-117">A pointer to the Unicode source string to be translated.</span></span>

</dd> <dt>

<span data-ttu-id="ee8de-118">\* UnicodeStringByteCount \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee8de-118">\*UnicodeStringByteCount \* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee8de-119">Specifica il numero di byte nella stringa di origine Unicode a cui punta il parametro *UnicodeStringSource* .</span><span class="sxs-lookup"><span data-stu-id="ee8de-119">Specifies the number of bytes in the Unicode source string that the *UnicodeStringSource* parameter points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee8de-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee8de-120">Return value</span></span>

<span data-ttu-id="ee8de-121">**RtlUnicodeToUTF8N** restituisce uno dei valori NTSTATUS seguenti:</span><span class="sxs-lookup"><span data-stu-id="ee8de-121">**RtlUnicodeToUTF8N** returns one of the following NTSTATUS values:</span></span>



| <span data-ttu-id="ee8de-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ee8de-122">Return code</span></span>                                                                                                  | <span data-ttu-id="ee8de-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee8de-123">Description</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ee8de-124"><dt>**STATO \_ riuscito**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8de-124"><dt>**STATUS\_SUCCESS**</dt></span></span> </dl>               | <span data-ttu-id="ee8de-125">La stringa Unicode è stata convertita in UTF-8.</span><span class="sxs-lookup"><span data-stu-id="ee8de-125">The Unicode string was converted to UTF-8.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="ee8de-126"><dt>**STATO \_ \_ non \_ mappato**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8de-126"><dt>**STATUS\_SOME\_NOT\_MAPPED**</dt></span></span> </dl>     | <span data-ttu-id="ee8de-127">È stato rilevato e sostituito un carattere di input non valido.</span><span class="sxs-lookup"><span data-stu-id="ee8de-127">An invalid input character was encountered and replaced.</span></span> <span data-ttu-id="ee8de-128">Questo stato è considerato uno stato di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ee8de-128">This status is considered a success status.</span></span><br/> |
| <dl> <span data-ttu-id="ee8de-129"><dt>**STATO \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8de-129"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="ee8de-130">Entrambi i puntatori a *UTF8StringDestination* e *UTF8StringActualByteCount* sono **null**.</span><span class="sxs-lookup"><span data-stu-id="ee8de-130">Both pointers to *UTF8StringDestination* and *UTF8StringActualByteCount* were **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="ee8de-131"><dt>**STATO \_ parametro non valido \_ \_ 4**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8de-131"><dt>**STATUS\_INVALID\_PARAMETER\_4**</dt></span></span> </dl> | <span data-ttu-id="ee8de-132">*UnicodeStringSource* è **null**.</span><span class="sxs-lookup"><span data-stu-id="ee8de-132">The *UnicodeStringSource* was **NULL**.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="ee8de-133"><dt>**BUFFER di stato \_ \_ troppo \_ piccolo**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8de-133"><dt>**STATUS\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>    | <span data-ttu-id="ee8de-134">*UTF8StringDestination* troncato.</span><span class="sxs-lookup"><span data-stu-id="ee8de-134">*UTF8StringDestination* was truncated.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="ee8de-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee8de-135">Remarks</span></span>

<span data-ttu-id="ee8de-136">Anche se *UTF8StringActualByteCount* è facoltativo e può essere **null**, i chiamanti devono fornire lo spazio di archiviazione, perché la lunghezza ricevuta può essere usata per determinare se la conversione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="ee8de-136">Although *UTF8StringActualByteCount* is optional and can be **NULL**, callers should provide storage for it, because the received length can be used to determine whether the conversion was successful.</span></span> <span data-ttu-id="ee8de-137">Questa routine non modifica la stringa di origine.</span><span class="sxs-lookup"><span data-stu-id="ee8de-137">This routine does not modify the source string.</span></span> <span data-ttu-id="ee8de-138">Restituisce una stringa UTF-8 con terminazione null se il *UnicodeStringSource* specificato include un carattere di terminazione null e se il *UTF8StringMaxByteCount* specificato non ha causato il troncamento.</span><span class="sxs-lookup"><span data-stu-id="ee8de-138">It returns a null-terminated UTF-8 string if the given *UnicodeStringSource* included a NULL terminator and if the given *UTF8StringMaxByteCount* did not cause truncation.</span></span>

<span data-ttu-id="ee8de-139">Se l'output viene troncato e viene rilevato un carattere di input non valido, la funzione restituisce un errore di buffer di stato \_ \_ troppo \_ piccolo.</span><span class="sxs-lookup"><span data-stu-id="ee8de-139">If the output is truncated and an invalid input character is encountered then the function returns STATUS\_BUFFER\_TOO\_SMALL error.</span></span>

<span data-ttu-id="ee8de-140">Se *UTF8StringDestination* è impostato su **null** , la funzione restituirà il numero di byte richiesto per ospitare la stringa tradotta senza troncamenti in *UTF8StringActualByteCount*.</span><span class="sxs-lookup"><span data-stu-id="ee8de-140">If the *UTF8StringDestination* is set to **NULL** the function will return the required number of bytes to host the translated string without any truncation in *UTF8StringActualByteCount*.</span></span>

<span data-ttu-id="ee8de-141">I chiamanti di **RtlUnicodeToUTF8N** devono essere in esecuzione a livello IRQL < livello di invio \_ .</span><span class="sxs-lookup"><span data-stu-id="ee8de-141">Callers of **RtlUnicodeToUTF8N** must be running at IRQL < DISPATCH\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee8de-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee8de-142">Requirements</span></span>



| <span data-ttu-id="ee8de-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee8de-143">Requirement</span></span> | <span data-ttu-id="ee8de-144">Valore</span><span class="sxs-lookup"><span data-stu-id="ee8de-144">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8de-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee8de-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ee8de-146">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ee8de-146">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ee8de-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee8de-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ee8de-148">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ee8de-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ee8de-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee8de-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee8de-150"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee8de-150"><dt>Wdm.h</dt></span></span> </dl>     |
| <span data-ttu-id="ee8de-151">DLL</span><span class="sxs-lookup"><span data-stu-id="ee8de-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee8de-152"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee8de-152"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee8de-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee8de-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee8de-154">**RtlUTF8ToUnicodeN**</span><span class="sxs-lookup"><span data-stu-id="ee8de-154">**RtlUTF8ToUnicodeN**</span></span>](rtlutf8tounicoden.md)
</dt> </dl>

 

 





---
description: Formatta l'ora come stringa temporale per le impostazioni locali specificate.
ms.assetid: 048b209c-f757-4b65-9ce7-282a5c21021f
title: GetTimeFormatWrapW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTimeFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 53f1bb88c2b3a79b58f3025daec31a7b1340b642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979647"
---
# <a name="gettimeformatwrapw-function"></a><span data-ttu-id="ab480-103">GetTimeFormatWrapW (funzione)</span><span class="sxs-lookup"><span data-stu-id="ab480-103">GetTimeFormatWrapW function</span></span>

<span data-ttu-id="ab480-104">\[**GetTimeFormatWrapW** è disponibile per l'utilizzo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab480-104">\[**GetTimeFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="ab480-105">Potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ab480-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="ab480-106">È consigliabile usare [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) al suo posto.\]</span><span class="sxs-lookup"><span data-stu-id="ab480-106">You should use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in its place.\]</span></span>

<span data-ttu-id="ab480-107">Formatta l'ora come stringa temporale per le impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="ab480-107">Formats time as a time string for a specified locale.</span></span> <span data-ttu-id="ab480-108">La funzione formatta un'ora specificata o l'ora di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="ab480-108">The function formats either a specified time or the local system time.</span></span>

> [!Note]  
> <span data-ttu-id="ab480-109">**GetTimeFormatWrapW** è un wrapper per la funzione **GetTimeFormatW** .</span><span class="sxs-lookup"><span data-stu-id="ab480-109">**GetTimeFormatWrapW** is a wrapper for the **GetTimeFormatW** function.</span></span> <span data-ttu-id="ab480-110">Per ulteriori note sull'utilizzo, vedere la pagina [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .</span><span class="sxs-lookup"><span data-stu-id="ab480-110">See the [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ab480-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab480-111">Syntax</span></span>


```C++
int GetTimeFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpTime,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzTimeStr,
  _In_        int        cchTime
);
```



## <a name="parameters"></a><span data-ttu-id="ab480-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab480-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab480-113">*Impostazioni locali* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab480-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab480-114">Tipo: **LCID**</span><span class="sxs-lookup"><span data-stu-id="ab480-114">Type: **LCID**</span></span>

<span data-ttu-id="ab480-115">Specifica le impostazioni locali per cui deve essere formattata la stringa dell'ora.</span><span class="sxs-lookup"><span data-stu-id="ab480-115">Specifies the locale for which the time string is to be formatted.</span></span> <span data-ttu-id="ab480-116">Se *pwzFormat* è **null**, la funzione formatta la stringa in base al formato dell'ora per le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="ab480-116">If *pwzFormat* is **NULL**, the function formats the string according to the time format for this locale.</span></span> <span data-ttu-id="ab480-117">Se *pwzFormat* non è **null**, la funzione usa le impostazioni locali solo per le informazioni non specificate nella stringa dell'immagine di formato (ad esempio, i marcatori temporali delle impostazioni locali).</span><span class="sxs-lookup"><span data-stu-id="ab480-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's time markers).</span></span>

<span data-ttu-id="ab480-118">Questo parametro può essere un identificatore delle impostazioni locali creato dalla macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) o uno dei seguenti valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="ab480-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="ab480-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**impostazioni locali del \_ sistema \_**</span><span class="sxs-lookup"><span data-stu-id="ab480-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="ab480-120">Impostazioni locali del sistema predefinite.</span><span class="sxs-lookup"><span data-stu-id="ab480-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="ab480-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_impostazione predefinita utente impostazioni locali \_**</span><span class="sxs-lookup"><span data-stu-id="ab480-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="ab480-122">Impostazioni locali dell'utente predefinite.</span><span class="sxs-lookup"><span data-stu-id="ab480-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ab480-123">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab480-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab480-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ab480-124">Type: **DWORD**</span></span>

<span data-ttu-id="ab480-125">Specifica varie opzioni di funzione.</span><span class="sxs-lookup"><span data-stu-id="ab480-125">Specifies various function options.</span></span> <span data-ttu-id="ab480-126">È possibile specificare una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ab480-126">You can specify a combination of the following values.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="ab480-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**impostazioni locali \_ NOUSEROVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="ab480-127"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="ab480-128">Se impostata, la funzione formatta la stringa utilizzando il formato di ora predefinito del sistema per le impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="ab480-128">If set, the function formats the string using the system default time format for the specified locale.</span></span> <span data-ttu-id="ab480-129">Se non è impostato, la funzione formatta la stringa usando qualsiasi override utente nel formato di ora predefinito delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="ab480-129">If not set, the function formats the string using any user overrides to the locale's default time format.</span></span> <span data-ttu-id="ab480-130">Questo flag può essere impostato solo se *pwzFormat* è **null**.</span><span class="sxs-lookup"><span data-stu-id="ab480-130">This flag can only be set if *pwzFormat* is **NULL**.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="ab480-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**impostazioni locali \_ usare \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="ab480-131"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="ab480-132">Usa la tabella codici ANSI di sistema per la conversione di stringhe anziché la tabella codici delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="ab480-132">Uses the system ANSI code page for string translation instead of the locale code page.</span></span>

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span data-ttu-id="ab480-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**TEMPO \_ NOMINUTESORSECONDS**</span><span class="sxs-lookup"><span data-stu-id="ab480-133"><span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**TIME\_NOMINUTESORSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="ab480-134">Non usa minuti o secondi.</span><span class="sxs-lookup"><span data-stu-id="ab480-134">Does not use minutes or seconds.</span></span>

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span data-ttu-id="ab480-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TEMPO \_ NOsecondi**</span><span class="sxs-lookup"><span data-stu-id="ab480-135"><span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**TIME\_NOSECONDS**</span></span>


</dt> <dd>

<span data-ttu-id="ab480-136">Non usa secondi.</span><span class="sxs-lookup"><span data-stu-id="ab480-136">Does not use seconds.</span></span>

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span data-ttu-id="ab480-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**TEMPO \_ NOTIMEMARKER**</span><span class="sxs-lookup"><span data-stu-id="ab480-137"><span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**TIME\_NOTIMEMARKER**</span></span>


</dt> <dd>

<span data-ttu-id="ab480-138">Non utilizza un marcatore di ora.</span><span class="sxs-lookup"><span data-stu-id="ab480-138">Does not use a time marker.</span></span>

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span data-ttu-id="ab480-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**TEMPO \_ FORCE24HOURFORMAT**</span><span class="sxs-lookup"><span data-stu-id="ab480-139"><span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**TIME\_FORCE24HOURFORMAT**</span></span>


</dt> <dd>

<span data-ttu-id="ab480-140">Usa sempre il formato a 24 ore.</span><span class="sxs-lookup"><span data-stu-id="ab480-140">Always uses a 24-hour time format.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ab480-141">*lpTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab480-141">*lpTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab480-142">Tipo: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="ab480-142">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="ab480-143">Puntatore a una struttura [_ *SYSTEMTIME* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) che contiene le informazioni sull'ora da formattare.</span><span class="sxs-lookup"><span data-stu-id="ab480-143">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the time information to be formatted.</span></span> <span data-ttu-id="ab480-144">Se questo puntatore è **null**, la funzione usa l'ora di sistema locale corrente.</span><span class="sxs-lookup"><span data-stu-id="ab480-144">If this pointer is **NULL**, the function uses the current local system time.</span></span>

</dd> <dt>

<span data-ttu-id="ab480-145">*pwzFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab480-145">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab480-146">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ab480-146">Type: **LPCWSTR**</span></span>

<span data-ttu-id="ab480-147">Puntatore a un formato da utilizzare per formare la stringa dell'ora.</span><span class="sxs-lookup"><span data-stu-id="ab480-147">A pointer to a format to use to form the time string.</span></span> <span data-ttu-id="ab480-148">Se *pwzFormat* è **null**, la funzione userà il formato dell'ora delle impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="ab480-148">If *pwzFormat* is **NULL**, the function uses the time format of the specified locale.</span></span> <span data-ttu-id="ab480-149">Per ulteriori informazioni, vedere [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .</span><span class="sxs-lookup"><span data-stu-id="ab480-149">See [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="ab480-150">*pwzTimeStr* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ab480-150">*pwzTimeStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab480-151">Tipo: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="ab480-151">Type: **LPWSTR**</span></span>

<span data-ttu-id="ab480-152">Puntatore a un buffer che riceve la stringa di tempo formattata.</span><span class="sxs-lookup"><span data-stu-id="ab480-152">A pointer to a buffer that receives the formatted time string.</span></span>

</dd> <dt>

<span data-ttu-id="ab480-153">*cchTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab480-153">*cchTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab480-154">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ab480-154">Type: **int**</span></span>

<span data-ttu-id="ab480-155">Dimensione, in caratteri, del buffer *pwzTimeStr* .</span><span class="sxs-lookup"><span data-stu-id="ab480-155">The size, in characters, of the *pwzTimeStr* buffer.</span></span> <span data-ttu-id="ab480-156">Se *cchTime* è zero, la funzione restituisce il numero di caratteri necessari per memorizzare la stringa di tempo formattata e il buffer a cui punta *pwzTimeStr* non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="ab480-156">If *cchTime* is zero, the function returns the number of characters required to hold the formatted time string, and the buffer pointed to by *pwzTimeStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab480-157">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab480-157">Return value</span></span>

<span data-ttu-id="ab480-158">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="ab480-158">Type: **int**</span></span>

<span data-ttu-id="ab480-159">Se la funzione ha esito positivo, il valore restituito è il numero di caratteri scritti nel buffer a cui punta *pwzTimeStr*.</span><span class="sxs-lookup"><span data-stu-id="ab480-159">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzTimeStr*.</span></span> <span data-ttu-id="ab480-160">Se il parametro *cchTime* è zero, il valore restituito è il numero di caratteri necessari per conservare la stringa di tempo formattata.</span><span class="sxs-lookup"><span data-stu-id="ab480-160">If the *cchTime* parameter is zero, the return value is the number of characters required to hold the formatted time string.</span></span> <span data-ttu-id="ab480-161">Il conteggio include il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="ab480-161">The count includes the terminating null character.</span></span>

<span data-ttu-id="ab480-162">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="ab480-162">If the function fails, the return value is zero.</span></span> <span data-ttu-id="ab480-163">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="ab480-163">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="ab480-164">**GetLastError** può restituire uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="ab480-164">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="ab480-165">**ERRORE \_ buffer insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="ab480-165">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="ab480-166">**flag di errore \_ non validi \_**</span><span class="sxs-lookup"><span data-stu-id="ab480-166">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="ab480-167">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="ab480-167">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ab480-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab480-168">Remarks</span></span>

<span data-ttu-id="ab480-169">**GetTimeFormatWrapW** offre la possibilità di utilizzare stringhe Unicode nei sistemi operativi precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab480-169">**GetTimeFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="ab480-170">Il metodo preferito consiste nell'usare [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) insieme a Microsoft Layer for Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="ab480-170">The preferred method is to use [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="ab480-171">**GetTimeFormatWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 310.</span><span class="sxs-lookup"><span data-stu-id="ab480-171">**GetTimeFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 310.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab480-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab480-172">Requirements</span></span>



| <span data-ttu-id="ab480-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab480-173">Requirement</span></span> | <span data-ttu-id="ab480-174">Valore</span><span class="sxs-lookup"><span data-stu-id="ab480-174">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab480-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab480-175">Minimum supported client</span></span><br/> | <span data-ttu-id="ab480-176">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ab480-176">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab480-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab480-177">Minimum supported server</span></span><br/> | <span data-ttu-id="ab480-178">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ab480-178">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ab480-179">DLL</span><span class="sxs-lookup"><span data-stu-id="ab480-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab480-180"><dt>Shlwapi.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="ab480-180"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab480-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab480-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab480-182">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="ab480-182">**GetTimeFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 

---
description: Formatta una data come stringa di data per le impostazioni locali specificate.
ms.assetid: e45f6d1c-2890-44f6-8406-022c99c59e02
title: GetDateFormatWrapW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDateFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: c9c369584fd15a27d5e684452b2277104b5b1da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227442"
---
# <a name="getdateformatwrapw-function"></a><span data-ttu-id="31de4-103">GetDateFormatWrapW (funzione)</span><span class="sxs-lookup"><span data-stu-id="31de4-103">GetDateFormatWrapW function</span></span>

<span data-ttu-id="31de4-104">\[**GetDateFormatWrapW** è disponibile per l'utilizzo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="31de4-104">\[**GetDateFormatWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="31de4-105">Non sarà disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="31de4-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="31de4-106">È consigliabile usare [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) al suo posto.\]</span><span class="sxs-lookup"><span data-stu-id="31de4-106">You should use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in its place.\]</span></span>

<span data-ttu-id="31de4-107">Formatta una data come stringa di data per le impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="31de4-107">Formats a date as a date string for a specified locale.</span></span> <span data-ttu-id="31de4-108">La funzione formatta una data specificata o una data di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="31de4-108">The function formats either a specified date or the local system date.</span></span>

> [!Note]  
> <span data-ttu-id="31de4-109">**GetDateFormatWrapW** è un wrapper per la funzione **GetDateFormatW** .</span><span class="sxs-lookup"><span data-stu-id="31de4-109">**GetDateFormatWrapW** is a wrapper for the **GetDateFormatW** function.</span></span> <span data-ttu-id="31de4-110">Per ulteriori note sull'utilizzo, vedere la pagina [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) .</span><span class="sxs-lookup"><span data-stu-id="31de4-110">See the [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="31de4-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31de4-111">Syntax</span></span>


```C++
int GetDateFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpDate,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzDateStr,
  _In_        int        cchDate
);
```



## <a name="parameters"></a><span data-ttu-id="31de4-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="31de4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31de4-113">*Impostazioni locali* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31de4-113">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31de4-114">Tipo: **LCID**</span><span class="sxs-lookup"><span data-stu-id="31de4-114">Type: **LCID**</span></span>

<span data-ttu-id="31de4-115">Impostazioni locali per cui deve essere formattata la stringa di data.</span><span class="sxs-lookup"><span data-stu-id="31de4-115">The locale for which the date string is to be formatted.</span></span> <span data-ttu-id="31de4-116">Se *pwzFormat* è **null**, la funzione formatta la stringa in base al formato della data per le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="31de4-116">If *pwzFormat* is **NULL**, the function formats the string according to the date format for this locale.</span></span> <span data-ttu-id="31de4-117">Se *pwzFormat* non è **null**, la funzione usa le impostazioni locali solo per le informazioni non specificate nella stringa dell'immagine di formato (ad esempio, i nomi di giorno e mese delle impostazioni locali).</span><span class="sxs-lookup"><span data-stu-id="31de4-117">If *pwzFormat* is not **NULL**, the function uses the locale only for information not specified in the format picture string (for example, the locale's day and month names).</span></span>

<span data-ttu-id="31de4-118">Questo parametro può essere un identificatore delle impostazioni locali creato dalla macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) o uno dei seguenti valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="31de4-118">This parameter can be a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro, or one of the following predefined values.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="31de4-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**impostazioni locali del \_ sistema \_**</span><span class="sxs-lookup"><span data-stu-id="31de4-119"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="31de4-120">Impostazioni locali del sistema predefinite.</span><span class="sxs-lookup"><span data-stu-id="31de4-120">Default system locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="31de4-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_impostazione predefinita utente impostazioni locali \_**</span><span class="sxs-lookup"><span data-stu-id="31de4-121"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="31de4-122">Impostazioni locali dell'utente predefinite.</span><span class="sxs-lookup"><span data-stu-id="31de4-122">Default user locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="31de4-123">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31de4-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31de4-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="31de4-124">Type: **DWORD**</span></span>

<span data-ttu-id="31de4-125">Specifica varie opzioni di funzione.</span><span class="sxs-lookup"><span data-stu-id="31de4-125">Specifies various function options.</span></span> <span data-ttu-id="31de4-126">Se *pwzFormat* non è **null**, questo parametro deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="31de4-126">If *pwzFormat* is not **NULL**, this parameter must be zero.</span></span> <span data-ttu-id="31de4-127">Se *pwzFormat* è **null**, è possibile specificare una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="31de4-127">If *pwzFormat* is **NULL**, you can specify a combination of the following values.</span></span> <span data-ttu-id="31de4-128">Se non si specifica data \_ YEARMONTH, date \_ shortdate o date \_ LONGDATE e *pwzFormat* è **null**, \_ viene utilizzata la data shortdate come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="31de4-128">If you do not specify either DATE\_YEARMONTH, DATE\_SHORTDATE, or DATE\_LONGDATE, and *pwzFormat* is **NULL**, then DATE\_SHORTDATE is used as the default.</span></span>

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span data-ttu-id="31de4-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**impostazioni locali \_ NOUSEROVERRIDE**</span><span class="sxs-lookup"><span data-stu-id="31de4-129"><span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**LOCALE\_NOUSEROVERRIDE**</span></span>


</dt> <dd>

<span data-ttu-id="31de4-130">Se impostata, la funzione formatta la stringa utilizzando il formato di data predefinito del sistema per le impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="31de4-130">If set, the function formats the string using the system default date format for the specified locale.</span></span> <span data-ttu-id="31de4-131">Se non è impostato, la funzione formatta la stringa usando qualsiasi override utente nel formato di data predefinito delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="31de4-131">If not set, the function formats the string using any user overrides to the locale's default date format.</span></span>

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span data-ttu-id="31de4-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**impostazioni locali \_ usare \_ CP \_ ACP**</span><span class="sxs-lookup"><span data-stu-id="31de4-132"><span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**LOCALE\_USE\_CP\_ACP**</span></span>


</dt> <dd>

<span data-ttu-id="31de4-133">Usa la tabella codici ANSI di sistema per la conversione di stringhe anziché la tabella codici delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="31de4-133">Uses the system ANSI code page for string translation instead of the locale's code page.</span></span>

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span data-ttu-id="31de4-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**Data \_ SHORTDATE**</span><span class="sxs-lookup"><span data-stu-id="31de4-134"><span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**DATE\_SHORTDATE**</span></span>


</dt> <dd>

<span data-ttu-id="31de4-135">Usa il formato di data breve.</span><span class="sxs-lookup"><span data-stu-id="31de4-135">Uses the short date format.</span></span> <span data-ttu-id="31de4-136">Questo valore non può essere usato con la data \_ LONGDATE o la data \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="31de4-136">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span data-ttu-id="31de4-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**Data \_ LONGDATE**</span><span class="sxs-lookup"><span data-stu-id="31de4-137"><span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**DATE\_LONGDATE**</span></span>


</dt> <dd>

<span data-ttu-id="31de4-138">Usa il formato di data estesa.</span><span class="sxs-lookup"><span data-stu-id="31de4-138">Uses the long date format.</span></span> <span data-ttu-id="31de4-139">Questo valore non può essere usato con la data \_ shortdate o la data \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="31de4-139">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span>

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span data-ttu-id="31de4-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**Data \_ YEARMONTH**</span><span class="sxs-lookup"><span data-stu-id="31de4-140"><span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**DATE\_YEARMONTH**</span></span>


</dt> <dd>

<span data-ttu-id="31de4-141">Usa il formato anno/mese.</span><span class="sxs-lookup"><span data-stu-id="31de4-141">Uses the year/month format.</span></span> <span data-ttu-id="31de4-142">Questo valore non può essere usato con la data \_ shortdate o la data \_ LONGDATE.</span><span class="sxs-lookup"><span data-stu-id="31de4-142">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span>

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span data-ttu-id="31de4-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**Data \_ utilizzo \_ ALT \_ Calendario**</span><span class="sxs-lookup"><span data-stu-id="31de4-143"><span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**DATE\_USE\_ALT\_CALENDAR**</span></span>


</dt> <dd>

<span data-ttu-id="31de4-144">Usa il calendario alternativo, se esistente, per formattare la stringa di data.</span><span class="sxs-lookup"><span data-stu-id="31de4-144">Uses the alternate calendar, if one exists, to format the date string.</span></span> <span data-ttu-id="31de4-145">Se questo flag è impostato, la funzione utilizza il formato predefinito per quel calendario alternativo, anziché utilizzare qualsiasi override utente.</span><span class="sxs-lookup"><span data-stu-id="31de4-145">If this flag is set, the function uses the default format for that alternate calendar, rather than using any user overrides.</span></span> <span data-ttu-id="31de4-146">Le sostituzioni utente verranno utilizzate solo nel caso in cui non esista un formato predefinito per il calendario alternativo specificato.</span><span class="sxs-lookup"><span data-stu-id="31de4-146">The user overrides will be used only in the event that there is no default format for the specified alternate calendar.</span></span>

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span data-ttu-id="31de4-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**Data \_ LTRREADING**</span><span class="sxs-lookup"><span data-stu-id="31de4-147"><span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**DATE\_LTRREADING**</span></span>


</dt> <dd>

<span data-ttu-id="31de4-148">Aggiunge contrassegni per il layout di lettura da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="31de4-148">Adds marks for left-to-right reading layout.</span></span> <span data-ttu-id="31de4-149">Questo valore non può essere usato con la data \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="31de4-149">This value cannot be used with DATE\_RTLREADING.</span></span>

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span data-ttu-id="31de4-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**Data \_ RTLREADING**</span><span class="sxs-lookup"><span data-stu-id="31de4-150"><span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**DATE\_RTLREADING**</span></span>


</dt> <dd>

<span data-ttu-id="31de4-151">Aggiunge contrassegni per il layout di lettura da destra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="31de4-151">Adds marks for right-to-left reading layout.</span></span> <span data-ttu-id="31de4-152">Questo valore non può essere usato con la data \_ LTRREADING.</span><span class="sxs-lookup"><span data-stu-id="31de4-152">This value cannot be used with DATE\_LTRREADING.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="31de4-153">*lpDate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31de4-153">*lpDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31de4-154">Tipo: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _</span><span class="sxs-lookup"><span data-stu-id="31de4-154">Type: \**const [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)\** _</span></span>

<span data-ttu-id="31de4-155">Puntatore a una struttura [_ *SYSTEMTIME* \*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) che contiene le informazioni sulla data da formattare.</span><span class="sxs-lookup"><span data-stu-id="31de4-155">A pointer to a [_ *SYSTEMTIME*\*](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date information to be formatted.</span></span> <span data-ttu-id="31de4-156">Se questo puntatore è **null**, la funzione usa la data corrente del sistema locale.</span><span class="sxs-lookup"><span data-stu-id="31de4-156">If this pointer is **NULL**, the function uses the current local system date.</span></span>

</dd> <dt>

<span data-ttu-id="31de4-157">*pwzFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31de4-157">*pwzFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31de4-158">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="31de4-158">Type: **LPCWSTR**</span></span>

<span data-ttu-id="31de4-159">Puntatore a un'immagine di formato da utilizzare per formare la stringa di data.</span><span class="sxs-lookup"><span data-stu-id="31de4-159">A pointer to a format picture to use to form the date string.</span></span> <span data-ttu-id="31de4-160">Se *pwzFormat* è **null**, la funzione utilizza il formato di data delle impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="31de4-160">If *pwzFormat* is **NULL**, the function uses the date format of the specified locale.</span></span> <span data-ttu-id="31de4-161">Per ulteriori informazioni, vedere [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) .</span><span class="sxs-lookup"><span data-stu-id="31de4-161">See [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) for more details.</span></span>

</dd> <dt>

<span data-ttu-id="31de4-162">*pwzDateStr* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="31de4-162">*pwzDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31de4-163">Tipo: **LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="31de4-163">Type: **LPWSTR**</span></span>

<span data-ttu-id="31de4-164">Puntatore a un buffer che riceve la stringa di data formattata.</span><span class="sxs-lookup"><span data-stu-id="31de4-164">A pointer to a buffer that receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="31de4-165">*cchDate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31de4-165">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31de4-166">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="31de4-166">Type: **int**</span></span>

<span data-ttu-id="31de4-167">Specifica la dimensione, in caratteri, del buffer *pwzDateStr* .</span><span class="sxs-lookup"><span data-stu-id="31de4-167">Specifies the size, in characters, of the *pwzDateStr* buffer.</span></span> <span data-ttu-id="31de4-168">Se *cchDate* è zero, la funzione restituisce il numero di caratteri necessari per memorizzare la stringa di data formattata e il buffer a cui punta *pwzDateStr* non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="31de4-168">If *cchDate* is zero, the function returns the number of characters required to hold the formatted date string, and the buffer pointed to by *pwzDateStr* is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31de4-169">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31de4-169">Return value</span></span>

<span data-ttu-id="31de4-170">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="31de4-170">Type: **int**</span></span>

<span data-ttu-id="31de4-171">Se la funzione ha esito positivo, il valore restituito è il numero di caratteri scritti nel buffer a cui punta *pwzDateStr*.</span><span class="sxs-lookup"><span data-stu-id="31de4-171">If the function succeeds, the return value is the number of characters written to the buffer pointed to by *pwzDateStr*.</span></span> <span data-ttu-id="31de4-172">Se il parametro *cchDate* è zero, il valore restituito è il numero di caratteri necessari per conservare la stringa di data formattata.</span><span class="sxs-lookup"><span data-stu-id="31de4-172">If the *cchDate* parameter is zero, the return value is the number of characters required to hold the formatted date string.</span></span> <span data-ttu-id="31de4-173">Il conteggio include il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="31de4-173">The count includes the terminating null character.</span></span>

<span data-ttu-id="31de4-174">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="31de4-174">If the function fails, the return value is zero.</span></span> <span data-ttu-id="31de4-175">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="31de4-175">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="31de4-176">**GetLastError** può restituire uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="31de4-176">**GetLastError** may return one of the following error codes.</span></span>

<dl> <dt>

<span data-ttu-id="31de4-177">**ERRORE \_ buffer insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="31de4-177">**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dt>

<span data-ttu-id="31de4-178">**flag di errore \_ non validi \_**</span><span class="sxs-lookup"><span data-stu-id="31de4-178">**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dt>

<span data-ttu-id="31de4-179">**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31de4-179">**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="31de4-180">Commenti</span><span class="sxs-lookup"><span data-stu-id="31de4-180">Remarks</span></span>

<span data-ttu-id="31de4-181">**GetDateFormatWrapW** offre la possibilità di utilizzare stringhe Unicode nei sistemi operativi precedenti a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="31de4-181">**GetDateFormatWrapW** provides the ability to use Unicode strings in operating systems earlier than Windows XP.</span></span> <span data-ttu-id="31de4-182">Il metodo preferito consiste nell'usare [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) insieme a Microsoft Layer for Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="31de4-182">The preferred method is to use [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="31de4-183">**GetDateFormatWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 311.</span><span class="sxs-lookup"><span data-stu-id="31de4-183">**GetDateFormatWrapW** must be called directly from Shlwapi.dll, using ordinal 311.</span></span>

## <a name="requirements"></a><span data-ttu-id="31de4-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31de4-184">Requirements</span></span>



| <span data-ttu-id="31de4-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="31de4-185">Requirement</span></span> | <span data-ttu-id="31de4-186">Valore</span><span class="sxs-lookup"><span data-stu-id="31de4-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31de4-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31de4-187">Minimum supported client</span></span><br/> | <span data-ttu-id="31de4-188">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31de4-188">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31de4-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31de4-189">Minimum supported server</span></span><br/> | <span data-ttu-id="31de4-190">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31de4-190">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="31de4-191">DLL</span><span class="sxs-lookup"><span data-stu-id="31de4-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31de4-192"><dt>Shlwapi.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="31de4-192"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31de4-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31de4-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31de4-194">**GetDateFormat**</span><span class="sxs-lookup"><span data-stu-id="31de4-194">**GetDateFormat**</span></span>](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 

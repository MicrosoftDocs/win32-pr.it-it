---
description: Deprecato.
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: GetCalendarDateFormatEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarDateFormatEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: b0130bf62c742d0565b1c98c138ac8c71ddf7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312873"
---
# <a name="getcalendardateformatex-function"></a><span data-ttu-id="4b101-103">GetCalendarDateFormatEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="4b101-103">GetCalendarDateFormatEx function</span></span>

<span data-ttu-id="4b101-104">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4b101-104">Deprecated.</span></span> <span data-ttu-id="4b101-105">Recupera una stringa di data formattata correttamente per le impostazioni locali specificate utilizzando la data e il calendario specificati.</span><span class="sxs-lookup"><span data-stu-id="4b101-105">Retrieves a properly formatted date string for the specified locale using the specified date and calendar.</span></span> <span data-ttu-id="4b101-106">L'utente può specificare il formato di data breve, il formato di data estesa, il formato dell'anno mese o un modello di formato personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4b101-106">The user can specify the short date format, the long date format, the year month format, or a custom format pattern.</span></span>

> [!Note]  
> <span data-ttu-id="4b101-107">Questa funzione può recuperare i dati che cambiano tra le versioni, ad esempio, a causa di impostazioni locali personalizzate.</span><span class="sxs-lookup"><span data-stu-id="4b101-107">This function can retrieve data that changes between releases, for example, due to a custom locale.</span></span> <span data-ttu-id="4b101-108">Se l'applicazione deve persistere o trasmettere dati, vedere [utilizzo di dati locali permanenti](using-persistent-locale-data.md).</span><span class="sxs-lookup"><span data-stu-id="4b101-108">If your application must persist or transmit data, see [Using Persistent Locale Data](using-persistent-locale-data.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4b101-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b101-109">Syntax</span></span>


```C++
BOOL GetCalendarDateFormatEx(
  _In_        LPCWSTR       lpszLocale,
  _In_        DWORD         dwFlags,
  _In_  const LPCALDATETIME lpCalDateTime,
  _In_        LPCWSTR       lpFormat,
  _Out_       LPWSTR        lpDateStr,
  _In_        int           cchDate
);
```



## <a name="parameters"></a><span data-ttu-id="4b101-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b101-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b101-111">*lpszLocale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b101-111">*lpszLocale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b101-112">Puntatore a un nome delle impostazioni locali o uno dei seguenti valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="4b101-112">Pointer to a locale name, or one of the following predefined values.</span></span>

-   [<span data-ttu-id="4b101-113">nome delle impostazioni locali \_ \_ invariante</span><span class="sxs-lookup"><span data-stu-id="4b101-113">LOCALE\_NAME\_INVARIANT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="4b101-114">impostazioni locali \_ nome \_ sistema \_ predefinito</span><span class="sxs-lookup"><span data-stu-id="4b101-114">LOCALE\_NAME\_SYSTEM\_DEFAULT</span></span>](locale-name-constants.md)
-   [<span data-ttu-id="4b101-115">\_ \_ impostazione predefinita utente nome impostazioni locali \_</span><span class="sxs-lookup"><span data-stu-id="4b101-115">LOCALE\_NAME\_USER\_DEFAULT</span></span>](locale-name-constants.md)

</dd> <dt>

<span data-ttu-id="4b101-116">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b101-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b101-117">Flag che specificano le opzioni relative al formato della data.</span><span class="sxs-lookup"><span data-stu-id="4b101-117">Flags specifying date format options.</span></span> <span data-ttu-id="4b101-118">Se *lpFormat* non è impostato su **null**, questo parametro deve essere impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="4b101-118">If *lpFormat* is not set to **NULL**, this parameter must be set to 0.</span></span> <span data-ttu-id="4b101-119">Se *lpFormat* è impostato su **null**, l'applicazione può specificare una combinazione dei valori seguenti e delle [impostazioni locali \_ NOUSEROVERRIDE](locale-nouseroverride.md).</span><span class="sxs-lookup"><span data-stu-id="4b101-119">If *lpFormat* is set to **NULL**, the application can specify a combination of the following values and [LOCALE\_NOUSEROVERRIDE](locale-nouseroverride.md).</span></span>



| <span data-ttu-id="4b101-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4b101-120">Value</span></span>                                                                                                                                                               | <span data-ttu-id="4b101-121">Significato</span><span class="sxs-lookup"><span data-stu-id="4b101-121">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <span data-ttu-id="4b101-122"><dt>**Data \_ SHORTDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="4b101-122"><dt>**DATE\_SHORTDATE**</dt></span></span> </dl>    | <span data-ttu-id="4b101-123">Usare il formato di data breve.</span><span class="sxs-lookup"><span data-stu-id="4b101-123">Use the short date format.</span></span> <span data-ttu-id="4b101-124">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="4b101-124">This is the default.</span></span> <span data-ttu-id="4b101-125">Questo valore non può essere usato con la data \_ LONGDATE o la data \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="4b101-125">This value cannot be used with DATE\_LONGDATE or DATE\_YEARMONTH.</span></span> <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <span data-ttu-id="4b101-126"><dt>**Data \_ LONGDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="4b101-126"><dt>**DATE\_LONGDATE**</dt></span></span> </dl>       | <span data-ttu-id="4b101-127">Usare il formato di data estesa.</span><span class="sxs-lookup"><span data-stu-id="4b101-127">Use the long date format.</span></span> <span data-ttu-id="4b101-128">Questo valore non può essere usato con la data \_ shortdate o la data \_ YEARMONTH.</span><span class="sxs-lookup"><span data-stu-id="4b101-128">This value cannot be used with DATE\_SHORTDATE or DATE\_YEARMONTH.</span></span> <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <span data-ttu-id="4b101-129"><dt>**Data \_ YEARMONTH**</dt></span><span class="sxs-lookup"><span data-stu-id="4b101-129"><dt>**DATE\_YEARMONTH**</dt></span></span> </dl>    | <span data-ttu-id="4b101-130">Usare il formato anno/mese.</span><span class="sxs-lookup"><span data-stu-id="4b101-130">Use the year/month format.</span></span> <span data-ttu-id="4b101-131">Questo valore non può essere usato con la data \_ shortdate o la data \_ LONGDATE.</span><span class="sxs-lookup"><span data-stu-id="4b101-131">This value cannot be used with DATE\_SHORTDATE or DATE\_LONGDATE.</span></span><br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <span data-ttu-id="4b101-132"><dt>**Data \_ LTRREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="4b101-132"><dt>**DATE\_LTRREADING**</dt></span></span> </dl> | <span data-ttu-id="4b101-133">Aggiungere i contrassegni per il layout di lettura da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="4b101-133">Add marks for left-to-right reading layout.</span></span> <span data-ttu-id="4b101-134">Questo valore non può essere usato con la data \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="4b101-134">This value cannot be used with DATE\_RTLREADING.</span></span><br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <span data-ttu-id="4b101-135"><dt>**Data \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="4b101-135"><dt>**DATE\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="4b101-136">Aggiungere contrassegni per il layout di lettura da destra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="4b101-136">Add marks for right-to-left reading layout.</span></span> <span data-ttu-id="4b101-137">Non è possibile usare questo valore con DATE \_ LTRREADING</span><span class="sxs-lookup"><span data-stu-id="4b101-137">This value cannot be used with DATE\_LTRREADING</span></span><br/>                        |



 

</dd> <dt>

<span data-ttu-id="4b101-138">*lpCalDateTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b101-138">*lpCalDateTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b101-139">Puntatore a una struttura [**CALDATETIME**](caldatetime.md) che contiene le informazioni sulla data e sul calendario da formattare.</span><span class="sxs-lookup"><span data-stu-id="4b101-139">Pointer to a [**CALDATETIME**](caldatetime.md) structure that contains the date and calendar information to format.</span></span>

</dd> <dt>

<span data-ttu-id="4b101-140">*lpFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b101-140">*lpFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b101-141">Puntatore a una stringa di immagine del formato utilizzata per formare la stringa di data.</span><span class="sxs-lookup"><span data-stu-id="4b101-141">Pointer to a format picture string that is used to form the date string.</span></span> <span data-ttu-id="4b101-142">I valori possibili per la stringa dell'immagine di formato sono definiti nelle [Immagini del formato giorno, mese, anno ed era](day--month--year--and-era-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="4b101-142">Possible values for the format picture string are defined in [Day, Month, Year, and Era Format Pictures](day--month--year--and-era-format-pictures.md).</span></span>

<span data-ttu-id="4b101-143">La stringa di formato dell'immagine deve essere con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="4b101-143">The format picture string must be null-terminated.</span></span> <span data-ttu-id="4b101-144">La funzione utilizza le impostazioni locali solo per le informazioni non specificate nella stringa dell'immagine di formato, ad esempio i nomi dei giorni e dei mesi per le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="4b101-144">The function uses the locale only for information not specified in the format picture string, for example, the day and month names for the locale.</span></span> <span data-ttu-id="4b101-145">Se la funzione usa il formato di data delle impostazioni locali specificate, l'applicazione imposta questo parametro su **null** .</span><span class="sxs-lookup"><span data-stu-id="4b101-145">The application sets this parameter to **NULL** if the function is to use the date format of the specified locale.</span></span>

</dd> <dt>

<span data-ttu-id="4b101-146">*lpDateStr* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4b101-146">*lpDateStr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b101-147">Puntatore a un buffer in cui questa funzione riceve la stringa di data formattata.</span><span class="sxs-lookup"><span data-stu-id="4b101-147">Pointer to a buffer in which this function receives the formatted date string.</span></span>

</dd> <dt>

<span data-ttu-id="4b101-148">*cchDate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b101-148">*cchDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b101-149">Dimensione, in caratteri, del buffer *lpDateStr* .</span><span class="sxs-lookup"><span data-stu-id="4b101-149">Size, in characters, of the *lpDateStr* buffer.</span></span> <span data-ttu-id="4b101-150">In alternativa, l'applicazione può impostare questo parametro su 0.</span><span class="sxs-lookup"><span data-stu-id="4b101-150">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="4b101-151">In questo caso, la funzione restituisce il numero di caratteri necessari per conservare la stringa di data formattata e il parametro *lpDateStr* non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="4b101-151">In this case, the function returns the number of characters required to hold the formatted date string, and the *lpDateStr* parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b101-152">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b101-152">Return value</span></span>

<span data-ttu-id="4b101-153">Restituisce il numero di caratteri scritti nel buffer *lpDateStr* in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4b101-153">Returns the number of characters written to the *lpDateStr* buffer if successful.</span></span> <span data-ttu-id="4b101-154">Se il parametro *cchDate* è impostato su 0, la funzione restituisce il numero di caratteri necessari per conservare la stringa di data formattata, incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="4b101-154">If the *cchDate* parameter is set to 0, the function returns the number of characters required to hold the formatted date string, including the terminating null character.</span></span>

<span data-ttu-id="4b101-155">Questa funzione restituisce 0 in caso di esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4b101-155">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="4b101-156">Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b101-156">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="4b101-157">\_Data di errore non \_ compresa nell' \_ \_ intervallo.</span><span class="sxs-lookup"><span data-stu-id="4b101-157">ERROR\_DATE\_OUT\_OF\_RANGE.</span></span> <span data-ttu-id="4b101-158">La data specificata non è compresa nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="4b101-158">The specified date was out of range.</span></span>
-   <span data-ttu-id="4b101-159">ERRORE \_ \_ nel buffer insufficiente.</span><span class="sxs-lookup"><span data-stu-id="4b101-159">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="4b101-160">Una dimensione del buffer specificata non è sufficientemente grande oppure è stata impostata erroneamente su **null**.</span><span class="sxs-lookup"><span data-stu-id="4b101-160">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="4b101-161">flag di errore \_ non validi \_ .</span><span class="sxs-lookup"><span data-stu-id="4b101-161">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="4b101-162">I valori specificati per i flag non sono validi.</span><span class="sxs-lookup"><span data-stu-id="4b101-162">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="4b101-163">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="4b101-163">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="4b101-164">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="4b101-164">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b101-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b101-165">Remarks</span></span>

<span data-ttu-id="4b101-166">La data meno recente supportata da questa funzione è il 1 gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="4b101-166">The earliest date supported by this function is January 1, 1601.</span></span>

<span data-ttu-id="4b101-167">A questa funzione non è associato un file di intestazione o un file di libreria.</span><span class="sxs-lookup"><span data-stu-id="4b101-167">This function does not have an associated header file or library file.</span></span> <span data-ttu-id="4b101-168">L'applicazione può chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della DLL (Kernel32.dll) per ottenere un handle del modulo.</span><span class="sxs-lookup"><span data-stu-id="4b101-168">The application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Kernel32.dll) to obtain a module handle.</span></span> <span data-ttu-id="4b101-169">Può quindi chiamare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con tale handle del modulo e il nome di questa funzione per ottenere l'indirizzo della funzione.</span><span class="sxs-lookup"><span data-stu-id="4b101-169">It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the name of this function to get the function address.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b101-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b101-170">Requirements</span></span>



| <span data-ttu-id="4b101-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b101-171">Requirement</span></span> | <span data-ttu-id="4b101-172">Valore</span><span class="sxs-lookup"><span data-stu-id="4b101-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b101-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b101-173">Minimum supported client</span></span><br/> | <span data-ttu-id="4b101-174">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b101-174">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4b101-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b101-175">Minimum supported server</span></span><br/> | <span data-ttu-id="4b101-176">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4b101-176">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b101-177">DLL</span><span class="sxs-lookup"><span data-stu-id="4b101-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b101-178"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b101-178"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b101-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b101-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b101-180">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="4b101-180">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="4b101-181">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="4b101-181">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="4b101-182">Immagini del formato giorno, mese, anno ed era</span><span class="sxs-lookup"><span data-stu-id="4b101-182">Day, Month, Year, and Era Format Pictures</span></span>](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[<span data-ttu-id="4b101-183">NLS: esempio di API basate su nome</span><span class="sxs-lookup"><span data-stu-id="4b101-183">NLS: Name-based APIs Sample</span></span>](nls--name-based-apis-sample.md)
</dt> <dt>

[<span data-ttu-id="4b101-184">**EnumDateFormatsExEx**</span><span class="sxs-lookup"><span data-stu-id="4b101-184">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[<span data-ttu-id="4b101-185">**GetDateFormat**</span><span class="sxs-lookup"><span data-stu-id="4b101-185">**GetDateFormat**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[<span data-ttu-id="4b101-186">**GetDateFormatEx**</span><span class="sxs-lookup"><span data-stu-id="4b101-186">**GetDateFormatEx**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[<span data-ttu-id="4b101-187">**CALDATETIME**</span><span class="sxs-lookup"><span data-stu-id="4b101-187">**CALDATETIME**</span></span>](caldatetime.md)
</dt> </dl>

 

 

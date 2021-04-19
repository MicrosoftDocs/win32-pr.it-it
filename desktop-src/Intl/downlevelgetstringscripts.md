---
description: Fornisce un elenco di script utilizzati nella stringa Unicode specificata.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: Funzione DownlevelGetStringScripts (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: bc5a9fdaf3beb9e1c401943f923fa48bd9d4b44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317163"
---
# <a name="downlevelgetstringscripts-function"></a><span data-ttu-id="77435-103">DownlevelGetStringScripts (funzione)</span><span class="sxs-lookup"><span data-stu-id="77435-103">DownlevelGetStringScripts function</span></span>

<span data-ttu-id="77435-104">Fornisce un elenco di script utilizzati nella stringa Unicode specificata.</span><span class="sxs-lookup"><span data-stu-id="77435-104">Provides a list of scripts used in the specified Unicode string.</span></span>

> [!Note]  
> <span data-ttu-id="77435-105">Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="77435-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="77435-106">Il relativo utilizzo richiede il pacchetto di download.</span><span class="sxs-lookup"><span data-stu-id="77435-106">Its use requires the download package.</span></span> <span data-ttu-id="77435-107">Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).</span><span class="sxs-lookup"><span data-stu-id="77435-107">Applications that only run on Windows Vista and later should call [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="77435-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77435-108">Syntax</span></span>


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="77435-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="77435-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77435-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77435-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77435-111">Flag che specificano le opzioni per il recupero di script.</span><span class="sxs-lookup"><span data-stu-id="77435-111">Flags specifying options for script retrieval.</span></span>



| <span data-ttu-id="77435-112">Valore</span><span class="sxs-lookup"><span data-stu-id="77435-112">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="77435-113">Significato</span><span class="sxs-lookup"><span data-stu-id="77435-113">Meaning</span></span>                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <span data-ttu-id="77435-114"><dt>**GSS \_ Consenti \_ ereditato \_ comune**</dt></span><span class="sxs-lookup"><span data-stu-id="77435-114"><dt>**GSS\_ALLOW\_INHERITED\_COMMON**</dt></span></span> </dl> | <span data-ttu-id="77435-115">Recuperare le informazioni sullo script "Qaii" (ereditato) e "Rachele" (comune).</span><span class="sxs-lookup"><span data-stu-id="77435-115">Retrieve "Qaii" (INHERITED) and "Zyyy" (COMMON) script information.</span></span> <span data-ttu-id="77435-116">Questo valore non influisce sull'elaborazione di caratteri non assegnati.</span><span class="sxs-lookup"><span data-stu-id="77435-116">This value does not affect the processing of unassigned characters.</span></span> <span data-ttu-id="77435-117">Questi caratteri nella stringa di input determinano sempre la visualizzazione di un "ZZZZ" (script non assegnato) nella stringa di script.</span><span class="sxs-lookup"><span data-stu-id="77435-117">These characters in the input string always cause a "Zzzz" (UNASSIGNED script) to appear in the script string.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="77435-118">Per impostazione predefinita, questa funzione ignora tutti i caratteri comuni o ereditati nella stringa Unicode di input.</span><span class="sxs-lookup"><span data-stu-id="77435-118">By default, this function ignores any inherited or common characters in the input Unicode string.</span></span> <span data-ttu-id="77435-119">Se GSS \_ Consenti \_ ereditato \_ Common non è impostato, non verrà visualizzato né "Qaii" né "Rachele" nella stringa dello script, anche se la stringa di input contiene tali caratteri.</span><span class="sxs-lookup"><span data-stu-id="77435-119">If GSS\_ALLOW\_INHERITED\_COMMON is not set, neither "Qaii" nor "Zyyy" will appear in the script string, even if the input string contains such characters.</span></span> <span data-ttu-id="77435-120">Se GSS \_ Consenti \_ ereditato \_ Common è impostato e se la stringa di input contiene caratteri ereditati e/o comuni, nella stringa dello script vengono visualizzati "Qaii" e/o "Rachele".</span><span class="sxs-lookup"><span data-stu-id="77435-120">If GSS\_ALLOW\_INHERITED\_COMMON is set, and if the input string contains inherited and/or common characters, "Qaii" and/or "Zyyy" appear in the script string.</span></span> <span data-ttu-id="77435-121">Vedere la sezione relativa alle osservazioni.</span><span class="sxs-lookup"><span data-stu-id="77435-121">See the Remarks section.</span></span>

 

</dd> <dt>

<span data-ttu-id="77435-122">*lpString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77435-122">*lpString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77435-123">Puntatore alla stringa Unicode da analizzare.</span><span class="sxs-lookup"><span data-stu-id="77435-123">Pointer to the Unicode string to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="77435-124">*cchString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77435-124">*cchString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77435-125">Dimensione, in caratteri, della stringa Unicode indicata da *lpString*.</span><span class="sxs-lookup"><span data-stu-id="77435-125">Size, in characters, of the Unicode string indicated by *lpString*.</span></span> <span data-ttu-id="77435-126">L'applicazione imposta questo parametro su-1 se la stringa è con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="77435-126">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="77435-127">Se l'applicazione imposta questo parametro su 0, la funzione recupera una stringa Unicode null (L " \\ 0") in *lpScripts* e restituisce 1.</span><span class="sxs-lookup"><span data-stu-id="77435-127">If the application sets this parameter to 0, the function retrieves a null Unicode string (L"\\0") in *lpScripts* and returns 1.</span></span>

</dd> <dt>

<span data-ttu-id="77435-128">*lpScripts* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="77435-128">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77435-129">Puntatore a un buffer in cui questa funzione recupera una stringa a terminazione null che rappresenta un elenco di script, usando la notazione di 4 caratteri usata nello standard [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="77435-129">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="77435-130">Ogni nome di script è costituito da quattro caratteri latini e i nomi vengono recuperati in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="77435-130">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="77435-131">Ogni nome, incluso l'ultimo, è seguito da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="77435-131">Each name, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="77435-132">In alternativa, questo parametro può contenere **null** se *cchScripts* è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="77435-132">Alternatively, this parameter can contain **NULL** if *cchScripts* set to 0.</span></span> <span data-ttu-id="77435-133">In questo caso, la funzione restituisce la dimensione richiesta per il buffer di script.</span><span class="sxs-lookup"><span data-stu-id="77435-133">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="77435-134">*cchScripts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77435-134">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77435-135">Dimensione, in caratteri, del buffer di script indicato da *lpScripts*.</span><span class="sxs-lookup"><span data-stu-id="77435-135">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="77435-136">In alternativa, l'applicazione può impostare questo parametro su 0.</span><span class="sxs-lookup"><span data-stu-id="77435-136">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="77435-137">In questo caso, la funzione recupera il **valore null** in *lpScripts* e restituisce la dimensione richiesta per il buffer di script.</span><span class="sxs-lookup"><span data-stu-id="77435-137">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77435-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="77435-138">Return value</span></span>

<span data-ttu-id="77435-139">Restituisce il numero di caratteri recuperati nel buffer di output, incluso un carattere di terminazione null, se ha esito positivo e *cchScripts* è impostato su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="77435-139">Returns the number of characters retrieved in the output buffer, including a terminating null character, if successful and *cchScripts* is set to a nonzero value.</span></span> <span data-ttu-id="77435-140">La funzione restituisce 1 per indicare che non è stato trovato alcuno script, ad esempio quando la stringa di input contiene solo caratteri comuni o EREDITAti e GSS \_ Consenti \_ ereditato \_ comune non è impostato.</span><span class="sxs-lookup"><span data-stu-id="77435-140">The function returns 1 to indicate that no script has been found, for example, when the input string only contains COMMON or INHERITED characters and GSS\_ALLOW\_INHERITED\_COMMON is not set.</span></span> <span data-ttu-id="77435-141">Dato che ogni script trovato aggiunge cinque caratteri (quattro caratteri + delimitatore), una semplice operazione matematica fornisce il conteggio degli script come ( \_ codice restituito-1)/5.</span><span class="sxs-lookup"><span data-stu-id="77435-141">Given that each found script adds five characters (four characters + delimiter), a simple mathematical operation provides the script count as (return\_code - 1) / 5.</span></span>

<span data-ttu-id="77435-142">Se la funzione ha esito positivo e il valore di *cchScripts* è 0, il valore restituito è la dimensione richiesta, in caratteri che include un carattere null di terminazione, per il buffer di script.</span><span class="sxs-lookup"><span data-stu-id="77435-142">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span> <span data-ttu-id="77435-143">Il numero di script è come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="77435-143">The script count is as described above.</span></span>

<span data-ttu-id="77435-144">Se l'operazione non riesce, la funzione restituisce 0.</span><span class="sxs-lookup"><span data-stu-id="77435-144">The function returns 0 if it does not succeed.</span></span> <span data-ttu-id="77435-145">Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="77435-145">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="77435-146">ERRORE \_ BADDB.</span><span class="sxs-lookup"><span data-stu-id="77435-146">ERROR\_BADDB.</span></span> <span data-ttu-id="77435-147">La funzione non è stata in grado di accedere ai dati.</span><span class="sxs-lookup"><span data-stu-id="77435-147">The function could not access the data.</span></span> <span data-ttu-id="77435-148">Questa situazione non dovrebbe in genere verificarsi e in genere indica un'installazione non valida, un problema del disco o un tipo simile.</span><span class="sxs-lookup"><span data-stu-id="77435-148">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="77435-149">ERRORE \_ \_ nel buffer insufficiente.</span><span class="sxs-lookup"><span data-stu-id="77435-149">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="77435-150">Una dimensione del buffer specificata non è sufficientemente grande oppure è stata impostata erroneamente su **null**.</span><span class="sxs-lookup"><span data-stu-id="77435-150">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="77435-151">flag di errore \_ non validi \_ .</span><span class="sxs-lookup"><span data-stu-id="77435-151">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="77435-152">I valori specificati per i flag non sono validi.</span><span class="sxs-lookup"><span data-stu-id="77435-152">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="77435-153">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="77435-153">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="77435-154">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="77435-154">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="77435-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="77435-155">Remarks</span></span>

<span data-ttu-id="77435-156">Questa funzione è utile come parte di una strategia per attenuare i problemi di sicurezza correlati ai [nomi di dominio internazionali (IDN)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="77435-156">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="77435-157">La determinazione degli script si basa sui valori di script pubblicati dal Consorzio Unicode in <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> , ad eccezione del fatto che i caratteri non assegnati hanno il valore "ZZZZ" (non assegnato) invece di "Rachele" (comune).</span><span class="sxs-lookup"><span data-stu-id="77435-157">The script determination is based on the script values published by the Unicode Consortium in <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt>, except that the unassigned characters have the value "Zzzz" (UNASSIGNED) instead of "Zyyy" (COMMON).</span></span>

<span data-ttu-id="77435-158">Di seguito sono riportati alcuni esempi del comportamento di questa funzione:</span><span class="sxs-lookup"><span data-stu-id="77435-158">Here are some examples of the behavior of this function:</span></span>



<span data-ttu-id="77435-159">Stringa di input</span><span class="sxs-lookup"><span data-stu-id="77435-159">Input string</span></span>

<span data-ttu-id="77435-160">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="77435-160">*dwFlags*</span></span>

<span data-ttu-id="77435-161">*lpScripts*</span><span class="sxs-lookup"><span data-stu-id="77435-161">*lpScripts*</span></span>

<span data-ttu-id="77435-162">Script</span><span class="sxs-lookup"><span data-stu-id="77435-162">Scripts</span></span>

<span data-ttu-id="77435-163">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="77435-163">Microsoft.com</span></span>

<span data-ttu-id="77435-164">0</span><span class="sxs-lookup"><span data-stu-id="77435-164">0</span></span>

<span data-ttu-id="77435-165">Latn</span><span class="sxs-lookup"><span data-stu-id="77435-165">Latn;</span></span>

<span data-ttu-id="77435-166">Latino</span><span class="sxs-lookup"><span data-stu-id="77435-166">Latin</span></span>

<span data-ttu-id="77435-167">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="77435-167">Microsoft.com</span></span>

<span data-ttu-id="77435-168">GSS \_ Consenti \_ ereditato \_ comune</span><span class="sxs-lookup"><span data-stu-id="77435-168">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="77435-169">Latn Rachele</span><span class="sxs-lookup"><span data-stu-id="77435-169">Latn;Zyyy;</span></span>

<span data-ttu-id="77435-170">Latino + comune</span><span class="sxs-lookup"><span data-stu-id="77435-170">Latin + Common</span></span>

<span data-ttu-id="77435-171">$ {ROWSPAN2} $Ni ño $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77435-171">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="77435-172">004E 0069 0241 006F</span><span class="sxs-lookup"><span data-stu-id="77435-172">004E 0069 0241 006F</span></span>

<span data-ttu-id="77435-173">$ {ROWSPAN2} $GSS \_ consentire \_ il \_ comune ereditato $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="77435-173">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="77435-174">$ {ROWSPAN2} $Latn; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77435-174">${ROWSPAN2}$Latn;${REMOVE}$</span></span>  

<span data-ttu-id="77435-175">$ {ROWSPAN2} $Latin $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77435-175">${ROWSPAN2}$Latin${REMOVE}$</span></span>  

<span data-ttu-id="77435-176">Usa la lettera latina MINUSCOLa N con TILDE</span><span class="sxs-lookup"><span data-stu-id="77435-176">Uses LATIN SMALL LETTER N WITH TILDE</span></span>

<span data-ttu-id="77435-177">$ {ROWSPAN2} $Ni ño $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77435-177">${ROWSPAN2}$Niño${REMOVE}$</span></span>  

<span data-ttu-id="77435-178">004E 0069 006E 0303 006F</span><span class="sxs-lookup"><span data-stu-id="77435-178">004E 0069 006E 0303 006F</span></span>

<span data-ttu-id="77435-179">$ {ROWSPAN2} $GSS \_ consentire \_ il \_ comune ereditato $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="77435-179">${ROWSPAN2}$GSS\_ALLOW\_INHERITED\_COMMON${REMOVE}$</span></span>  

<span data-ttu-id="77435-180">$ {ROWSPAN2} $Latn; Qaii; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77435-180">${ROWSPAN2}$Latn;Qaii;${REMOVE}$</span></span>  

<span data-ttu-id="77435-181">$ {ROWSPAN2} $Latin + ereditato $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77435-181">${ROWSPAN2}$Latin + Inherited${REMOVE}$</span></span>  

<span data-ttu-id="77435-182">Usa la combinazione TILDE</span><span class="sxs-lookup"><span data-stu-id="77435-182">Uses COMBINING TILDE</span></span>

<span data-ttu-id="77435-183">$ {ROWSPAN2} $Sp ооf $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77435-183">${ROWSPAN2}$Spооf${REMOVE}$</span></span>  

<span data-ttu-id="77435-184">0053 0070 043e 043e 0066</span><span class="sxs-lookup"><span data-stu-id="77435-184">0053 0070 043e 043e 0066</span></span>

<span data-ttu-id="77435-185">$ {ROWSPAN2} $0 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77435-185">${ROWSPAN2}$0${REMOVE}$</span></span>  

<span data-ttu-id="77435-186">$ {ROWSPAN2} $Latn; Cyrl; $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77435-186">${ROWSPAN2}$Latn;Cyrl;${REMOVE}$</span></span>  

<span data-ttu-id="77435-187">$ {ROWSPAN2} $Latin + Cirillico $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="77435-187">${ROWSPAN2}$Latin + Cyrillic${REMOVE}$</span></span>  

<span data-ttu-id="77435-188">Usa la lettera MINUSCOLa cirillico O</span><span class="sxs-lookup"><span data-stu-id="77435-188">Uses CYRILLIC SMALL LETTER O</span></span>

<span data-ttu-id="77435-189"></span><span class="sxs-lookup"><span data-stu-id="77435-189"></span></span>

<span data-ttu-id="77435-190">U + F000</span><span class="sxs-lookup"><span data-stu-id="77435-190">U+f000</span></span>

<span data-ttu-id="77435-191">0</span><span class="sxs-lookup"><span data-stu-id="77435-191">0</span></span>

<span data-ttu-id="77435-192">ZZZZ</span><span class="sxs-lookup"><span data-stu-id="77435-192">Zzzz;</span></span>

<span data-ttu-id="77435-193">Unassigned (Non assegnato)</span><span class="sxs-lookup"><span data-stu-id="77435-193">Unassigned</span></span>

<span data-ttu-id="77435-194"></span><span class="sxs-lookup"><span data-stu-id="77435-194"></span></span>

<span data-ttu-id="77435-195">U + F000</span><span class="sxs-lookup"><span data-stu-id="77435-195">U+f000</span></span>

<span data-ttu-id="77435-196">GSS \_ Consenti \_ ereditato \_ comune</span><span class="sxs-lookup"><span data-stu-id="77435-196">GSS\_ALLOW\_INHERITED\_COMMON</span></span>

<span data-ttu-id="77435-197">ZZZZ</span><span class="sxs-lookup"><span data-stu-id="77435-197">Zzzz;</span></span>

<span data-ttu-id="77435-198">Unassigned (Non assegnato)</span><span class="sxs-lookup"><span data-stu-id="77435-198">Unassigned</span></span>



 

<span data-ttu-id="77435-199">Il file di intestazione e la DLL necessari fanno parte del download di ["API di mitigazione del nome di dominio Microsoft (IDN)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) , disponibile nell' [area download MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="77435-199">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="77435-200">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77435-200">Requirements</span></span>



| <span data-ttu-id="77435-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="77435-201">Requirement</span></span> | <span data-ttu-id="77435-202">Valore</span><span class="sxs-lookup"><span data-stu-id="77435-202">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77435-203">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77435-203">Minimum supported client</span></span><br/> | <span data-ttu-id="77435-204">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="77435-204">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="77435-205">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77435-205">Minimum supported server</span></span><br/> | <span data-ttu-id="77435-206">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77435-206">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="77435-207">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="77435-207">Redistributable</span></span><br/>          | <span data-ttu-id="77435-208">API di mitigazione Microsoft per il nome di dominio internazionale (IDN) in Windows XP (SP2 o versioni successive), Windows Server 2003 (SP1 o versione successiva) o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77435-208">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="77435-209">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77435-209">Header</span></span><br/>                   | <dl> <span data-ttu-id="77435-210"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77435-210"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="77435-211">DLL</span><span class="sxs-lookup"><span data-stu-id="77435-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77435-212"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77435-212"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="77435-213">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77435-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77435-214">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="77435-214">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="77435-215">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="77435-215">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="77435-216">Gestione dei nomi di dominio internazionalizzati (IDN)</span><span class="sxs-lookup"><span data-stu-id="77435-216">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="77435-217">**DownlevelGetLocaleScripts**</span><span class="sxs-lookup"><span data-stu-id="77435-217">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="77435-218">**DownlevelVerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="77435-218">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="77435-219">**GetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="77435-219">**GetStringScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 

---
description: Confronta due stringhe di caratteri Unicode, usando le impostazioni locali specificate.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: CompareStringWrapW (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 0731182f5c01ad56db722972628d2cbe39373835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977383"
---
# <a name="comparestringwrapw-function"></a><span data-ttu-id="72b83-103">CompareStringWrapW (funzione)</span><span class="sxs-lookup"><span data-stu-id="72b83-103">CompareStringWrapW function</span></span>

<span data-ttu-id="72b83-104">\[**CompareStringWrapW** è disponibile per l'utilizzo in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="72b83-104">\[**CompareStringWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="72b83-105">Non sarà disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="72b83-105">It will not be available in subsequent versions.</span></span> <span data-ttu-id="72b83-106">È consigliabile usare [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) al suo posto.\]</span><span class="sxs-lookup"><span data-stu-id="72b83-106">You should use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in its place.\]</span></span>

<span data-ttu-id="72b83-107">Confronta due stringhe di caratteri Unicode, usando le impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="72b83-107">Compares two Unicode character strings, using a specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="72b83-108">**CompareStringWrapW** è un wrapper per la funzione **CompareStringW** .</span><span class="sxs-lookup"><span data-stu-id="72b83-108">**CompareStringWrapW** is a wrapper for the **CompareStringW** function.</span></span> <span data-ttu-id="72b83-109">Per ulteriori note sull'utilizzo, vedere la pagina [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) .</span><span class="sxs-lookup"><span data-stu-id="72b83-109">See the [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) page for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="72b83-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72b83-110">Syntax</span></span>


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a><span data-ttu-id="72b83-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="72b83-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72b83-112">*Impostazioni locali* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72b83-112">*Locale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72b83-113">Tipo: **LCID**</span><span class="sxs-lookup"><span data-stu-id="72b83-113">Type: **LCID**</span></span>

<span data-ttu-id="72b83-114">Identificatore delle impostazioni locali utilizzato per il confronto.</span><span class="sxs-lookup"><span data-stu-id="72b83-114">A locale identifier used for the comparison.</span></span> <span data-ttu-id="72b83-115">Questo parametro può essere uno dei seguenti identificatori delle impostazioni locali predefiniti o un identificatore delle impostazioni locali creato dalla macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) .</span><span class="sxs-lookup"><span data-stu-id="72b83-115">This parameter can be one of the following predefined locale identifiers or a locale identifier created by the [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) macro.</span></span>

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span data-ttu-id="72b83-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**impostazioni locali del \_ sistema \_**</span><span class="sxs-lookup"><span data-stu-id="72b83-116"><span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE\_SYSTEM\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="72b83-117">Impostazioni locali predefinite del sistema.</span><span class="sxs-lookup"><span data-stu-id="72b83-117">The system's default locale.</span></span>

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span data-ttu-id="72b83-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_impostazione predefinita utente impostazioni locali \_**</span><span class="sxs-lookup"><span data-stu-id="72b83-118"><span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE\_USER\_DEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="72b83-119">Impostazioni locali predefinite dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="72b83-119">The current user's default locale.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="72b83-120">*dwCmpFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72b83-120">*dwCmpFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72b83-121">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="72b83-121">Type: **DWORD**</span></span>

<span data-ttu-id="72b83-122">Flag che indicano il modo in cui la funzione Confronta le due stringhe.</span><span class="sxs-lookup"><span data-stu-id="72b83-122">The flags that indicate how the function compares the two strings.</span></span> <span data-ttu-id="72b83-123">Per impostazione predefinita, questi flag non sono impostati.</span><span class="sxs-lookup"><span data-stu-id="72b83-123">By default, these flags are not set.</span></span> <span data-ttu-id="72b83-124">Impostare su zero per ottenere il comportamento predefinito o per qualsiasi combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="72b83-124">Set to zero to get the default behavior or to any combination of the following values.</span></span>

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span data-ttu-id="72b83-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**\_IgnoreCase Norm**</span><span class="sxs-lookup"><span data-stu-id="72b83-125"><span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**NORM\_IGNORECASE**</span></span>


</dt> <dd>

<span data-ttu-id="72b83-126">Ignora maiuscole/minuscole.</span><span class="sxs-lookup"><span data-stu-id="72b83-126">Ignore case.</span></span>

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span data-ttu-id="72b83-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**\_IGNOREKANATYPE Norm**</span><span class="sxs-lookup"><span data-stu-id="72b83-127"><span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**NORM\_IGNOREKANATYPE**</span></span>


</dt> <dd>

<span data-ttu-id="72b83-128">Non distinguere tra caratteri Hiragana e katakana.</span><span class="sxs-lookup"><span data-stu-id="72b83-128">Do not differentiate between Hiragana and Katakana characters.</span></span> <span data-ttu-id="72b83-129">I caratteri Hiragana e Katakana corrispondenti vengono considerati uguali.</span><span class="sxs-lookup"><span data-stu-id="72b83-129">Corresponding Hiragana and Katakana characters compare as equal.</span></span>

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span data-ttu-id="72b83-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**\_IGNORENONSPACE Norm**</span><span class="sxs-lookup"><span data-stu-id="72b83-130"><span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**NORM\_IGNORENONSPACE**</span></span>


</dt> <dd>

<span data-ttu-id="72b83-131">Ignora caratteri senza spaziatura.</span><span class="sxs-lookup"><span data-stu-id="72b83-131">Ignore nonspacing characters.</span></span>

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span data-ttu-id="72b83-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**\_IGNORESYMBOLS Norm**</span><span class="sxs-lookup"><span data-stu-id="72b83-132"><span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**NORM\_IGNORESYMBOLS**</span></span>


</dt> <dd>

<span data-ttu-id="72b83-133">Ignorare i simboli.</span><span class="sxs-lookup"><span data-stu-id="72b83-133">Ignore symbols.</span></span>

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span data-ttu-id="72b83-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**\_IGNOREWIDTH Norm**</span><span class="sxs-lookup"><span data-stu-id="72b83-134"><span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**NORM\_IGNOREWIDTH**</span></span>


</dt> <dd>

<span data-ttu-id="72b83-135">Non distinguere tra un carattere a byte singolo e lo stesso carattere di un carattere a byte doppio.</span><span class="sxs-lookup"><span data-stu-id="72b83-135">Do not differentiate between a single-byte character and the same character as a double-byte character.</span></span>

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span data-ttu-id="72b83-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**Ordina \_ STRINGSORT**</span><span class="sxs-lookup"><span data-stu-id="72b83-136"><span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**SORT\_STRINGSORT**</span></span>


</dt> <dd>

<span data-ttu-id="72b83-137">Considera la punteggiatura uguale ai simboli.</span><span class="sxs-lookup"><span data-stu-id="72b83-137">Treat punctuation the same as symbols.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="72b83-138">*lpString1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72b83-138">*lpString1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72b83-139">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="72b83-139">Type: **LPCWSTR**</span></span>

<span data-ttu-id="72b83-140">Puntatore alla prima stringa Unicode da confrontare.</span><span class="sxs-lookup"><span data-stu-id="72b83-140">A pointer to the first Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="72b83-141">*cchCount1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72b83-141">*cchCount1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72b83-142">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="72b83-142">Type: **int**</span></span>

<span data-ttu-id="72b83-143">Numero di caratteri nella stringa a cui punta il parametro *lpString1* .</span><span class="sxs-lookup"><span data-stu-id="72b83-143">The number of characters in the string pointed to by the *lpString1* parameter.</span></span> <span data-ttu-id="72b83-144">Il conteggio non include il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="72b83-144">The count does not include the terminating null character.</span></span> <span data-ttu-id="72b83-145">Se questo parametro è un valore negativo, si presuppone che la stringa sia con terminazione null e che la lunghezza venga calcolata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="72b83-145">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> <dt>

<span data-ttu-id="72b83-146">*lpString2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72b83-146">*lpString2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72b83-147">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="72b83-147">Type: **LPCWSTR**</span></span>

<span data-ttu-id="72b83-148">Puntatore alla seconda stringa Unicode da confrontare.</span><span class="sxs-lookup"><span data-stu-id="72b83-148">A pointer to the second Unicode string to be compared.</span></span>

</dd> <dt>

<span data-ttu-id="72b83-149">*cchCount2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72b83-149">*cchCount2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72b83-150">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="72b83-150">Type: **int**</span></span>

<span data-ttu-id="72b83-151">Numero di caratteri nella stringa a cui punta il parametro *lpString2* .</span><span class="sxs-lookup"><span data-stu-id="72b83-151">The number of characters in the string pointed to by the *lpString2* parameter.</span></span> <span data-ttu-id="72b83-152">Il conteggio non include il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="72b83-152">The count does not include the terminating null character.</span></span> <span data-ttu-id="72b83-153">Se questo parametro è un valore negativo, si presuppone che la stringa sia con terminazione null e che la lunghezza venga calcolata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="72b83-153">If this parameter is a negative value, the string is assumed to be null-terminated and the length is calculated automatically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72b83-154">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72b83-154">Return value</span></span>

<span data-ttu-id="72b83-155">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="72b83-155">Type: **int**</span></span>

<span data-ttu-id="72b83-156">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="72b83-156">If the function fails, the return value is zero.</span></span> <span data-ttu-id="72b83-157">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="72b83-157">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="72b83-158">**GetLastError** può restituire uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="72b83-158">**GetLastError** may return one of the following error codes.</span></span>

-   <span data-ttu-id="72b83-159">flag di errore \_ non validi \_</span><span class="sxs-lookup"><span data-stu-id="72b83-159">ERROR\_INVALID\_FLAGS</span></span>
-   <span data-ttu-id="72b83-160">ERRORE \_ parametro non valido \_</span><span class="sxs-lookup"><span data-stu-id="72b83-160">ERROR\_INVALID\_PARAMETER</span></span>

<span data-ttu-id="72b83-161">Se la funzione ha esito positivo, il valore restituito è uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="72b83-161">If the function succeeds, the return value is one of the following values.</span></span> 

| <span data-ttu-id="72b83-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="72b83-162">Requirement</span></span> | <span data-ttu-id="72b83-163">Valore</span><span class="sxs-lookup"><span data-stu-id="72b83-163">Value</span></span> |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72b83-164">CSTR \_ minore \_ di</span><span class="sxs-lookup"><span data-stu-id="72b83-164">CSTR\_LESS\_THAN</span></span>    | <span data-ttu-id="72b83-165">La stringa a cui punta il parametro *lpString1* è minore del valore lessicale rispetto alla stringa a cui punta il parametro *lpString2* .</span><span class="sxs-lookup"><span data-stu-id="72b83-165">The string pointed to by the *lpString1* parameter is less in lexical value than the string pointed to by the *lpString2* parameter.</span></span> |
| <span data-ttu-id="72b83-166">CSTR \_ uguale a</span><span class="sxs-lookup"><span data-stu-id="72b83-166">CSTR\_EQUAL</span></span>         | <span data-ttu-id="72b83-167">La stringa a cui punta *lpString1* è uguale al valore lessicale alla stringa a cui punta *lpString2*.</span><span class="sxs-lookup"><span data-stu-id="72b83-167">The string pointed to by *lpString1* is equal in lexical value to the string pointed to by *lpString2*.</span></span>                              |
| <span data-ttu-id="72b83-168">CSTR \_ maggiore \_ di</span><span class="sxs-lookup"><span data-stu-id="72b83-168">CSTR\_GREATER\_THAN</span></span> | <span data-ttu-id="72b83-169">La stringa a cui punta *lpString1* è maggiore nel valore lessicale della stringa a cui punta *lpString2*</span><span class="sxs-lookup"><span data-stu-id="72b83-169">The string pointed to by *lpString1* is greater in lexical value than the string pointed to by *lpString2*</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="72b83-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="72b83-170">Remarks</span></span>

<span data-ttu-id="72b83-171">**Avviso di sicurezza:** L'uso errato di questa funzione può compromettere la sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="72b83-171">**Security Warning:** Using this function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="72b83-172">Le stringhe che non vengono confrontate correttamente possono produrre un input non valido.</span><span class="sxs-lookup"><span data-stu-id="72b83-172">Strings that are not compared correctly can produce invalid input.</span></span> <span data-ttu-id="72b83-173">Testare le stringhe per assicurarsi che siano valide prima di utilizzarle e fornire gestori di errori.</span><span class="sxs-lookup"><span data-stu-id="72b83-173">Test strings to make sure they are valid before using them and provide error handlers.</span></span> <span data-ttu-id="72b83-174">Per altre informazioni, vedere [considerazioni sulla sicurezza: funzionalità internazionali](../intl/security-considerations--international-features.md)</span><span class="sxs-lookup"><span data-stu-id="72b83-174">For more information, see [Security Considerations: International Features](../intl/security-considerations--international-features.md)</span></span>

<span data-ttu-id="72b83-175">Il metodo preferito consiste nell'usare [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) insieme a Microsoft Layer for Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="72b83-175">The preferred method is to use [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="72b83-176">**CompareStringWrapW** deve essere chiamato direttamente da Shlwapi.dll, usando il numero ordinale 45.</span><span class="sxs-lookup"><span data-stu-id="72b83-176">**CompareStringWrapW** must be called directly from Shlwapi.dll, using ordinal 45.</span></span>

## <a name="requirements"></a><span data-ttu-id="72b83-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72b83-177">Requirements</span></span>



| <span data-ttu-id="72b83-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="72b83-178">Requirement</span></span> | <span data-ttu-id="72b83-179">Valore</span><span class="sxs-lookup"><span data-stu-id="72b83-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72b83-180">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72b83-180">Minimum supported client</span></span><br/> | <span data-ttu-id="72b83-181">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="72b83-181">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72b83-182">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72b83-182">Minimum supported server</span></span><br/> | <span data-ttu-id="72b83-183">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="72b83-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="72b83-184">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72b83-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="72b83-185"><dt>Nessuno</dt></span><span class="sxs-lookup"><span data-stu-id="72b83-185"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="72b83-186">DLL</span><span class="sxs-lookup"><span data-stu-id="72b83-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72b83-187"><dt>Shlwapi.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="72b83-187"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72b83-188">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72b83-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b83-189">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="72b83-189">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 

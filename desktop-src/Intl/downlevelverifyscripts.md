---
description: Confronta due elenchi enumerati di script.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: Funzione DownlevelVerifyScripts (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelVerifyScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 62e029576d53109e3c57faf4ec913472f8aea65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317160"
---
# <a name="downlevelverifyscripts-function"></a><span data-ttu-id="55b42-103">DownlevelVerifyScripts (funzione)</span><span class="sxs-lookup"><span data-stu-id="55b42-103">DownlevelVerifyScripts function</span></span>

<span data-ttu-id="55b42-104">Confronta due elenchi enumerati di script.</span><span class="sxs-lookup"><span data-stu-id="55b42-104">Compares two enumerated lists of scripts.</span></span>

> [!Note]  
> <span data-ttu-id="55b42-105">Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="55b42-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="55b42-106">Il relativo utilizzo richiede il pacchetto di download.</span><span class="sxs-lookup"><span data-stu-id="55b42-106">Its use requires the download package.</span></span> <span data-ttu-id="55b42-107">Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span><span class="sxs-lookup"><span data-stu-id="55b42-107">Applications that only run on Windows Vista and later should call [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="55b42-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55b42-108">Syntax</span></span>


```C++
BOOL DownlevelVerifyScripts(
  _In_ DWORD   dwFlags,
  _In_ LPCWSTR lpLocaleScripts,
  _In_ int     cchLocaleScripts,
  _In_ LPCWSTR lpTestScripts,
  _In_ int     cchTestScripts
);
```



## <a name="parameters"></a><span data-ttu-id="55b42-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="55b42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55b42-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55b42-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b42-111">Flag che specificano le opzioni di verifica dello script.</span><span class="sxs-lookup"><span data-stu-id="55b42-111">Flags specifying script verification options.</span></span>



| <span data-ttu-id="55b42-112">Valore</span><span class="sxs-lookup"><span data-stu-id="55b42-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="55b42-113">Significato</span><span class="sxs-lookup"><span data-stu-id="55b42-113">Meaning</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <span data-ttu-id="55b42-114"><dt>**VS \_ consente il \_ latino**</dt></span><span class="sxs-lookup"><span data-stu-id="55b42-114"><dt>**VS\_ALLOW\_LATIN**</dt></span></span> </dl> | <span data-ttu-id="55b42-115">Consenti "Latn" (alfabeto latino) nell'elenco dei test, anche se non è presente nell'elenco delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="55b42-115">Allow "Latn" (Latin script) in the test list, even if it is not in the locale list.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="55b42-116">*lpLocaleScripts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55b42-116">*lpLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b42-117">Puntatore all'elenco delle impostazioni locali, l'elenco enumerato di script per le impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="55b42-117">Pointer to the locale list, the enumerated list of scripts for a given locale.</span></span> <span data-ttu-id="55b42-118">Questo elenco viene popolato in genere chiamando [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).</span><span class="sxs-lookup"><span data-stu-id="55b42-118">This list is typically populated by calling [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="55b42-119">*cchLocaleScripts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55b42-119">*cchLocaleScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b42-120">Dimensione, in caratteri, della stringa indicata da *lpLocaleScripts*.</span><span class="sxs-lookup"><span data-stu-id="55b42-120">Size, in characters, of the string indicated by *lpLocaleScripts*.</span></span> <span data-ttu-id="55b42-121">L'applicazione imposta questo parametro su-1 se la stringa è con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="55b42-121">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="55b42-122">Se questo parametro è impostato su 0, la funzione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="55b42-122">If this parameter is set to 0, the function fails.</span></span>

</dd> <dt>

<span data-ttu-id="55b42-123">*lpTestScripts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55b42-123">*lpTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b42-124">Puntatore all'elenco dei test, un secondo elenco enumerato di script.</span><span class="sxs-lookup"><span data-stu-id="55b42-124">Pointer to the test list, a second enumerated list of scripts.</span></span> <span data-ttu-id="55b42-125">Questo elenco viene popolato in genere chiamando [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).</span><span class="sxs-lookup"><span data-stu-id="55b42-125">This list is typically populated by calling [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).</span></span>

</dd> <dt>

<span data-ttu-id="55b42-126">*cchTestScripts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55b42-126">*cchTestScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b42-127">Dimensione, in caratteri, della stringa indicata da *lpTestScripts*.</span><span class="sxs-lookup"><span data-stu-id="55b42-127">Size, in characters, of the string indicated by *lpTestScripts*.</span></span> <span data-ttu-id="55b42-128">L'applicazione imposta questo parametro su-1 se la stringa è con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="55b42-128">The application sets this parameter to -1 if the string is null-terminated.</span></span> <span data-ttu-id="55b42-129">Se questo parametro è impostato su 0, la funzione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="55b42-129">If this parameter is set to 0, the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55b42-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55b42-130">Return value</span></span>

<span data-ttu-id="55b42-131">Restituisce **true** se l'elenco di test non è vuoto e tutti gli elementi dell'elenco sono inclusi anche nell'elenco delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="55b42-131">Returns **TRUE** if the test list is non-empty and all items in the list are also included in the locale list.</span></span> <span data-ttu-id="55b42-132">In caso contrario, la funzione restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="55b42-132">Otherwise, the function returns **FALSE**.</span></span>

<span data-ttu-id="55b42-133">Un valore restituito di **false** può indicare che l'elenco di test contiene un elemento che non è presente nell'elenco delle impostazioni locali oppure può indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="55b42-133">A return value of **FALSE** can indicate that the test list contains an item that is not in the locale list, or it can indicate an error.</span></span> <span data-ttu-id="55b42-134">Per distinguere tra questi due casi, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="55b42-134">To distinguish between these two cases, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> <span data-ttu-id="55b42-135">Se **DownlevelVerifyScripts** ha determinato che è presente un elemento nell'elenco di test che non è presente nell'elenco delle impostazioni locali, **GetLastError** restituisce Error \_ Success.</span><span class="sxs-lookup"><span data-stu-id="55b42-135">If **DownlevelVerifyScripts** has successfully determined that there is an item in the test list that is not in the locale list, **GetLastError** returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="55b42-136">In caso contrario, **GetLastError** può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="55b42-136">Otherwise, **GetLastError** can return one of the following error codes:</span></span>

-   <span data-ttu-id="55b42-137">flag di errore \_ non validi \_ .</span><span class="sxs-lookup"><span data-stu-id="55b42-137">ERROR\_INVALID\_FLAGS.</span></span> <span data-ttu-id="55b42-138">I valori specificati per i flag non sono validi.</span><span class="sxs-lookup"><span data-stu-id="55b42-138">The values supplied for flags were not valid.</span></span>
-   <span data-ttu-id="55b42-139">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="55b42-139">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="55b42-140">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="55b42-140">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="55b42-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="55b42-141">Remarks</span></span>

<span data-ttu-id="55b42-142">Questa funzione Confronta le stringhe, ad esempio "Latn; Cyrl; ", costituito da una serie di nomi di script di 4 caratteri, con ogni nome di script seguito da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="55b42-142">This function compares strings, such as "Latn;Cyrl;", that consist of a series of 4-character script names, with each script name followed by a semicolon.</span></span> <span data-ttu-id="55b42-143">Ha anche un caso speciale per tenere conto del fatto che lo script latino viene spesso usato in linguaggi e impostazioni locali per cui non è nativo.</span><span class="sxs-lookup"><span data-stu-id="55b42-143">It also has a special case to account for the fact that the Latin script is often used in languages and locales for which it is not native.</span></span>

<span data-ttu-id="55b42-144">Questa funzione è utile come parte di una strategia per attenuare i problemi di sicurezza correlati ai [nomi di dominio internazionali (IDN)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="55b42-144">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="55b42-145">Di seguito sono riportati esempi della restituzione di questa funzione e di una chiamata successiva a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) in diversi scenari.</span><span class="sxs-lookup"><span data-stu-id="55b42-145">The following are examples of the return of this function and a subsequent call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) in various scenarios.</span></span> <span data-ttu-id="55b42-146">Gli ultimi due esempi illustrano, rispettivamente, un caso in cui l'elenco di test non dispone di un punto e virgola di terminazione (stringa in formato non corretto) e di un caso in cui l'elenco di test è vuoto.</span><span class="sxs-lookup"><span data-stu-id="55b42-146">The last two examples illustrate, respectively, a case in which the test list lacks a terminating semicolon (malformed string) and a case in which the test list is empty.</span></span>



| <span data-ttu-id="55b42-147">Stringa "impostazioni locali"</span><span class="sxs-lookup"><span data-stu-id="55b42-147">"Locale" string</span></span> | <span data-ttu-id="55b42-148">Stringa "test"</span><span class="sxs-lookup"><span data-stu-id="55b42-148">"Test" string</span></span> | <span data-ttu-id="55b42-149">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="55b42-149">*dwFlags*</span></span>        | <span data-ttu-id="55b42-150">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55b42-150">Return value</span></span> | <span data-ttu-id="55b42-151">Restituito GetLastError</span><span class="sxs-lookup"><span data-stu-id="55b42-151">GetLastError return</span></span>       |
|-----------------|---------------|------------------|--------------|---------------------------|
| <span data-ttu-id="55b42-152">Hani Hira Kana</span><span class="sxs-lookup"><span data-stu-id="55b42-152">Hani;Hira;Kana;</span></span> | <span data-ttu-id="55b42-153">Hani</span><span class="sxs-lookup"><span data-stu-id="55b42-153">Hani;</span></span>         | <span data-ttu-id="55b42-154">N/D</span><span class="sxs-lookup"><span data-stu-id="55b42-154">N/A</span></span>              | <span data-ttu-id="55b42-155">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="55b42-155">**TRUE**</span></span>     | <span data-ttu-id="55b42-156">N/D</span><span class="sxs-lookup"><span data-stu-id="55b42-156">N/A</span></span>                       |
| <span data-ttu-id="55b42-157">Hani Hira Kana</span><span class="sxs-lookup"><span data-stu-id="55b42-157">Hani;Hira;Kana;</span></span> | <span data-ttu-id="55b42-158">Hani Latn</span><span class="sxs-lookup"><span data-stu-id="55b42-158">Hani;Latn;</span></span>    | <span data-ttu-id="55b42-159">0</span><span class="sxs-lookup"><span data-stu-id="55b42-159">0</span></span>                | <span data-ttu-id="55b42-160">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="55b42-160">**FALSE**</span></span>    | <span data-ttu-id="55b42-161">ERRORE \_ riuscito</span><span class="sxs-lookup"><span data-stu-id="55b42-161">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="55b42-162">Hani Hira Kana</span><span class="sxs-lookup"><span data-stu-id="55b42-162">Hani;Hira;Kana;</span></span> | <span data-ttu-id="55b42-163">Hani Latn</span><span class="sxs-lookup"><span data-stu-id="55b42-163">Hani;Latn;</span></span>    | <span data-ttu-id="55b42-164">VS \_ consente il \_ latino</span><span class="sxs-lookup"><span data-stu-id="55b42-164">VS\_ALLOW\_LATIN</span></span> | <span data-ttu-id="55b42-165">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="55b42-165">**TRUE**</span></span>     | <span data-ttu-id="55b42-166">N/D</span><span class="sxs-lookup"><span data-stu-id="55b42-166">N/A</span></span>                       |
| <span data-ttu-id="55b42-167">Hani Hira Kana</span><span class="sxs-lookup"><span data-stu-id="55b42-167">Hani;Hira;Kana;</span></span> | <span data-ttu-id="55b42-168">Cyrl</span><span class="sxs-lookup"><span data-stu-id="55b42-168">Cyrl;</span></span>         | <span data-ttu-id="55b42-169">N/D</span><span class="sxs-lookup"><span data-stu-id="55b42-169">N/A</span></span>              | <span data-ttu-id="55b42-170">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="55b42-170">**FALSE**</span></span>    | <span data-ttu-id="55b42-171">ERRORE \_ riuscito</span><span class="sxs-lookup"><span data-stu-id="55b42-171">ERROR\_SUCCESS</span></span>            |
| <span data-ttu-id="55b42-172">Hani Hira Kana</span><span class="sxs-lookup"><span data-stu-id="55b42-172">Hani;Hira;Kana;</span></span> | <span data-ttu-id="55b42-173">Cyrl</span><span class="sxs-lookup"><span data-stu-id="55b42-173">Cyrl;</span></span>         | <span data-ttu-id="55b42-174">N/D</span><span class="sxs-lookup"><span data-stu-id="55b42-174">N/A</span></span>              | <span data-ttu-id="55b42-175">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="55b42-175">**FALSE**</span></span>    | <span data-ttu-id="55b42-176">ERRORE \_ parametro non valido \_</span><span class="sxs-lookup"><span data-stu-id="55b42-176">ERROR\_INVALID\_PARAMETER</span></span> |
| <span data-ttu-id="55b42-177">Hani Hira Kana</span><span class="sxs-lookup"><span data-stu-id="55b42-177">Hani;Hira;Kana;</span></span> |               | <span data-ttu-id="55b42-178">N/D</span><span class="sxs-lookup"><span data-stu-id="55b42-178">N/A</span></span>              | <span data-ttu-id="55b42-179">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="55b42-179">**FALSE**</span></span>    | <span data-ttu-id="55b42-180">ERRORE \_ riuscito</span><span class="sxs-lookup"><span data-stu-id="55b42-180">ERROR\_SUCCESS</span></span>            |



 

<span data-ttu-id="55b42-181">Il file di intestazione e la DLL necessari fanno parte del download di ["API di mitigazione del nome di dominio Microsoft (IDN)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponibile nell' [area download MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="55b42-181">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="55b42-182">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55b42-182">Requirements</span></span>



| <span data-ttu-id="55b42-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="55b42-183">Requirement</span></span> | <span data-ttu-id="55b42-184">Valore</span><span class="sxs-lookup"><span data-stu-id="55b42-184">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55b42-185">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55b42-185">Minimum supported client</span></span><br/> | <span data-ttu-id="55b42-186">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="55b42-186">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                  |
| <span data-ttu-id="55b42-187">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55b42-187">Minimum supported server</span></span><br/> | <span data-ttu-id="55b42-188">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="55b42-188">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                         |
| <span data-ttu-id="55b42-189">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="55b42-189">Redistributable</span></span><br/>          | <span data-ttu-id="55b42-190">API di mitigazione Microsoft per il nome di dominio internazionale (IDN) in Windows XP con SP2, Windows Server 2003 con SP1, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55b42-190">Microsoft Internationalized Domain Name (IDN) Mitigation APIs onWindows XP with SP2,Windows Server 2003 with SP1, orWindows Vista</span></span><br/> |
| <span data-ttu-id="55b42-191">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55b42-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="55b42-192"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55b42-192"><dt>Idndl.h</dt></span></span> </dl>                                                           |
| <span data-ttu-id="55b42-193">DLL</span><span class="sxs-lookup"><span data-stu-id="55b42-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55b42-194"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55b42-194"><dt>Idndl.dll</dt></span></span> </dl>                                                         |



## <a name="see-also"></a><span data-ttu-id="55b42-195">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55b42-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b42-196">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="55b42-196">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="55b42-197">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="55b42-197">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="55b42-198">Gestione dei nomi di dominio internazionalizzati (IDN)</span><span class="sxs-lookup"><span data-stu-id="55b42-198">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="55b42-199">**DownlevelGetLocaleScripts**</span><span class="sxs-lookup"><span data-stu-id="55b42-199">**DownlevelGetLocaleScripts**</span></span>](downlevelgetlocalescripts.md)
</dt> <dt>

[<span data-ttu-id="55b42-200">**DownlevelGetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="55b42-200">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="55b42-201">**VerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="55b42-201">**VerifyScripts**</span></span>](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 

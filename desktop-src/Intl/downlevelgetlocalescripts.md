---
description: Fornisce un elenco di script per le impostazioni locali specificate.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: Funzione DownlevelGetLocaleScripts (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetLocaleScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: f636ab426cd4d50878df93e3e30d69de54d60ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233310"
---
# <a name="downlevelgetlocalescripts-function"></a><span data-ttu-id="7d685-103">DownlevelGetLocaleScripts (funzione)</span><span class="sxs-lookup"><span data-stu-id="7d685-103">DownlevelGetLocaleScripts function</span></span>

<span data-ttu-id="7d685-104">Fornisce un elenco di script per le impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="7d685-104">Provides a list of scripts for the specified locale.</span></span>

> [!Note]  
> <span data-ttu-id="7d685-105">Questa funzione viene utilizzata solo dalle applicazioni eseguite in sistemi operativi precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7d685-105">This function is used only by applications that run on pre-Windows Vista operating systems.</span></span> <span data-ttu-id="7d685-106">Il relativo utilizzo richiede il pacchetto di download.</span><span class="sxs-lookup"><span data-stu-id="7d685-106">Its use requires the download package.</span></span> <span data-ttu-id="7d685-107">Le applicazioni che vengono eseguite solo in Windows Vista e versioni successive devono chiamare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) con *LCType* impostato su [locale \_ SSCRIPTS](locale-sscripts.md).</span><span class="sxs-lookup"><span data-stu-id="7d685-107">Applications that only run on Windows Vista and later should call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) with *LCType* set to [LOCALE\_SSCRIPTS](locale-sscripts.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7d685-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d685-108">Syntax</span></span>


```C++
int DownlevelGetLocaleScripts(
  _In_  LPCWSTR lpLocaleName,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a><span data-ttu-id="7d685-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d685-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d685-110">*lpLocaleName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d685-110">*lpLocaleName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d685-111">Puntatore a un [nome delle impostazioni locali](locale-names.md)con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="7d685-111">Pointer to a null-terminated [locale name](locale-names.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d685-112">*lpScripts* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7d685-112">*lpScripts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d685-113">Puntatore a un buffer in cui questa funzione recupera una stringa a terminazione null che rappresenta un elenco di script, usando la notazione di 4 caratteri usata nello standard [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span><span class="sxs-lookup"><span data-stu-id="7d685-113">Pointer to a buffer in which this function retrieves a null-terminated string representing a list of scripts, using the 4-character notation used in [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html).</span></span> <span data-ttu-id="7d685-114">Ogni nome di script è costituito da quattro caratteri latini e i nomi vengono recuperati in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="7d685-114">Each script name consists of four Latin characters, and the names are retrieved in alphabetical order.</span></span> <span data-ttu-id="7d685-115">Ognuno di essi, incluso l'ultimo, è seguito da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="7d685-115">Each of them, including the last, is followed by a semicolon.</span></span>

<span data-ttu-id="7d685-116">In alternativa, questo parametro può contenere **null** se *cchScripts* è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="7d685-116">Alternatively, this parameter can contain **NULL** if *cchScripts* is set to 0.</span></span> <span data-ttu-id="7d685-117">In questo caso, la funzione restituisce la dimensione richiesta per il buffer di script.</span><span class="sxs-lookup"><span data-stu-id="7d685-117">In this case, the function returns the required size for the script buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7d685-118">*cchScripts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d685-118">*cchScripts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d685-119">Dimensione, in caratteri, del buffer di script indicato da *lpScripts*.</span><span class="sxs-lookup"><span data-stu-id="7d685-119">Size, in characters, for the script buffer indicated by *lpScripts*.</span></span>

<span data-ttu-id="7d685-120">In alternativa, l'applicazione può impostare questo parametro su 0.</span><span class="sxs-lookup"><span data-stu-id="7d685-120">Alternatively, the application can set this parameter to 0.</span></span> <span data-ttu-id="7d685-121">In questo caso, la funzione recupera il **valore null** in *lpScripts* e restituisce la dimensione richiesta per il buffer di script.</span><span class="sxs-lookup"><span data-stu-id="7d685-121">In this case, the function retrieves **NULL** in *lpScripts* and returns the required size for the script buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d685-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d685-122">Return value</span></span>

<span data-ttu-id="7d685-123">Restituisce il numero di caratteri recuperati nel buffer di script, incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="7d685-123">Returns the number of characters retrieved in the script buffer, including the terminating null character.</span></span> <span data-ttu-id="7d685-124">Se la funzione ha esito positivo e il valore di *cchScripts* è 0, il valore restituito è la dimensione richiesta, in caratteri che include un carattere null di terminazione, per il buffer di script.</span><span class="sxs-lookup"><span data-stu-id="7d685-124">If the function succeeds and the value of *cchScripts* is 0, the return value is the required size, in characters including a terminating null character, for the script buffer.</span></span>

<span data-ttu-id="7d685-125">Questa funzione restituisce 0 in caso di esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7d685-125">This function returns 0 if it does not succeed.</span></span> <span data-ttu-id="7d685-126">Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="7d685-126">To get extended error information, the application can call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), which can return one of the following error codes:</span></span>

-   <span data-ttu-id="7d685-127">ERRORE \_ BADDB.</span><span class="sxs-lookup"><span data-stu-id="7d685-127">ERROR\_BADDB.</span></span> <span data-ttu-id="7d685-128">La funzione non è stata in grado di accedere ai dati.</span><span class="sxs-lookup"><span data-stu-id="7d685-128">The function could not access the data.</span></span> <span data-ttu-id="7d685-129">Questa situazione non dovrebbe in genere verificarsi e in genere indica un'installazione non valida, un problema del disco o un tipo simile.</span><span class="sxs-lookup"><span data-stu-id="7d685-129">This situation should not normally occur, and typically indicates a bad installation, a disk problem, or the like.</span></span>
-   <span data-ttu-id="7d685-130">ERRORE \_ \_ nel buffer insufficiente.</span><span class="sxs-lookup"><span data-stu-id="7d685-130">ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="7d685-131">Una dimensione del buffer specificata non è sufficientemente grande oppure è stata impostata erroneamente su **null**.</span><span class="sxs-lookup"><span data-stu-id="7d685-131">A supplied buffer size was not large enough, or it was incorrectly set to **NULL**.</span></span>
-   <span data-ttu-id="7d685-132">ERRORE \_ parametro non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="7d685-132">ERROR\_INVALID\_PARAMETER.</span></span> <span data-ttu-id="7d685-133">Uno dei valori di parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="7d685-133">Any of the parameter values was invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d685-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d685-134">Remarks</span></span>

<span data-ttu-id="7d685-135">Questa funzione è utile come parte di una strategia per attenuare i problemi di sicurezza correlati ai [nomi di dominio internazionali (IDN)](handling-internationalized-domain-names--idns.md).</span><span class="sxs-lookup"><span data-stu-id="7d685-135">This function is useful as part of a strategy to mitigate security issues related to [internationalized domain names (IDNs)](handling-internationalized-domain-names--idns.md).</span></span>

<span data-ttu-id="7d685-136">Di seguito sono riportati alcuni esempi di input e output per questa funzione, presumendo una dimensione del buffer sufficiente:</span><span class="sxs-lookup"><span data-stu-id="7d685-136">Here are some examples of inputs and outputs for this function, assuming a sufficient buffer size:</span></span>



| <span data-ttu-id="7d685-137">Locale</span><span class="sxs-lookup"><span data-stu-id="7d685-137">Locale</span></span>                  | <span data-ttu-id="7d685-138">*lpLocaleName*</span><span class="sxs-lookup"><span data-stu-id="7d685-138">*lpLocaleName*</span></span> | <span data-ttu-id="7d685-139">*lpScripts*</span><span class="sxs-lookup"><span data-stu-id="7d685-139">*lpScripts*</span></span>     |
|-------------------------|----------------|-----------------|
| <span data-ttu-id="7d685-140">Inglese (Stati Uniti)</span><span class="sxs-lookup"><span data-stu-id="7d685-140">English (United States)</span></span> | <span data-ttu-id="7d685-141">it-IT</span><span class="sxs-lookup"><span data-stu-id="7d685-141">en-US</span></span>          | <span data-ttu-id="7d685-142">Latn</span><span class="sxs-lookup"><span data-stu-id="7d685-142">Latn;</span></span>           |
| <span data-ttu-id="7d685-143">Hindi (India)</span><span class="sxs-lookup"><span data-stu-id="7d685-143">Hindi (India)</span></span>           | <span data-ttu-id="7d685-144">hi-IN</span><span class="sxs-lookup"><span data-stu-id="7d685-144">hi-IN</span></span>          | <span data-ttu-id="7d685-145">Deva</span><span class="sxs-lookup"><span data-stu-id="7d685-145">Deva;</span></span>           |
| <span data-ttu-id="7d685-146">Giapponese (Giappone)</span><span class="sxs-lookup"><span data-stu-id="7d685-146">Japanese (Japan)</span></span>        | <span data-ttu-id="7d685-147">ja-JP</span><span class="sxs-lookup"><span data-stu-id="7d685-147">ja-JP</span></span>          | <span data-ttu-id="7d685-148">Hani Hira Kana</span><span class="sxs-lookup"><span data-stu-id="7d685-148">Hani;Hira;Kana;</span></span> |



 

<span data-ttu-id="7d685-149">L'elenco non contiene lo script latino, a meno che non si tratti di una parte essenziale del sistema di scrittura usato per le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="7d685-149">The list does not contain the Latin script unless it is an essential part of the writing system used for a locale.</span></span> <span data-ttu-id="7d685-150">Tuttavia, i caratteri latini vengono spesso usati nel contesto delle impostazioni locali per cui non sono nativi, come per un nome aziendale esterno.</span><span class="sxs-lookup"><span data-stu-id="7d685-150">However, Latin characters are often used in the context of locales for which they are not native, as for a foreign business name.</span></span> <span data-ttu-id="7d685-151">Nell'esempio precedente per hindi in India, l'unico script recuperato è "Deva" (per devangato), anche se i caratteri latini possono anche essere visualizzati in testo Hindi.</span><span class="sxs-lookup"><span data-stu-id="7d685-151">In the example above for Hindi in India, the only script retrieved is "Deva" (for Devanagari), although Latin characters can also appear in Hindi text.</span></span> <span data-ttu-id="7d685-152">La funzione [**DownlevelVerifyScripts**](downlevelverifyscripts.md) ha un flag speciale per risolvere il caso.</span><span class="sxs-lookup"><span data-stu-id="7d685-152">The [**DownlevelVerifyScripts**](downlevelverifyscripts.md) function has a special flag to address that case.</span></span>

<span data-ttu-id="7d685-153">Il file di intestazione e la DLL necessari fanno parte del download di ["API di mitigazione del nome di dominio Microsoft (IDN)"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponibile nell' [area download MSDN](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="7d685-153">The required header file and DLL are part of the ["Microsoft Internationalized Domain Name (IDN) Mitigation APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) download, available at the [MSDN Download Center](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d685-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d685-154">Requirements</span></span>



| <span data-ttu-id="7d685-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d685-155">Requirement</span></span> | <span data-ttu-id="7d685-156">Valore</span><span class="sxs-lookup"><span data-stu-id="7d685-156">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d685-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d685-157">Minimum supported client</span></span><br/> | <span data-ttu-id="7d685-158">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7d685-158">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                 |
| <span data-ttu-id="7d685-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d685-159">Minimum supported server</span></span><br/> | <span data-ttu-id="7d685-160">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d685-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                        |
| <span data-ttu-id="7d685-161">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7d685-161">Redistributable</span></span><br/>          | <span data-ttu-id="7d685-162">API di mitigazione Microsoft per il nome di dominio internazionale (IDN) in Windows XP (SP2 o versioni successive), Windows Server 2003 (SP1 o versione successiva) o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d685-162">Microsoft Internationalized Domain Name (IDN) Mitigation APIs on Windows XP (SP2 or later), Windows Server 2003 (SP1 or later), or Windows Vista</span></span><br/> |
| <span data-ttu-id="7d685-163">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d685-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d685-164"><dt>Idndl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d685-164"><dt>Idndl.h</dt></span></span> </dl>                                                                          |
| <span data-ttu-id="7d685-165">DLL</span><span class="sxs-lookup"><span data-stu-id="7d685-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d685-166"><dt>Idndl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d685-166"><dt>Idndl.dll</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="7d685-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d685-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d685-168">Supporto per lingua nazionale</span><span class="sxs-lookup"><span data-stu-id="7d685-168">National Language Support</span></span>](national-language-support.md)
</dt> <dt>

[<span data-ttu-id="7d685-169">Funzioni di supporto del linguaggio nazionale</span><span class="sxs-lookup"><span data-stu-id="7d685-169">National Language Support Functions</span></span>](national-language-support-functions.md)
</dt> <dt>

[<span data-ttu-id="7d685-170">Gestione dei nomi di dominio internazionalizzati (IDN)</span><span class="sxs-lookup"><span data-stu-id="7d685-170">Handling Internationalized Domain Names (IDNs)</span></span>](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[<span data-ttu-id="7d685-171">**DownlevelGetStringScripts**</span><span class="sxs-lookup"><span data-stu-id="7d685-171">**DownlevelGetStringScripts**</span></span>](downlevelgetstringscripts.md)
</dt> <dt>

[<span data-ttu-id="7d685-172">**DownlevelVerifyScripts**</span><span class="sxs-lookup"><span data-stu-id="7d685-172">**DownlevelVerifyScripts**</span></span>](downlevelverifyscripts.md)
</dt> <dt>

[<span data-ttu-id="7d685-173">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="7d685-173">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 

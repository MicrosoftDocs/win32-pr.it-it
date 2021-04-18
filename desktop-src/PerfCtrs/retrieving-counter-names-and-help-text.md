---
description: I dati sulle prestazioni contengono valori di indice utilizzati per individuare i nomi e il testo della Guida per ogni oggetto e contatore registrato.
ms.assetid: 9ddd1672-61cf-41c2-bec0-0d2b775bf970
title: Recupero di nomi di contatori e testo della Guida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b49f852e6af22dc2ec31d341ee6176913f98e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312087"
---
# <a name="retrieving-counter-names-and-help-text"></a><span data-ttu-id="a442c-103">Recupero di nomi di contatori e testo della Guida</span><span class="sxs-lookup"><span data-stu-id="a442c-103">Retrieving Counter Names and Help Text</span></span>

<span data-ttu-id="a442c-104">I dati sulle prestazioni contengono valori di indice utilizzati per individuare i nomi e il testo della Guida per ogni oggetto e contatore registrato.</span><span class="sxs-lookup"><span data-stu-id="a442c-104">The performance data contains index values that you use to locate the names and help text for each registered object and counter.</span></span> <span data-ttu-id="a442c-105">I membri **ObjectNameTitleIndex** e **ObjectHelpTitleIndex** della struttura [**del \_ \_ tipo di oggetto Perf**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) contengono rispettivamente i valori di indice per il nome dell'oggetto e il testo della guida e i membri **CounterNameTitleIndex** e **CounterHelpTitleIndex** della struttura di [**\_ \_ definizione dei contatori delle prestazioni**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) contengono rispettivamente i valori di indice e il nome del contatore e il testo della guida.</span><span class="sxs-lookup"><span data-stu-id="a442c-105">The **ObjectNameTitleIndex** and **ObjectHelpTitleIndex** members of the [**PERF\_OBJECT\_TYPE**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) structure contain the index values to the object name and help text, respectively, and the **CounterNameTitleIndex** and **CounterHelpTitleIndex** members of the [**PERF\_COUNTER\_DEFINITION**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) structure contain the index values to the counter name and help text, respectively.</span></span>

<span data-ttu-id="a442c-106">Per recuperare i nomi o il testo della guida, chiamare la funzione [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) .</span><span class="sxs-lookup"><span data-stu-id="a442c-106">To retrieve the names or help text, call the [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function.</span></span> <span data-ttu-id="a442c-107">Impostare il parametro *HKEY* su una delle chiavi predefinite seguenti.</span><span class="sxs-lookup"><span data-stu-id="a442c-107">Set the *hKey* parameter to one of the following predefined keys.</span></span> <span data-ttu-id="a442c-108">In genere, si utilizzerà la chiave **\_ \_ NLSTEXT delle prestazioni di HKEY** , pertanto non è necessario determinare l'identificatore di lingua dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a442c-108">Typically, you would use the **HKEY\_PERFORMANCE\_NLSTEXT** key, so you do not have to determine the user's language identifier.</span></span>



| <span data-ttu-id="a442c-109">Chiave</span><span class="sxs-lookup"><span data-stu-id="a442c-109">Key</span></span>                            | <span data-ttu-id="a442c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a442c-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a442c-111">**\_dati sulle prestazioni di HKEY \_**</span><span class="sxs-lookup"><span data-stu-id="a442c-111">**HKEY\_PERFORMANCE\_DATA**</span></span>    | <span data-ttu-id="a442c-112">Eseguire una query sulle stringhe in base al valore dell'identificatore di lingua specificato nel parametro *lpValueName* .</span><span class="sxs-lookup"><span data-stu-id="a442c-112">Query strings based on the language identifier value that you specify in the *lpValueName* parameter.</span></span> <span data-ttu-id="a442c-113">Impostare il parametro *lpValueName* su "Counter &lt; LangID &gt; " o "Help &lt; LangID &gt; " per recuperare rispettivamente i nomi o il testo della guida, dove " &lt; LangID &gt; " è l'identificatore della lingua di sistema formattato come **numero esadecimale a 3 cifre** con riempimento zero.</span><span class="sxs-lookup"><span data-stu-id="a442c-113">Set *lpValueName* parameter to either "Counter &lt;langid&gt;" or "Help &lt;langid&gt;" to retrieve the names or help text, respectively, where "&lt;langid&gt;" is the system language identifier formatted as **zero-padded 3-digit hex number**.</span></span> <span data-ttu-id="a442c-114">L'identificatore di lingua è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a442c-114">The language identifier is optional.</span></span> <span data-ttu-id="a442c-115">Se non si specifica un identificatore di lingua, la funzione restituisce le stringhe in lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="a442c-115">If you do not specify a language identifier, the function returns English strings.</span></span> <span data-ttu-id="a442c-116">Controllare la `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Perflib` chiave del registro di sistema per l'elenco delle lingue disponibili nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a442c-116">Check the `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Perflib` registry key for the list of languages available on your system.</span></span><br/><span data-ttu-id="a442c-117">Per recuperare il testo nella maggior parte dei linguaggi, specificare solo l'identificatore della lingua primaria.</span><span class="sxs-lookup"><span data-stu-id="a442c-117">To retrieve text in most languages, specify the primary language identifier only.</span></span> <span data-ttu-id="a442c-118">Per recuperare le stringhe in lingua inglese, ad esempio, specificare l'identificatore della lingua come 009, non 1033 per l'inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="a442c-118">For example, to retrieve English strings, specify the language identifier as 009, not 1033 for English-US.</span></span><br/><span data-ttu-id="a442c-119">Per recuperare il testo in cinese e portoghese, specificare sia gli identificatori primari che quelli del linguaggio di sottolinguaggio.</span><span class="sxs-lookup"><span data-stu-id="a442c-119">To retrieve Chinese and Portuguese text, specify both the primary and sublanguage identifiers.</span></span><br/><span data-ttu-id="a442c-120">**Windows Server 2003 e Windows XP:** Specificare solo l'identificatore della lingua principale per il portoghese.</span><span class="sxs-lookup"><span data-stu-id="a442c-120">**Windows Server 2003 and Windows XP:** Specify only the primary language identifier for Portuguese.</span></span><br/><span data-ttu-id="a442c-121">**Windows 10**: il testo "Help &lt; LangID &gt; " con l'identificatore della lingua personalizzata restituisce sempre le stringhe in inglese, anche se il valore localizzato può comunque essere recuperato dal registro di sistema utilizzando la chiave sopra indicata.</span><span class="sxs-lookup"><span data-stu-id="a442c-121">**Windows 10**: "Help &lt;langid&gt;" text with custom language identifier always returns strings in English, although localized value can still be retrieved from the registry using the aforementioned key.</span></span><br/><br/> |
| <span data-ttu-id="a442c-122">**\_NLSTEXT prestazioni \_ HKEY**</span><span class="sxs-lookup"><span data-stu-id="a442c-122">**HKEY\_PERFORMANCE\_NLSTEXT**</span></span> | <span data-ttu-id="a442c-123">Esegue una query sulle stringhe basate sulla lingua predefinita dell'interfaccia utente dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="a442c-123">Query strings based on the default UI language of the current user.</span></span> <span data-ttu-id="a442c-124">Impostare il parametro *lpValueName* su "Counter" o "Help" per recuperare rispettivamente i nomi o il testo della guida.</span><span class="sxs-lookup"><span data-stu-id="a442c-124">Set the *lpValueName* parameter to either "Counter" or "Help" to retrieve the names or help text, respectively.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a442c-125">**\_testo prestazioni \_ HKEY**</span><span class="sxs-lookup"><span data-stu-id="a442c-125">**HKEY\_PERFORMANCE\_TEXT**</span></span>    | <span data-ttu-id="a442c-126">Eseguire query sulle stringhe in lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="a442c-126">Query English strings.</span></span> <span data-ttu-id="a442c-127">Impostare il parametro *lpValueName* su "Counter" o "Help" per recuperare rispettivamente i nomi o il testo della guida.</span><span class="sxs-lookup"><span data-stu-id="a442c-127">Set the *lpValueName* parameter to either "Counter" or "Help" to retrieve the names or help text, respectively.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |





<span data-ttu-id="a442c-128">La funzione restituisce i dati come un elenco di stringhe.</span><span class="sxs-lookup"><span data-stu-id="a442c-128">The function returns the data as a list of strings.</span></span> <span data-ttu-id="a442c-129">Ogni stringa è con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="a442c-129">Each string is null-terminated.</span></span> <span data-ttu-id="a442c-130">L'ultima stringa è seguita da un carattere di terminazione null aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="a442c-130">The last string is followed by an additional null terminator.</span></span> <span data-ttu-id="a442c-131">Le stringhe sono elencate in coppie.</span><span class="sxs-lookup"><span data-stu-id="a442c-131">The strings are listed in pairs.</span></span> <span data-ttu-id="a442c-132">La prima stringa di ogni coppia è l'indice e la seconda stringa è il testo associato all'indice.</span><span class="sxs-lookup"><span data-stu-id="a442c-132">The first string of each pair is the index, and the second string is the text associated with the index.</span></span> <span data-ttu-id="a442c-133">I dati del contatore utilizzano solo indici con numerazione uniforme, mentre i dati della Guida utilizzano indici dispari.</span><span class="sxs-lookup"><span data-stu-id="a442c-133">The counter data uses only even-numbered indexes, while the help data uses odd-numbered indexes.</span></span> <span data-ttu-id="a442c-134">Le coppie vengono restituite in ordine di indice crescente.</span><span class="sxs-lookup"><span data-stu-id="a442c-134">The pairs are returned in increasing index order.</span></span>

<span data-ttu-id="a442c-135">Negli elenchi seguenti vengono illustrati esempi di contatori e dati della guida.</span><span class="sxs-lookup"><span data-stu-id="a442c-135">The following lists show examples of counter and help data.</span></span> <span data-ttu-id="a442c-136">L'incremento di un valore di indice di un determinato contatore fornisce l'indice al testo della guida del contatore.</span><span class="sxs-lookup"><span data-stu-id="a442c-136">Incrementing a given counter's index value by one gives you the index to the counter's help text.</span></span> <span data-ttu-id="a442c-137">7, ad esempio, è l'indice della Guida associato all'indice del contatore 6.</span><span class="sxs-lookup"><span data-stu-id="a442c-137">For example, 7 is the help index associated with counter index 6.</span></span>

<span data-ttu-id="a442c-138">Coppie di dati contatore.</span><span class="sxs-lookup"><span data-stu-id="a442c-138">Counter data pairs.</span></span>

<dl> <span data-ttu-id="a442c-139">2 sistema 4 memoria 6% tempo processore</span><span class="sxs-lookup"><span data-stu-id="a442c-139">2 System 4 Memory 6 % Processor Time</span></span>
</dl>

<span data-ttu-id="a442c-140">Coppie di dati della guida.</span><span class="sxs-lookup"><span data-stu-id="a442c-140">Help data pairs.</span></span>

<dl> <span data-ttu-id="a442c-141">3 il tipo di oggetto di sistema include i contatori... 5 il tipo di oggetto Memory include i contatori... 7 il tempo processore è espresso come percentuale del...</span><span class="sxs-lookup"><span data-stu-id="a442c-141">3 The System object type includes those counters that ... 5 The Memory object type includes those counters that ... 7 Processor Time is expressed as a percentage of the ...</span></span>
</dl>

<span data-ttu-id="a442c-142">Si noti che la prima coppia di stringhe nei dati del contatore non identifica un nome di contatore e può essere ignorata.</span><span class="sxs-lookup"><span data-stu-id="a442c-142">Note that the first pair of strings in the counter data do not identify a counter name and can be ignored.</span></span> <span data-ttu-id="a442c-143">Il numero di indice della prima coppia è 1 e la stringa è una stringa numerica che rappresenta il valore di indice massimo per i contatori di sistema.</span><span class="sxs-lookup"><span data-stu-id="a442c-143">The index number of the first pair is 1 and the string is a numeric string that represents the maximum index value for system counters.</span></span>

<span data-ttu-id="a442c-144">Per informazioni sul modo in cui un provider carica il nome e il testo della guida, vedere [aggiunta di nomi di contatori e descrizioni al registro di sistema](adding-counter-names-and-descriptions-to-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="a442c-144">For information on how a provider loads the name and help text, see [Adding Counter Names and Descriptions to the Registry](adding-counter-names-and-descriptions-to-the-registry.md).</span></span>

<span data-ttu-id="a442c-145">Nel testo non sono presenti informazioni che indicano se il testo identifica un contatore o un oggetto prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a442c-145">There is no information in the text that indicates if the text identifies a counter or performance object.</span></span> <span data-ttu-id="a442c-146">L'unico modo per determinare questa operazione o la relazione tra i contatori e gli oggetti consiste nell'eseguire una query sui dati relativi alle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a442c-146">The only way to determine this, or the relationship between counters and objects, is to query the performance data itself.</span></span> <span data-ttu-id="a442c-147">Se, ad esempio, si desidera visualizzare un elenco di oggetti e i relativi contatori in un'interfaccia utente, è necessario recuperare i dati sulle prestazioni e quindi utilizzare i valori di indice per analizzare i dati di testo per le stringhe.</span><span class="sxs-lookup"><span data-stu-id="a442c-147">For example, if you want to display a list of objects and their counters in a user interface, you must retrieve the performance data, and then use the index values to parse the text data for the strings.</span></span> <span data-ttu-id="a442c-148">Per un esempio, vedere [visualizzazione di oggetti, istanze e nomi dei contatori](displaying-object-instance-and-counter-names.md).</span><span class="sxs-lookup"><span data-stu-id="a442c-148">For an example that does this, see [Displaying Object, Instance, and Counter Names](displaying-object-instance-and-counter-names.md).</span></span>

<span data-ttu-id="a442c-149">Nell'esempio seguente viene illustrato come utilizzare **HKEY \_ performance \_ NLSTEXT** per recuperare il contatore e il testo della guida e compilare una tabella per l'accesso successivo.</span><span class="sxs-lookup"><span data-stu-id="a442c-149">The following example shows how to use **HKEY\_PERFORMANCE\_NLSTEXT** to retrieve the counter and help text and build a table for subsequent access.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

LPWSTR GetText(LPWSTR pwszSource);
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets);
DWORD GetNumberOfTextEntries(LPWSTR pwszSource);
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets);

void wmain(void)
{
    LPWSTR pCounterTextHead = NULL; // Head of the MULTI_SZ buffer that contains the Counter text.
    LPWSTR pHelpTextHead = NULL;    // Head of the MULTI_SZ buffer that contains the Help text.
    LPDWORD pTextOffsets = NULL;    // Array of DWORDS that contain the offsets to the text in
                                    // pCounterTextHead and pHelpTextHead. The text index
                                    // values mirror the array index.
    DWORD dwNumberOfOffsets = 0;    // Number of elements in the pTextOffsets array.


    pCounterTextHead = GetText(L"Counter");
    if (NULL == pCounterTextHead)
    {
        wprintf(L"GetText(L\"Counter\") failed.\n");
        goto cleanup;
    }

    pHelpTextHead = GetText(L"Help");
    if (NULL == pHelpTextHead)
    {
        wprintf(L"GetText(L\"Help\") failed.\n");
        goto cleanup;
    }

    if (BuildTextTable(pCounterTextHead, pHelpTextHead, &pTextOffsets, &dwNumberOfOffsets))
    {
        PrintCounterAndHelpText(pCounterTextHead, pHelpTextHead, pTextOffsets, dwNumberOfOffsets);
    }
    else
    {
        wprintf(L"BuildTextTable failed.\n");
    }

cleanup:

    if (pCounterTextHead)
        free(pCounterTextHead);

    if (pHelpTextHead)
        free(pHelpTextHead);

    if (pTextOffsets)
        free(pTextOffsets);

    // You do not need to call RegCloseKey if you are only
    // retrieving names and help text.
}


// Get the text based on the source value. This function uses the
// HKEY_PERFORMANCE_NLSTEXT key to get the strings.
LPWSTR GetText(LPWSTR pwszSource)
{
    LPWSTR pBuffer = NULL;
    DWORD dwBufferSize = 0;
    LONG status = ERROR_SUCCESS;

    // Query the size of the text data so you can allocate the buffer.
    status = RegQueryValueEx(HKEY_PERFORMANCE_NLSTEXT, pwszSource, NULL, NULL, NULL, &dwBufferSize);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed getting required buffer size. Error is 0x%x.\n", status);
        goto cleanup;
    }

    // Allocate the text buffer and query the text.
    pBuffer = (LPWSTR)malloc(dwBufferSize);
    if (pBuffer)
    {
        status = RegQueryValueEx(HKEY_PERFORMANCE_NLSTEXT, pwszSource, NULL, NULL, (LPBYTE)pBuffer, &dwBufferSize);
        if (ERROR_SUCCESS != status)
        {
            wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
            free(pBuffer);
            pBuffer = NULL;
            goto cleanup;
        }
    }
    else
    {
        wprintf(L"malloc failed to allocate memory.\n");
    }

cleanup:

    return pBuffer;
}


// Build a table of offsets into the counter and help text buffers. Use the index
// values from the performance data queries to access the offsets.
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets)
{
    BOOL fSuccess = FALSE;
    LPWSTR pwszCounterText = NULL;  // Used to cycle through the Counter text
    LPWSTR pwszHelpText = NULL;     // Used to cycle through the Help text
    LPDWORD pOffsets = NULL;
    DWORD dwCounterIndex = 0;       // Index value of the Counter text
    DWORD dwHelpIndex = 0;          // Index value of the Help text
    DWORD dwSize = 0;               // Size of the block of memory that holds the offset array


    pwszCounterText = pCounterHead;
    pwszHelpText = pHelpHead;

    *pNumberOfOffsets = GetNumberOfTextEntries(L"Last Help");
    if (0 == *pNumberOfOffsets)
    {
        wprintf(L"GetNumberOfTextEntries failed; returned 0 for number of entries.\n");
        goto cleanup;
    }

    dwSize = sizeof(DWORD) * (*pNumberOfOffsets + 1);  // Add one to make the array one-based

    pOffsets = (LPDWORD)malloc(dwSize);
    if (pOffsets)
    {
        ZeroMemory(pOffsets, dwSize);
        *pOffsetsHead = pOffsets;

        // Bypass first record (pair) of the counter data - contains upper bounds of system counter index.
        pwszCounterText += (wcslen(pwszCounterText)+1);
        pwszCounterText += (wcslen(pwszCounterText)+1);

        for (; *pwszCounterText; pwszCounterText += (wcslen(pwszCounterText)+1))
        {
            dwCounterIndex = _wtoi(pwszCounterText);
            dwHelpIndex = _wtoi(pwszHelpText);

            // Use the counter's index value as an indexer into the pOffsets array.
            // Store the offset to the counter text in the array element.
            pwszCounterText += (wcslen(pwszCounterText)+1);  //Skip past index value
            pOffsets[dwCounterIndex] = (DWORD)(pwszCounterText - pCounterHead);

            // Some help indexes for system counters do not have a matching counter, so loop
            // until you find the matching help index or the index is greater than the corresponding
            // counter index. For example, if the indexes were as follows, you would loop
            // until the help index was 11.
            //
            // Counter index       Help Index
            //   2                    3
            //   4                    5
            //   6                    7
            //                        9   (skip because there is no matching Counter index)
            //   10                   11
            while (*pwszHelpText && dwHelpIndex < dwCounterIndex)
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past index value
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past help text to the next index value
                dwHelpIndex = _wtoi(pwszHelpText);
            }

            // Use the Help index value as an indexer into the pOffsets array.
            // Store the offset to the help text in the array element.
            if (dwHelpIndex == (dwCounterIndex + 1))
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past index value
                pOffsets[dwHelpIndex] = (DWORD)(pwszHelpText - pHelpHead);
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past help text to next index value
            }
        }

        fSuccess = TRUE;
    }

cleanup:

    return fSuccess;
}


// Retrieve the last help index used from the registry. Use this number
// to allocate an array of DWORDs. Note that index values are not contiguous.
DWORD GetNumberOfTextEntries(LPWSTR pwszSource)
{
    DWORD dwEntries = 0;
    LONG status = ERROR_SUCCESS;
    HKEY hkey = NULL;
    DWORD dwSize = sizeof(DWORD);
    LPWSTR pwszMessage = NULL;

    status = RegOpenKeyEx(HKEY_LOCAL_MACHINE,
        L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib",
        0,
        KEY_READ,
        &hkey);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegOpenKeyEx failed with 0x%x.\n", status);
        goto cleanup;
    }

    status = RegQueryValueEx(hkey, pwszSource, NULL, 0, (LPBYTE)&dwEntries, &dwSize);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
    }

cleanup:

    if (hkey)
        RegCloseKey(hkey);

    return dwEntries;
}


// Print the pairs of counter and help text.
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets)
{    UNREFERENCED_PARAMETER(dwNumberOfOffsets);
    // Counter index values are even numbers that start at 2 so begin with
    // the second element of the array of offsets. Many array elements will
    // not contain offset values (index values are not contiguous).

    // There is typically a large number of counters, so this example prints
    // the first 10 counters and help text.
    //for (DWORD i = 2; i < (dwNumberOfOffsets+1); i++)

    for (DWORD i = 2; i < 22; i++)
    {
        if (pTextOffsets[i]) // If index offset is not zero
        {
            if (0 == (i % 2)) // Counter text index (even number)
                wprintf(L"%d %s\n", i, pCounterTextHead+pTextOffsets[i]);
            else
                wprintf(L"%d %s\n\n", i, pHelpTextHead+pTextOffsets[i]);
        }
    }
}
```



<span data-ttu-id="a442c-150">Nell'esempio seguente viene illustrato come utilizzare **i \_ \_ dati sulle prestazioni di HKEY** per recuperare il testo del contatore.</span><span class="sxs-lookup"><span data-stu-id="a442c-150">The following example shows how to use **HKEY\_PERFORMANCE\_DATA** to retrieve the counter text.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <strsafe.h>

#pragma comment(lib, "advapi32.lib")

LPWSTR GetText(LPWSTR pwszSource);
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets);
DWORD GetNumberOfTextEntries(LPWSTR pwszSource);
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets);
LANGID GetLanguageId();

void wmain(void)
{
    LPWSTR pCounterTextHead = NULL; // Head of the MULTI_SZ buffer that contains the Counter text.
    LPWSTR pHelpTextHead = NULL;    // Head of the MULTI_SZ buffer that contains the Help text.
    LPDWORD pTextOffsets = NULL;    // Array of DWORDS that contain the offsets to the text in
                                    // pCounterTextHead and pHelpTextHead. The text index
                                    // values mirror the array index.
    DWORD dwNumberOfOffsets = 0;    // Number of elements in the pTextOffsets array.

    pCounterTextHead = GetText(L"Counter");
    if (NULL == pCounterTextHead)
    {
        wprintf(L"GetText(L\"Counter\") failed.\n");
        goto cleanup;
    }

    pHelpTextHead = GetText(L"Help");
    if (NULL == pHelpTextHead)
    {
        wprintf(L"GetText(L\"Help\") failed.\n");
        goto cleanup;
    }

    if (BuildTextTable(pCounterTextHead, pHelpTextHead, &pTextOffsets, &dwNumberOfOffsets))
    {
        PrintCounterAndHelpText(pCounterTextHead, pHelpTextHead, pTextOffsets, dwNumberOfOffsets);
    }
    else
    {
        wprintf(L"BuildTextTable failed.\n");
    }

cleanup:

    if (pCounterTextHead)
        free(pCounterTextHead);

    if (pHelpTextHead)
        free(pHelpTextHead);

    if (pTextOffsets)
        free(pTextOffsets);

    // You do not need to call RegCloseKey if you are only
    // retrieving names and help text.
}


// Get the text based on the source value. This function uses the
// HKEY_PERFORMANCE_DATA key to get the strings.
LPWSTR GetText(LPWSTR pwszSource)
{
    LPWSTR pBuffer = NULL;
    DWORD dwBufferSize = 0;
    LONG status = ERROR_SUCCESS;
    LANGID langid = 0;
    WCHAR wszSourceAndLangId[15];   // Identifies the source of the text; either
                                    // "Counter <langid>" or "Help <langid>"


    // Create the lpValueName string for the registry query.
    langid = GetLanguageId();
    if (0 == langid)
    {
        wprintf(L"GetLanguageId failed to get the default language identifier.\n");
        goto cleanup;
    }

    StringCchPrintf(wszSourceAndLangId, 15, L"%s %03x", pwszSource, langid);

    // Query the size of the text data so you can allocate the buffer.
    status = RegQueryValueEx(HKEY_PERFORMANCE_DATA, wszSourceAndLangId, NULL, NULL, NULL, &dwBufferSize);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed getting required buffer size. Error is 0x%x.\n", status);
        goto cleanup;
    }

    // Allocate the text buffer and query the text.
    pBuffer = (LPWSTR)malloc(dwBufferSize);
    if (pBuffer)
    {
        status = RegQueryValueEx(HKEY_PERFORMANCE_DATA, wszSourceAndLangId, NULL, NULL, (LPBYTE)pBuffer, &dwBufferSize);
        if (ERROR_SUCCESS != status)
        {
            wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
            free(pBuffer);
            pBuffer = NULL;
            goto cleanup;
        }
    }
    else
    {
        wprintf(L"malloc failed to allocate memory.\n");
    }

cleanup:

    return pBuffer;
}


// Retrieve the default language identifier of the current user. For most languages,
// you use the primary language identifier only to retrieve the text. In Windows XP and
// Windows Server 2003, you use the complete language identifier to retrieve Chinese
// text. In Windows Vista, you use the complete language identifier to retrieve Portuguese
// text.
LANGID GetLanguageId()
{
    LANGID langid = 0;  // Complete language identifier.
    WORD primary = 0;   // Primary language identifier.
    OSVERSIONINFO osvi;

    ZeroMemory(&osvi, sizeof(OSVERSIONINFO));
    osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFO);

    if (GetVersionEx(&osvi))
    {
        langid = GetUserDefaultUILanguage();
        primary = PRIMARYLANGID(langid);

        if ( (LANG_PORTUGUESE == primary && osvi.dwBuildNumber > 5) || // Windows Vista and later
             (LANG_CHINESE == primary && (osvi.dwMajorVersion == 5 && osvi.dwMinorVersion >= 1)) ) // XP and Windows Server 2003
        {
            ; //Use the complete language identifier.
        }
        else
        {
            langid = primary;
        }
    }
    else
    {
        wprintf(L"GetVersionEx failed with 0x%x.\n", GetLastError());
    }

    return langid;
}


// Build a table of offsets into the counter and help text buffers. Use the index
// values from the performance data queries to access the offsets.
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets)
{
    BOOL fSuccess = FALSE;
    LPWSTR pwszCounterText = NULL;  // Used to cycle through the Counter text
    LPWSTR pwszHelpText = NULL;     // Used to cycle through the Help text
    LPDWORD pOffsets = NULL;
    DWORD dwCounterIndex = 0;       // Index value of the Counter text
    DWORD dwHelpIndex = 0;          // Index value of the Help text
    DWORD dwSize = 0;               // Size of the block of memory that holds the offset array

    pwszCounterText = pCounterHead;
    pwszHelpText = pHelpHead;

    *pNumberOfOffsets = GetNumberOfTextEntries(L"Last Help");
    if (0 == *pNumberOfOffsets)
    {
        wprintf(L"GetNumberOfTextEntries failed; returned 0 for number of entries.\n");
        goto cleanup;
    }

    dwSize = sizeof(DWORD) * (*pNumberOfOffsets + 1);  // Add one to make the array one-based

    pOffsets = (LPDWORD)malloc(dwSize);
    if (pOffsets)
    {
        ZeroMemory(pOffsets, dwSize);
        *pOffsetsHead = pOffsets;

        // Bypass first record (pair) of the counter data - contains upper bounds of system counter index.
        pwszCounterText += (wcslen(pwszCounterText)+1);
        pwszCounterText += (wcslen(pwszCounterText)+1);

        for (; *pwszCounterText; pwszCounterText += (wcslen(pwszCounterText)+1))
        {
            dwCounterIndex = _wtoi(pwszCounterText);
            dwHelpIndex = _wtoi(pwszHelpText);

            // Use the counter's index value as an indexer into the pOffsets array.
            // Store the offset to the counter text in the array element.
            pwszCounterText += (wcslen(pwszCounterText)+1);  //Skip past index value
            pOffsets[dwCounterIndex] = (DWORD)(pwszCounterText - pCounterHead);

            // Some help indexes for system counters do not have a matching counter, so loop
            // until you find the matching help index or the index is greater than the corresponding
            // counter index. For example, if the indexes were as follows, you would loop
            // until the help index was 11.
            //
            // Counter index       Help Index
            //   2                    3
            //   4                    5
            //   6                    7
            //                        9   (skip because there is no matching Counter index)
            //   10                   11
            while (*pwszHelpText && dwHelpIndex < dwCounterIndex)
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past index value
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past help text to the next index value
                dwHelpIndex = _wtoi(pwszHelpText);
            }

            // Use the Help index value as an indexer into the pOffsets array.
            // Store the offset to the help text in the array element.
            if (dwHelpIndex == (dwCounterIndex + 1))
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past index value
                pOffsets[dwHelpIndex] = (DWORD)(pwszHelpText - pHelpHead);
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past help text to next index value
            }
        }

        fSuccess = TRUE;
    }

cleanup:

    return fSuccess;
}


// Retrieve the last help index used from the registry. Use this number
// to allocate an array of DWORDs. Note that index values are not contiguous.
DWORD GetNumberOfTextEntries(LPWSTR pwszSource)
{
    DWORD dwEntries = 0;
    LONG status = ERROR_SUCCESS;
    HKEY hkey = NULL;
    DWORD dwSize = sizeof(DWORD);
    LPWSTR pwszMessage = NULL;

    status = RegOpenKeyEx(HKEY_LOCAL_MACHINE,
        L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib",
        0,
        KEY_READ,
        &hkey);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegOpenKeyEx failed with 0x%x.\n", status);
        goto cleanup;
    }

    status = RegQueryValueEx(hkey, pwszSource, NULL, 0, (LPBYTE)&dwEntries, &dwSize);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
    }

cleanup:

    if (hkey)
        RegCloseKey(hkey);

    return dwEntries;
}


// Print the pairs of counter and help text.
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets)
{   UNREFERENCED_PARAMETER(dwNumberOfOffsets);
    // Counter index values are even numbers that start at 2 so begin with
    // the second element of the array of offsets. Many array elements will
    // not contain offset values (index values are not contiguous).

    // There is typically a large number of counters, so this example prints
    // the first 10 counters and help text.
    //for (DWORD i = 2; i < (dwNumberOfOffsets+1); i++)

    for (DWORD i = 2; i < 22; i++)
    {
        if (pTextOffsets[i]) // If index offset is not zero
        {
            if (0 == (i % 2)) // Counter text index (even number)
                wprintf(L"%d %s\n", i, pCounterTextHead+pTextOffsets[i]);
            else
                wprintf(L"%d %s\n\n", i, pHelpTextHead+pTextOffsets[i]);
        }
    }
}
```

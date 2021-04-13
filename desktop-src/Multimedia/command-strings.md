---
title: Stringhe di comando
description: Stringhe di comando
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- Stringhe di comando MCI, informazioni
- Stringhe di comando MCI, sintassi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b62013abff091f668a3b045e9f3ca2e8745f0d9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398860"
---
# <a name="command-strings"></a><span data-ttu-id="25f2f-105">Stringhe di comando</span><span class="sxs-lookup"><span data-stu-id="25f2f-105">Command Strings</span></span>

<span data-ttu-id="25f2f-106">Per inviare un comando stringa a un dispositivo MCI, usare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , che include i parametri per il comando stringa e un buffer per tutte le informazioni restituite.</span><span class="sxs-lookup"><span data-stu-id="25f2f-106">To send a string command to an MCI device, use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function, which includes parameters for the string command and a buffer for any returned information.</span></span>

<span data-ttu-id="25f2f-107">La funzione **mciSendString** restituisce zero in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="25f2f-107">The **mciSendString** function returns zero if successful.</span></span> <span data-ttu-id="25f2f-108">Se la funzione ha esito negativo, la parola di ordine inferiore del valore restituito contiene un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="25f2f-108">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="25f2f-109">È possibile passare questo codice di errore alla funzione [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) per ottenere una descrizione di testo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="25f2f-109">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-strings"></a><span data-ttu-id="25f2f-110">Sintassi delle stringhe di comando</span><span class="sxs-lookup"><span data-stu-id="25f2f-110">Syntax of Command Strings</span></span>

<span data-ttu-id="25f2f-111">Le stringhe di comando MCI usano una sintassi coerente di modificatore di oggetti verbo.</span><span class="sxs-lookup"><span data-stu-id="25f2f-111">MCI command strings use a consistent verb-object-modifier syntax.</span></span> <span data-ttu-id="25f2f-112">Ogni stringa di comando include un comando, un identificatore di dispositivo e gli argomenti del comando.</span><span class="sxs-lookup"><span data-stu-id="25f2f-112">Each command string includes a command, a device identifier, and command arguments.</span></span> <span data-ttu-id="25f2f-113">Gli argomenti sono facoltativi per alcuni comandi e sono obbligatori per altri.</span><span class="sxs-lookup"><span data-stu-id="25f2f-113">Arguments are optional for some commands and required for others.</span></span>

<span data-ttu-id="25f2f-114">Una stringa di comando ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="25f2f-114">A command string has the following form:</span></span>

<span data-ttu-id="25f2f-115">*\_argomenti ID dispositivo comando*</span><span class="sxs-lookup"><span data-stu-id="25f2f-115">*command device\_id arguments*</span></span>

<span data-ttu-id="25f2f-116">Questi componenti contengono le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="25f2f-116">These components contain the following information:</span></span>

-   <span data-ttu-id="25f2f-117">Il *comando* specifica un comando MCI, ad esempio [**Open**](open.md), [**Close**](close.md)o [**Play**](play.md).</span><span class="sxs-lookup"><span data-stu-id="25f2f-117">The *command* specifies an MCI command, such as [**open**](open.md), [**close**](close.md), or [**play**](play.md).</span></span>
-   <span data-ttu-id="25f2f-118">L' *\_ ID dispositivo* identifica un'istanza di un driver MCI.</span><span class="sxs-lookup"><span data-stu-id="25f2f-118">The *device\_id* identifies an instance of an MCI driver.</span></span> <span data-ttu-id="25f2f-119">L' *\_ ID dispositivo* viene creato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="25f2f-119">The *device\_id* is created when the device is opened.</span></span>
-   <span data-ttu-id="25f2f-120">Gli *argomenti* specificano i flag e le variabili utilizzati dal comando.</span><span class="sxs-lookup"><span data-stu-id="25f2f-120">The *arguments* specify the flags and variables used by the command.</span></span> <span data-ttu-id="25f2f-121">I flag sono parole chiave riconosciute con il comando MCI.</span><span class="sxs-lookup"><span data-stu-id="25f2f-121">Flags are keywords recognized with the MCI command.</span></span> <span data-ttu-id="25f2f-122">Le variabili sono numeri o stringhe che si applicano al comando o al flag MCI.</span><span class="sxs-lookup"><span data-stu-id="25f2f-122">Variables are numbers or strings that apply to the MCI command or flag.</span></span>

    <span data-ttu-id="25f2f-123">Ad esempio, il comando **Play** usa gli argomenti "from *position* " e "to *position* " per indicare le posizioni in cui iniziare e terminare Play.</span><span class="sxs-lookup"><span data-stu-id="25f2f-123">For example, the **play** command uses the arguments "from *position* " and "to *position* " to indicate the positions at which to start and end play.</span></span> <span data-ttu-id="25f2f-124">È possibile elencare i flag utilizzati con un comando in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="25f2f-124">You can list the flags used with a command in any order.</span></span> <span data-ttu-id="25f2f-125">Quando si usa un flag a cui è associata una variabile, è necessario specificare un valore per la variabile.</span><span class="sxs-lookup"><span data-stu-id="25f2f-125">When you use a flag that has a variable associated with it, you must supply a value for the variable.</span></span>

    <span data-ttu-id="25f2f-126">Gli argomenti del comando non specificati (e facoltativi) presuppongono un valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="25f2f-126">Unspecified (and optional) command arguments assume a default value.</span></span>

<span data-ttu-id="25f2f-127">La funzione di esempio seguente invia il comando [**Play**](play.md) con i flag "from" e "to".</span><span class="sxs-lookup"><span data-stu-id="25f2f-127">The following example function sends the [**play**](play.md) command with the "from" and "to" flags.</span></span>


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



## <a name="data-types-for-command-variables"></a><span data-ttu-id="25f2f-128">Tipi di dati per le variabili di comando</span><span class="sxs-lookup"><span data-stu-id="25f2f-128">Data Types for Command Variables</span></span>

<span data-ttu-id="25f2f-129">È possibile utilizzare i tipi di dati seguenti per le variabili in una stringa di comando.</span><span class="sxs-lookup"><span data-stu-id="25f2f-129">You can use the following data types for the variables in a command string.</span></span>



| <span data-ttu-id="25f2f-130">**Tipo di dati**</span><span class="sxs-lookup"><span data-stu-id="25f2f-130">**Data type**</span></span>        | <span data-ttu-id="25f2f-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="25f2f-131">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25f2f-132">Stringhe</span><span class="sxs-lookup"><span data-stu-id="25f2f-132">Strings</span></span>              | <span data-ttu-id="25f2f-133">I tipi di dati stringa sono delimitati da spazi vuoti iniziali e finali e virgolette.</span><span class="sxs-lookup"><span data-stu-id="25f2f-133">String data types are delimited by leading and trailing white spaces and quotation marks.</span></span> <span data-ttu-id="25f2f-134">MCI rimuove le virgolette singole da una stringa.</span><span class="sxs-lookup"><span data-stu-id="25f2f-134">MCI removes single quotation marks from a string.</span></span> <span data-ttu-id="25f2f-135">Per inserire le virgolette in una stringa, utilizzare un set di due virgolette in cui si desidera incorporare le virgolette.</span><span class="sxs-lookup"><span data-stu-id="25f2f-135">To put a quotation mark in a string, use a set of two quotation marks where you want to embed your quotation mark.</span></span> <span data-ttu-id="25f2f-136">Per usare una stringa vuota, usare due virgolette delimitate da spazi vuoti iniziali e finali.</span><span class="sxs-lookup"><span data-stu-id="25f2f-136">To use an empty string, use two quotation marks delimited by leading and trailing white spaces.</span></span> |
| <span data-ttu-id="25f2f-137">Integer long con segno</span><span class="sxs-lookup"><span data-stu-id="25f2f-137">Signed long integers</span></span> | <span data-ttu-id="25f2f-138">I tipi di dati long integer con segno sono delimitati da spazi vuoti iniziali e finali.</span><span class="sxs-lookup"><span data-stu-id="25f2f-138">Signed long integer data types are delimited by leading and trailing white spaces.</span></span> <span data-ttu-id="25f2f-139">Se non diversamente specificato, i numeri interi possono essere positivi o negativi.</span><span class="sxs-lookup"><span data-stu-id="25f2f-139">Unless otherwise specified, integers can be positive or negative.</span></span> <span data-ttu-id="25f2f-140">Se si utilizzano numeri interi negativi, è consigliabile non separare il segno meno e la prima cifra con uno spazio.</span><span class="sxs-lookup"><span data-stu-id="25f2f-140">If you use negative integers, you should not separate the minus sign and the first digit with a space.</span></span>                                                                                                    |
| <span data-ttu-id="25f2f-141">Rettangoli</span><span class="sxs-lookup"><span data-stu-id="25f2f-141">Rectangles</span></span>           | <span data-ttu-id="25f2f-142">I tipi di dati Rectangle sono un elenco ordinato di quattro valori short con segno.</span><span class="sxs-lookup"><span data-stu-id="25f2f-142">Rectangle data types are an ordered list of four signed short values.</span></span> <span data-ttu-id="25f2f-143">Lo spazio vuoto delimita questo tipo di dati e separa ogni intero nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="25f2f-143">White space delimits this data type and separates each integer in the list.</span></span>                                                                                                                                                                                                              |



 

 

 
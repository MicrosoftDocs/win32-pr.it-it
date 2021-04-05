---
title: Dizionario nome visualizzato set di proprietà
description: Un dizionario di nomi visualizzati delle proprietà consente agli utenti del set di proprietà di alleghire il significato alle proprietà, oltre a quelle fornite dall'indicatore del tipo.
ms.assetid: b6813a86-39d3-4754-86e4-51035a7c91d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd844b4d37d4f10434fc5b73f936b4b6565c1506
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729071"
---
# <a name="property-set-display-name-dictionary"></a><span data-ttu-id="a4f2b-103">Dizionario nome visualizzato set di proprietà</span><span class="sxs-lookup"><span data-stu-id="a4f2b-103">Property Set Display Name Dictionary</span></span>

<span data-ttu-id="a4f2b-104">Un dizionario di nomi visualizzati delle proprietà consente agli utenti del set di proprietà di alleghire il significato alle proprietà, oltre a quelle fornite dall'indicatore del tipo.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-104">A dictionary of property display names enables property set users to attach meaning to properties - beyond those provided by the type indicator.</span></span>

## <a name="dictionary-structure"></a><span data-ttu-id="a4f2b-105">Struttura del dizionario</span><span class="sxs-lookup"><span data-stu-id="a4f2b-105">Dictionary Structure</span></span>

<span data-ttu-id="a4f2b-106">Il dizionario contiene un conteggio delle voci nell'elenco, seguito da un elenco di voci del dizionario.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-106">The dictionary contains a count of entries in the list, followed by a list of dictionary entries.</span></span>

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a><span data-ttu-id="a4f2b-107">Struttura di immissione del dizionario</span><span class="sxs-lookup"><span data-stu-id="a4f2b-107">Dictionary Entry Structure</span></span>

<span data-ttu-id="a4f2b-108">Ogni voce di dizionario nell'elenco è una coppia identificatore/stringa della proprietà.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-108">Each dictionary entry in the list is a Property Identifier/String pair.</span></span> <span data-ttu-id="a4f2b-109">Di seguito è riportata una definizione di pseudo-struttura per una voce del dizionario.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-109">The following is a pseudo-structure definition for a dictionary entry.</span></span> <span data-ttu-id="a4f2b-110">Si tratta di una pseudo-struttura perché il \[ \] membro SZ è di dimensioni variabili.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-110">It's a pseudo-structure because the sz\[\] member is variable in size.</span></span>

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a><span data-ttu-id="a4f2b-111">Dizionario di esempio</span><span class="sxs-lookup"><span data-stu-id="a4f2b-111">Sample Dictionary</span></span>

<span data-ttu-id="a4f2b-112">Il seguente esempio di trasferimento dei dati sul mercato azionario potrebbe includere un nome visualizzabile "quotazioni azionarie" per l'intero set e "simbolo di spunta" per il \_ simbolo PID.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-112">The following stock market data transfer example might include a displayable name "Stock Quote" for the entire set, and "Ticker Symbol" for PID\_SYMBOL.</span></span> <span data-ttu-id="a4f2b-113">Se un set di proprietà contiene solo un simbolo e il dizionario, la sezione del set di proprietà avrà un flusso di byte simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-113">If a property set contained just a symbol and the dictionary, the property set section would have a byte stream that looked like the following.</span></span>

``` syntax
Offset     Bytes 
; Start of section 
0000    5C 01 00 00    ; DWORD size of section 
0004    04 00 00 00    ; DWORD number of properties in section 
 
; Start of PropID/Offset pairs 
0008    01 00 00 00    ; DWORD Property ID (1 == code page) 
000C    28 00 00 00    ; DWORD offset to property ID 
0010    00 00 00 80    ; DWORD Property ID (0x80000000 == locale
                                                 ID) 
0014    30 00 00 00    ; DWORD offset to property ID 
0018    00 00 00 00    ; DWORD Property ID (0 == dictionary) 
001C    38 00 00 00    ; DWORD offset to property ID 
0020    07 00 00 00    ; DWORD Property ID (7 == PID_SYMBOL)
0024    5C 01 00 00    ; DWORD offset to property ID
 
; Start of Property 1 (code page)
0028    01 00 00 00    ; DWORD type indicator (VT_12)
002C    B0 04          ; USHORT codepage (0x04b0 == 1200 ==
                                                 unicode)
002E    00 00          ; Pad to 32-bit boundary
 
; Start of Property 0x80000000 (Local ID)
0030    13 00 00 00    ; DWORD type indicator (VT_U14)
0034    09 04 00 00    ; ULONG locale ID (0x0409 == American 
                                                 English)
 
; Start of Property 0 (the dictionary)
0038    08 00 00 00    ; DWORD number of entries in dictionary
                             (Note:  No type indicator)
003C    00 00 00 00    ; DWORD propid == 0 (the dictionary)
0040    0C 00 00 00    ; DWORD cch == wcslen(L"Stock Quote") +
                                                 sizeof(L'\0') == 12
0044    L"Stock Quote" ; wchar_t wsz(12)
005C    05 00 00 00    ; DWORD propid == 5 (PID_HIGH)
0060    0B 00 00 00    ; DWORD cch == wcslen(L"High Price") + 
                                                 sizeof(L'\0') == 11
0064    L"High Price\0"; wchar_t wsz(11)
007A    00 00          ; padding for 32-bit alignment (necessary
                             because the codepage is unicode)
007C    07 00 00 00    ; DWORD propid == 7 (PID_SYMBOL)
0080    0E 00 00 00    ; DWORD cch - wcslen(L"Ticker Symbol\0") 
                             == 14
0084    L"Ticker Symbol\0" ; wchar_t wsz(14)
 
    // The dictionary would continue, but may not contain entries 
    // for every possible property, and may contain entries for 
    // properties that are not present. Entries are not required  
    // to be in order.
```

<span data-ttu-id="a4f2b-114">Tenere presente i seguenti problemi relativi ai dizionari dei set di proprietà:</span><span class="sxs-lookup"><span data-stu-id="a4f2b-114">Be aware of the following issues regarding property set dictionaries:</span></span>

-   <span data-ttu-id="a4f2b-115">L'ID di proprietà 0 non ha un indicatore di tipo.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-115">Property ID 0 does not have a type indicator.</span></span> <span data-ttu-id="a4f2b-116">Il tipo di dati **DWORD** che indica il numero di voci risiede nella posizione dell'indicatore del tipo.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-116">The **DWORD** data type that indicates the count of entries sits in the type-indicator position.</span></span>
-   <span data-ttu-id="a4f2b-117">Il numero di caratteri nella stringa di attestazione include il carattere zero che termina *la stringa.*</span><span class="sxs-lookup"><span data-stu-id="a4f2b-117">The count of characters in the *cch* string includes the zero character that terminates the string.</span></span> <span data-ttu-id="a4f2b-118">Quando la tabella codici della proprietà impostata non è Unicode, questo campo è effettivamente un numero di **byte** .</span><span class="sxs-lookup"><span data-stu-id="a4f2b-118">When the codepage of the property set is not Unicode, this field is actually a **byte** count.</span></span> <span data-ttu-id="a4f2b-119">Per i set di proprietà con una versione di formato 0, questo conteggio non può essere maggiore di 256.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-119">For property sets with a format version of 0, this count may not exceed 256.</span></span> <span data-ttu-id="a4f2b-120">Per i set di proprietà con una versione di formato 1, questo conteggio può avere dimensioni pari a quelle consentite dalla dimensione totale del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-120">For property sets with a format version of 1, this count may be as large as is allowed by the total property set size.</span></span>
-   <span data-ttu-id="a4f2b-121">Il dizionario è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-121">The dictionary is optional.</span></span> <span data-ttu-id="a4f2b-122">Non è necessario che tutti i nomi delle proprietà nel set siano presenti nel dizionario.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-122">Not all the names of properties in the set are required to appear in the dictionary.</span></span> <span data-ttu-id="a4f2b-123">Viceversa, non tutti i nomi nel dizionario devono corrispondere alle proprietà nel set.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-123">Conversely, not all names in the dictionary are required to correspond to properties in the set.</span></span> <span data-ttu-id="a4f2b-124">Il dizionario deve omettere le voci per le proprietà che si presuppone vengano riconosciute universalmente dalle applicazioni che modificano il set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-124">The dictionary should omit entries for properties assumed to be universally recognized by applications manipulating the property set.</span></span> <span data-ttu-id="a4f2b-125">In genere, i nomi per i set di proprietà di base per gli standard ampiamente accettati vengono omessi, ma i set di proprietà per scopi specifici possono includere dizionari per l'uso da parte dei browser.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-125">Typically, names for the base property sets for widely-accepted standards are omitted, but special-purpose property sets may include dictionaries for use by browsers.</span></span>
-   <span data-ttu-id="a4f2b-126">I nomi delle proprietà nel dizionario vengono archiviati nella tabella codici indicata dalla [proprietà ID 1](/windows/desktop/Stg/reserved-property-identifiers).</span><span class="sxs-lookup"><span data-stu-id="a4f2b-126">Property names in the dictionary are stored in the code page indicated by [Property ID 1](/windows/desktop/Stg/reserved-property-identifiers).</span></span> <span data-ttu-id="a4f2b-127">Per le tabelle codici ANSI, ogni voce del dizionario è allineata ai byte.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-127">For ANSI code pages, each dictionary entry is byte-aligned.</span></span> <span data-ttu-id="a4f2b-128">Non esiste pertanto alcuna spaziatura tra i nomi di proprietà con ID proprietà 0.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-128">Thus, there is no spacing between property names with Property ID 0.</span></span> <span data-ttu-id="a4f2b-129">Questo è l'unico caso in cui i valori dei tipi di dati **DWORD** (ID della proprietà e **valore DWORD** di lunghezza del nome della proprietà) non devono essere allineati sui limiti a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-129">This is the only case where values of **DWORD** data types (the property ID and property name-length **DWORD** s) are not required to be aligned on 32-bit boundaries.</span></span> <span data-ttu-id="a4f2b-130">Per le pagine Unicode, ogni voce del dizionario è allineata a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-130">For Unicode pages, each dictionary entry is 32-bit aligned.</span></span>
-   <span data-ttu-id="a4f2b-131">I nomi di proprietà che iniziano con i caratteri Unicode binari 0x0001 tramite 0x001F sono riservati per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-131">Property names that begin with the binary Unicode characters 0x0001 through 0x001F are reserved for future use.</span></span>
-   <span data-ttu-id="a4f2b-132">Il nome della proprietà associato all'ID di proprietà 0 rappresenta il nome dell'intero set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="a4f2b-132">The property name associated with Property ID 0 represents the name of the entire property set.</span></span>

 

 
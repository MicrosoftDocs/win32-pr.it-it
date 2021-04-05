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
# <a name="property-set-display-name-dictionary"></a>Dizionario nome visualizzato set di proprietà

Un dizionario di nomi visualizzati delle proprietà consente agli utenti del set di proprietà di alleghire il significato alle proprietà, oltre a quelle fornite dall'indicatore del tipo.

## <a name="dictionary-structure"></a>Struttura del dizionario

Il dizionario contiene un conteggio delle voci nell'elenco, seguito da un elenco di voci del dizionario.

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a>Struttura di immissione del dizionario

Ogni voce di dizionario nell'elenco è una coppia identificatore/stringa della proprietà. Di seguito è riportata una definizione di pseudo-struttura per una voce del dizionario. Si tratta di una pseudo-struttura perché il \[ \] membro SZ è di dimensioni variabili.

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a>Dizionario di esempio

Il seguente esempio di trasferimento dei dati sul mercato azionario potrebbe includere un nome visualizzabile "quotazioni azionarie" per l'intero set e "simbolo di spunta" per il \_ simbolo PID. Se un set di proprietà contiene solo un simbolo e il dizionario, la sezione del set di proprietà avrà un flusso di byte simile al seguente.

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

Tenere presente i seguenti problemi relativi ai dizionari dei set di proprietà:

-   L'ID di proprietà 0 non ha un indicatore di tipo. Il tipo di dati **DWORD** che indica il numero di voci risiede nella posizione dell'indicatore del tipo.
-   Il numero di caratteri nella stringa di attestazione include il carattere zero che termina *la stringa.* Quando la tabella codici della proprietà impostata non è Unicode, questo campo è effettivamente un numero di **byte** . Per i set di proprietà con una versione di formato 0, questo conteggio non può essere maggiore di 256. Per i set di proprietà con una versione di formato 1, questo conteggio può avere dimensioni pari a quelle consentite dalla dimensione totale del set di proprietà.
-   Il dizionario è facoltativo. Non è necessario che tutti i nomi delle proprietà nel set siano presenti nel dizionario. Viceversa, non tutti i nomi nel dizionario devono corrispondere alle proprietà nel set. Il dizionario deve omettere le voci per le proprietà che si presuppone vengano riconosciute universalmente dalle applicazioni che modificano il set di proprietà. In genere, i nomi per i set di proprietà di base per gli standard ampiamente accettati vengono omessi, ma i set di proprietà per scopi specifici possono includere dizionari per l'uso da parte dei browser.
-   I nomi delle proprietà nel dizionario vengono archiviati nella tabella codici indicata dalla [proprietà ID 1](/windows/desktop/Stg/reserved-property-identifiers). Per le tabelle codici ANSI, ogni voce del dizionario è allineata ai byte. Non esiste pertanto alcuna spaziatura tra i nomi di proprietà con ID proprietà 0. Questo è l'unico caso in cui i valori dei tipi di dati **DWORD** (ID della proprietà e **valore DWORD** di lunghezza del nome della proprietà) non devono essere allineati sui limiti a 32 bit. Per le pagine Unicode, ogni voce del dizionario è allineata a 32 bit.
-   I nomi di proprietà che iniziano con i caratteri Unicode binari 0x0001 tramite 0x001F sono riservati per un uso futuro.
-   Il nome della proprietà associato all'ID di proprietà 0 rappresenta il nome dell'intero set di proprietà.

 

 
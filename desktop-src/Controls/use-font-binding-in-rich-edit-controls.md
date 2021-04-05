---
title: Come usare l'associazione di tipi di carattere nei controlli Rich Edit
description: Microsoft Rich Edit 3,0 assegna un set di caratteri a caratteri testo normale a seconda del contesto.
ms.assetid: 975B9C33-6766-4FF1-A93E-2169C140CEE9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17c2f8e0e8c1b57611839a5bbf992f9af6bf65
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103872231"
---
# <a name="how-to-use-font-binding-in-rich-edit-controls"></a>Come usare l'associazione di tipi di carattere nei controlli Rich Edit

Microsoft Rich Edit 3,0 assegna un set di caratteri a caratteri testo normale a seconda del contesto. Di seguito sono riportati alcuni esempi:

-   Ai caratteri greci viene assegnato il **\_ set** di caratteri greco.
-   Ai simboli Hangul viene assegnato il **\_ set di caratteri Hangul**.
-   Ai caratteri cinesi viene assegnato il **\_ set** di caratteri ShiftJis se sono presenti caratteri Kana adiacenti o **GB2312 \_ CharSet** se non viene trovato alcun Kana in prossimità.
-   Ai caratteri ANSI non neutri viene assegnato il **\_ set** di caratteri ANSI in qualsiasi evento.

> [!Note]  
> Il controllo Rich Edit usa Unicode internamente, pertanto l'uso di set di caratteri è diverso da quello originale usato nelle specifiche dei tipi di carattere. Tuttavia, la struttura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) dispone di una posizione ben definita per il set di caratteri.

 

Ai caratteri neutri, ad esempio gli spazi vuoti e le cifre viene assegnato un set di caratteri a seconda del contesto. Ad esempio, uno spazio vuoto racchiuso tra caratteri dello stesso set di caratteri ottiene tale set di caratteri. I set di caratteri neutri e cifre usati per il testo bidirezionale sono assegnati a un modo basato sull'algoritmo bidirezionale Unicode.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="use-font-binding-in-a-rich-edit-control"></a>Usare l'associazione di tipi di carattere in un controllo Rich Edit

Dopo aver assegnato i set di caratteri, Rich Edit esegue l'analisi del testo intorno al punto di inserimento avanti e indietro per trovare i tipi di carattere più vicini utilizzati per i set di caratteri. Se non viene trovato alcun carattere per un set di caratteri, Rich Edit usa il tipo di carattere scelto dal client per tale set di caratteri. Se il client non ha specificato un tipo di carattere per il set di caratteri, Rich Edit usa il tipo di carattere predefinito per tale set di caratteri. Se il client vuole un altro tipo di carattere, il client può sempre modificarlo, ma questo approccio funzionerà nella maggior parte dei casi. Le opzioni relative al tipo di carattere predefinite correnti sono basate sulla tabella riportata di seguito. Si noti che i tipi di carattere predefiniti sono impostati per processo ed esistono elenchi distinti per l'utilizzo dell'interfaccia utente e per l'utilizzo non dell'interfaccia utente.



| Linguaggio                    | Nome del tipo di carattere dell'interfaccia utente  | Dimensioni del carattere dell'interfaccia utente | nome del tipo di carattere non dell'interfaccia utente | dimensioni del carattere non dell'interfaccia utente |
|-----------------------------|---------------|--------------|------------------|------------------|
| Occidentale, CE, ME, vietnamita | Tahoma        | 8            | Arial            | 10               |
| Giapponese                    | Interfaccia utente gotica MS  | 9            | Gotico MS P      | 10               |
| Coreano                      | Gulim         | 9            | Gulim            | 9                |
| Cinese semplificato          | SimSun        | 9            | SimSun           | 10               |
| Cinese tradizionale         | PMingLiU      | 9            | PMingLiU         | 9                |
| Thai                        | MS Sans Serif | 8            | Tahoma           | 14               |
| Simboli                     | Wingdings     | 8            | Wingdings        | 10               |
| Devanagari                  | Mangal        | 8            | Mangal           | 10               |
| Tamil                       | Lucci         | 8            | Lucci            | 10               |
| Georgiano, armeno          | Arial Unicode | 8            | Arial Unicode    | 10               |



 

Pertanto, nella tabella di associazione dei tipi di carattere predefinita (le voci hanno un set di caratteri, il nome del tipo di carattere e la dimensione), Rich Edit consente \_ al set di caratteri ANSI di trovare la corrispondenza con diversi set di caratteri, mentre il set di caratteri appropriato corrisponde ad altri tipi di carattere su uno a uno. Più precisamente, Rich Edit usa la \_ scelta del set di caratteri ANSI ogni volta che non viene trovata nessun'altra alternativa. Sarà possibile specificare una granularità più fine rispetto a questa. ad esempio, assegnare un set di \_ caratteri arabo specifico per le esecuzioni arabe, un tipo di carattere greco specifico per le esecuzioni greche e così via. Questa granularità più fine verrà utilizzata anche se un tipo di carattere con il timbro del set di caratteri desiderato viene trovato in un punto del documento prima dell'area a cui è associato il tipo di carattere.

Si noti che Rich Edit non gestisce attualmente un glifo mancante in un tipo di carattere che attesta per supportare un set di caratteri, ma è incompleto. Al momento della visualizzazione in uno script complesso, Rich Edit significa che tale glifo non è presente, ma non comporta l'utilizzo di un nuovo tipo di carattere da parte dell'archivio di backup. In genere, il collegamento del tipo di carattere sottostante del sistema operativo lo condurrà.

## <a name="remarks"></a>Commenti

**Modifica dettagliata 4,1:** Per impostare il tipo di carattere predefinito per uno script, chiamare [**em \_ SETCHARFORMAT**](em-setcharformat.md) con [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a), specificando i valori per i membri **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **LCID** . Inoltre, per ottenere il tipo di carattere predefinito per una tabella codici specifica, chiamare [**em \_ GETCHARFORMAT**](em-getcharformat.md) con **CHARFORMAT2**, specificando i valori per i membri **bCharSet** e **LCID** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 





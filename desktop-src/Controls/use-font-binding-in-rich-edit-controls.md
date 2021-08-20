---
title: Come usare il binding dei tipi di carattere nei controlli Rich Edit
description: Microsoft Rich Edit 3.0 assegna un set di caratteri a caratteri di testo normale a seconda del contesto.
ms.assetid: 975B9C33-6766-4FF1-A93E-2169C140CEE9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3086f9f74469bc535700f28b6eeb45c204024beb34c21663139fd3d63746d4ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829025"
---
# <a name="how-to-use-font-binding-in-rich-edit-controls"></a>Come usare il binding dei tipi di carattere nei controlli Rich Edit

Microsoft Rich Edit 3.0 assegna un set di caratteri a caratteri di testo normale a seconda del contesto. Di seguito sono riportati alcuni esempi:

-   Ai caratteri greci viene **assegnato GRECO \_ CHARSET**.
-   Ai simboli hangul viene assegnato **HANGUL \_ CHARSET.**
-   Ai caratteri cinesi viene **assegnato SHIFTJIS \_ CHARSET se** vengono trovati caratteri Kana nelle vicinanze oppure **GB2312 \_ CHARSET** se non vengono trovati caratteri Kana nelle vicinanze.
-   Ai caratteri ANSI non neutri viene assegnato **UNSI \_ CHARSET** in qualsiasi evento.

> [!Note]  
> Il controllo Rich Edit usa Unicode internamente, quindi questo uso dei set di caratteri è diverso da quello originale usato nelle specifiche dei tipi di carattere. Tuttavia, [**la struttura CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) ha una posizione ben definita per il set di caratteri.

 

Ai caratteri neutri come spazi vuoti e cifre viene assegnato un set di caratteri a seconda del contesto. Ad esempio, uno spazio vuoto racchiuso tra caratteri dello stesso set di caratteri ottiene tale set di caratteri. Ai valori neutri e alle cifre utilizzati per il testo bidirezionale vengono assegnati set di caratteri in modo basato sull'algoritmo bidirezionale Unicode.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="use-font-binding-in-a-rich-edit-control"></a>Usare l'associazione di tipi di carattere in un controllo Rich Edit

Dopo l'assegnazione dei set di caratteri, Rich Edit analizza il testo intorno al punto di inserimento in avanti e indietro per trovare i tipi di carattere più vicini usati per i set di caratteri. Se non viene trovato alcun tipo di carattere per un set di caratteri, Rich Edit usa il tipo di carattere scelto dal client per tale set di caratteri. Se il client non ha specificato un tipo di carattere per il set di caratteri, Rich Edit usa il tipo di carattere predefinito per tale set di caratteri. Se il client desidera un altro tipo di carattere, il client può sempre modificarlo, ma questo approccio funzionerà nella maggior parte dei casi. Le opzioni correnti per i tipi di carattere predefiniti si basano sulla tabella seguente. Si noti che i tipi di carattere predefiniti sono impostati per processo e sono disponibili elenchi separati per l'utilizzo dell'interfaccia utente e per l'utilizzo non dell'interfaccia utente.



| Linguaggio                    | Nome del tipo di carattere dell'interfaccia utente  | Dimensioni del carattere dell'interfaccia utente | nome del tipo di carattere non dell'interfaccia utente | dimensioni del carattere non dell'interfaccia utente |
|-----------------------------|---------------|--------------|------------------|------------------|
| Occidentale, Ce, Me, Taiwanese | Tahoma        | 8            | Arial            | 10               |
| Giapponese                    | Ms UI 2016  | 9            | MS P Insod      | 10               |
| Coreano                      | Gulim         | 9            | Gulim            | 9                |
| Cinese semplificato          | Simsun        | 9            | SimSun           | 10               |
| Cinese tradizionale         | PMingLiU      | 9            | PMingLiU         | 9                |
| Thai                        | MS Sans Serif | 8            | Tahoma           | 14               |
| Simboli                     | Wingdings     | 8            | Wingdings        | 10               |
| Devanagari                  | Mangal        | 8            | Mangal           | 10               |
| Tamil                       | Lucian         | 8            | Lucian            | 10               |
| Serbo, Armeno          | Arial Unicode | 8            | Arial Unicode    | 10               |



 

Pertanto, nella tabella di associazione dei tipi di carattere predefinita (le voci hanno un set di caratteri, un nome e una dimensione), Rich Edit consente a ANSI CHARSET di corrispondere a diversi set di caratteri, mentre il set di caratteri appropriato corrisponde ad altri tipi di carattere \_ uno-a-uno. Più precisamente, rich edit usa la scelta ANSI \_ CHARSET ogni volta che non vengono trovate altre alternative. Sarà possibile specificare una granularità più fine rispetto a questa. ad esempio assegnare un charSET arabo specifico per le esecuzioni arabe, un tipo di carattere greco specifico per le esecuzioni \_ greche e così via. Questa granularità più fine verrà usata anche se un tipo di carattere con lo stamp del set di caratteri desiderato si trova in un punto del documento prima dell'area associata al tipo di carattere.

Si noti che Rich Edit attualmente non gestisce un glifo mancante in un tipo di carattere che dichiara di supportare un set di caratteri, ma è incompleto. In fase di visualizzazione in uno script complesso, Rich Edit non è in grado di sapere che tale glifo è mancante, ma non fa sì che l'archivio di backup usi un nuovo tipo di carattere. In genere, il collegamento del tipo di carattere sottostante del sistema operativo consente di eseguire questa operazione.

## <a name="remarks"></a>Commenti

**Rich Edit 4.1:** Per impostare il tipo di carattere predefinito per uno script, chiamare [**EM \_ SETCHARFORMAT**](em-setcharformat.md) con [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a), specificando i valori per i membri **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **lcid.** Inoltre, per ottenere il tipo di carattere predefinito per una tabella codici specifica, chiamare [**EM \_ GETCHARFORMAT**](em-getcharformat.md) con **CHARFORMAT2,** specificando i valori per **i membri bCharSet** e **lcid.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 





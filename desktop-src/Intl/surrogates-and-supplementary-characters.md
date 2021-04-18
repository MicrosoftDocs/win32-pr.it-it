---
description: Surrogati e caratteri supplementari
ms.assetid: 0dea39e2-a2b4-47fc-b44a-56af8ba1e346
title: Surrogati e caratteri supplementari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8d6b738955c8b8de4f6cb0ae43c78f86752a928
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306602"
---
# <a name="surrogates-and-supplementary-characters"></a>Surrogati e caratteri supplementari

Le applicazioni Windows usano in genere UTF-16 per rappresentare i dati di tipo carattere [Unicode](unicode.md) . L'uso di 16 bit consente la rappresentazione diretta di 65.536 caratteri univoci, ma questo piano multilingue di base (BMP) non è abbastanza sufficiente per coprire tutti i simboli usati nelle lingue umane. La versione Unicode 4,1 include oltre 97.000 caratteri, con oltre 70.000 caratteri solo per il cinese.

Lo standard Unicode ha stabilito 16 "piani" aggiuntivi di caratteri, ognuno con le stesse dimensioni del BMP. Naturalmente, la maggior parte dei punti di codice oltre al BMP non dispone ancora di caratteri assegnati, ma la definizione dei piani fornisce a Unicode la possibilità di definire 1.114.112 caratteri (ovvero, 2 ¹ ⁶ \* 17 caratteri) nell'intervallo di punti di codice compreso tra u + 0000 e u + 10FFFF. Per UTF-16 per rappresentare questo set di caratteri più ampio, lo standard Unicode definisce "caratteri supplementari".

## <a name="about-supplementary-characters"></a>Informazioni sui caratteri supplementari

Un carattere supplementare è un carattere che si trova oltre il BMP e un "surrogato" è un valore di codice UTF-16. Per UTF-16, è necessaria una "coppia di surrogati" per rappresentare un singolo carattere supplementare. Il primo surrogato (alto) è un valore di codice a 16 bit compreso nell'intervallo tra U + D800 e U + DBFF. Il secondo surrogato (basso) è un valore di codice a 16 bit compreso nell'intervallo tra U + DC00 e U + DFFF. Utilizzando il meccanismo surrogato, UTF-16 può supportare tutti 1.114.112 caratteri Unicode potenziali. Per ulteriori informazioni sui caratteri supplementari, sui surrogati e sulle coppie di surrogati, vedere [lo standard Unicode](https://www.unicode.org/standard/standard.html).

> [!Note]  
> Windows 2000 introduce il supporto per l'input di base, l'output e l'ordinamento semplice dei caratteri supplementari. Tuttavia, non tutti i componenti di sistema sono compatibili con caratteri supplementari.

 

Il sistema operativo supporta caratteri supplementari nei modi seguenti:

-   Il formato 12 della tabella CMAP del tipo di carattere OpenType supporta direttamente il codice carattere a 4 byte. Per ulteriori informazioni, vedere la [specifica del tipo di carattere OpenType](/typography/opentype/spec/).
-   Windows supporta [IME (Input Method Editor)](../dxtecharts/installing-and-using-input-method-editors.md)abilitati per surrogati.
-   L'API [Windows GDI](../gdi/windows-gdi.md) supporta il formato 12 tabelle cmap nei tipi di carattere, in modo che i surrogati possano essere visualizzati correttamente.
-   L'API [Uniscribe](uniscribe.md) supporta caratteri supplementari.
-   I [controlli Windows](../controls/window-controls.md), tra cui [modifica](../controls/edit-controls.md) e [Rich Edit](../controls/rich-edit-controls.md), supportano i caratteri supplementari.
-   Il motore HTML supporta le pagine HTML che includono caratteri supplementari per la visualizzazione, la modifica (tramite Outlook Express) e l'invio di form.
-   La tabella di ordinamento del sistema operativo supporta caratteri supplementari.

## <a name="general-guidelines-for-software-development-using-supplementary-characters"></a>Linee guida generali per lo sviluppo di software con caratteri supplementari

UTF-16 gestisce i caratteri supplementari come coppie di surrogati. Il sistema operativo elabora una coppia di surrogati in modo analogo al modo in cui elabora i [Contrassegni senza spaziatura](using-nonspacing-characters-and-diacritics.md). Al momento della visualizzazione, la coppia di surrogati viene visualizzata come un glifo per mezzo di Uniscribe, come previsto dallo standard Unicode.

In Windows Vista sono state introdotte tre nuove macro che consentono di identificare i surrogati e le coppie di surrogati nelle stringhe UTF-16. Si tratta di un surrogato [**\_ alto \_**](/windows/win32/api/Winnls/nf-winnls-is_high_surrogate), [**è un \_ \_ surrogato basso**](/windows/win32/api/Winnls/nf-winnls-is_low_surrogate)ed [**è una \_ \_ coppia di surrogati**](/windows/win32/api/Winnls/nf-winnls-is_surrogate_pair).

Le applicazioni supportano automaticamente i caratteri supplementari se supportano Unicode e utilizzano i controlli di sistema e le funzioni API standard, ad esempio [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) e [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Quindi, se l'applicazione usa controlli di sistema standard o usa chiamate di tipo [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)generali per la visualizzazione, i caratteri supplementari dovrebbero funzionare senza alcuna codifica speciale.

Le applicazioni che implementano il proprio supporto di modifica elaborando le posizioni dei glifi in modo personalizzato possono usare Uniscribe per tutta l'elaborazione del testo. Uniscribe dispone di funzioni separate per gestire l'elaborazione di script complessi, ad esempio la visualizzazione di testo, l'hit test e lo spostamento del cursore. Per ottenere queste funzionalità avanzate, un'applicazione deve chiamare le funzioni Uniscribe in modo specifico. Si noti che le applicazioni che usano le funzioni Uniscribe sono completamente multilingue, ma ciò impone una riduzione delle prestazioni. Pertanto, alcune applicazioni devono eseguire la propria elaborazione dei caratteri supplementari.

Poiché il meccanismo surrogato per rappresentare caratteri supplementari è ben definito, l'applicazione può includere il codice per gestire l'elaborazione del testo surrogato UTF-16. Quando l'applicazione rileva un valore UTF-16 separato dall'intervallo di surrogati riservato inferiore (un surrogato basso) o dall'intervallo di surrogati riservato superiore (un surrogato alto), il valore deve essere una metà di una coppia di surrogati. In questo modo, l'applicazione può rilevare una coppia di surrogati eseguendo semplici verifiche degli intervalli. Se viene rilevato un valore UTF-16 nell'intervallo inferiore o superiore, è necessario tenere traccia della larghezza precedente o diretta di 1 16 bit per ottenere il resto del carattere. Quando si scrive l'applicazione, tenere presente che [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta) e [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva) si spostano da punti di codice a 16 bit, non da coppie di surrogati.

> [!Note]  
> I punti di codice surrogati autonomi hanno un surrogato alto senza un surrogato basso adiacente o viceversa. Questi punti di codice non sono validi e non sono supportati. Il loro comportamento non è definito.

 

Se si sviluppa un tipo di carattere o un provider IME, si noti che i sistemi operativi precedenti a Windows XP disabilitano il supporto dei caratteri supplementari per impostazione predefinita. Per impostazione predefinita, in Windows XP e versioni successive sono abilitati caratteri supplementari. Se si specifica un tipo di carattere e un pacchetto IME per i quali sono richiesti caratteri supplementari, l'applicazione deve impostare i seguenti valori del registro di sistema:


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\LanguagePack]
SURROGATE=(REG_DWORD)0x00000002

[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\International\Scripts\42]
IEFixedFontName=[Surrogate Font Face Name]
IEPropFontName=[Surrogate Font Face Name]
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Character Sets](character-sets.md)
</dt> </dl>

 

 

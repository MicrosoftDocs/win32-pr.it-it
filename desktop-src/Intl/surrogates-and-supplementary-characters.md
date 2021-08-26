---
description: Surrogati e caratteri supplementari
ms.assetid: 0dea39e2-a2b4-47fc-b44a-56af8ba1e346
title: Surrogati e caratteri supplementari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b1dc4743627297962c7279449c06cc1ff967ac35f931a6e945b4577c937b59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130051"
---
# <a name="surrogates-and-supplementary-characters"></a>Surrogati e caratteri supplementari

Windows applicazioni usano in genere UTF-16 per rappresentare dati di tipo carattere [Unicode.](unicode.md) L'uso di 16 bit consente la rappresentazione diretta di 65.536 caratteri univoci, ma questo piano BMP (Basic Multilingual Plane) non è quasi sufficiente per coprire tutti i simboli usati nelle lingue umane. La versione Unicode 4.1 include più di 97.000 caratteri, con oltre 70.000 caratteri solo per il cinese.

Lo standard Unicode ha stabilito 16 "piani" aggiuntivi di caratteri, ognuno delle stesse dimensioni del BMP. Naturalmente, la maggior parte dei punti di codice oltre il BMP non ha ancora caratteri assegnati, ma la definizione dei piani offre a Unicode la possibilità di definire da 1.114.112 caratteri (ovvero 2⁶ 17 caratteri) nell'intervallo di punti di codice \* da U+0000 a U+10FFFF. Per fare in modo che UTF-16 rappresenti questo set di caratteri più ampio, lo standard Unicode definisce "caratteri supplementari".

## <a name="about-supplementary-characters"></a>Informazioni sui caratteri supplementari

Un carattere supplementare è un carattere che si trova oltre BMP e un "surrogato" è un valore di codice UTF-16. Per UTF-16, è necessaria una "coppia di surrogati" per rappresentare un singolo carattere supplementare. Il primo surrogato (alto) è un valore di codice a 16 bit compreso nell'intervallo da U+D800 a U+DBFF. Il secondo surrogato (basso) è un valore di codice a 16 bit compreso nell'intervallo da U+DC00 a U+DFFF. Usando il meccanismo surrogato, UTF-16 può supportare tutti i 1.114.112 potenziali caratteri Unicode. Per altre informazioni sui caratteri supplementari, i surrogati e le coppie di surrogati, vedere [Lo standard Unicode.](https://www.unicode.org/standard/standard.html)

> [!Note]  
> Windows 2000 introduce il supporto per l'input di base, l'output e l'ordinamento semplice dei caratteri supplementari. Tuttavia, non tutti i componenti di sistema sono compatibili con i caratteri supplementari.

 

Il sistema operativo supporta i caratteri supplementari nei modi seguenti:

-   Il formato 12 della tabella cmap del tipo di carattere OpenType supporta direttamente il codice carattere a 4 byte. Per altre informazioni, vedere la specifica del [tipo di carattere OpenType.](/typography/opentype/spec/)
-   Windows supporta gli [IME (Input Method Editor) abilitati](../dxtecharts/installing-and-using-input-method-editors.md)per i surrogati.
-   [L Windows API GDI](../gdi/windows-gdi.md) supporta il formato di 12 tabelle cmap nei tipi di carattere in modo che i surrogati possano essere visualizzati correttamente.
-   [L'API Uniscribe](uniscribe.md) supporta i caratteri supplementari.
-   [Windows controlli](../controls/window-controls.md), inclusi [Edit](../controls/edit-controls.md) e [Rich Edit,](../controls/rich-edit-controls.md)supportano i caratteri supplementari.
-   Il motore HTML supporta pagine HTML che includono caratteri supplementari per la visualizzazione, la modifica (tramite Outlook Express) e l'invio di moduli.
-   La tabella di ordinamento del sistema operativo supporta i caratteri supplementari.

## <a name="general-guidelines-for-software-development-using-supplementary-characters"></a>Linee guida generali per lo sviluppo di software con caratteri supplementari

UTF-16 gestisce i caratteri supplementari come coppie di surrogati. Il sistema operativo elabora una coppia di surrogati in modo analogo al modo in cui elabora [i segni di nonspatura](using-nonspacing-characters-and-diacritics.md). In fase di visualizzazione, la coppia di surrogati viene visualizzata come un glifo tramite Uniscribe, come prescritto dallo standard Unicode.

Windows Vista introduce tre nuove macro per facilitare l'identificazione di surrogati e coppie di surrogati nelle stringhe UTF-16. Si tratta [**di IS \_ HIGH \_ SURROGATE,**](/windows/win32/api/Winnls/nf-winnls-is_high_surrogate) [**IS LOW \_ \_ SURROGATE**](/windows/win32/api/Winnls/nf-winnls-is_low_surrogate)e [**IS \_ SURROGATE \_ PAIR**](/windows/win32/api/Winnls/nf-winnls-is_surrogate_pair).

Le applicazioni supportano automaticamente i caratteri supplementari se supportano Unicode e usano controlli di sistema e funzioni API standard, ad esempio [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) [**e DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Pertanto, se l'applicazione usa controlli di sistema standard o chiamate generali di tipo [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)per la visualizzazione, i caratteri supplementari dovrebbero funzionare senza scrivere codice speciale.

Le applicazioni che implementano il proprio supporto di modifica elaborando le posizioni dei glifi in modo personalizzato possono usare Uniscribe per l'elaborazione del testo. Uniscribe include funzioni separate per gestire l'elaborazione di script complessi, ad esempio la visualizzazione del testo, l'hit testing e lo spostamento del cursore. Un'applicazione deve chiamare le funzioni Uniscribe in modo specifico per ottenere queste funzionalità avanzate. Si noti che le applicazioni che usano le funzioni Uniscribe sono completamente multilingue, ma ciò comporta una penalizzazione delle prestazioni. Alcune applicazioni devono quindi eseguire la propria elaborazione dei caratteri supplementari.

Poiché il meccanismo di surrogati per rappresentare i caratteri supplementari è ben definito, l'applicazione può includere codice per gestire l'elaborazione del testo surrogato UTF-16. Quando l'applicazione rileva un valore UTF-16 separato dall'intervallo di surrogati riservati inferiore (un surrogato basso) o dall'intervallo di surrogati riservati superiore (surrogato alto), il valore deve essere metà di una coppia di surrogati. Di conseguenza, l'applicazione può rilevare una coppia di surrogati eseguendo un semplice controllo dell'intervallo. Se rileva un valore UTF-16 nell'intervallo inferiore o superiore, deve tenere traccia di una larghezza di 16 bit indietro o avanti per ottenere il resto del carattere. Quando si scrive l'applicazione, tenere presente che [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta) e [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva) si spostano di punti di codice a 16 bit, non da coppie di surrogati.

> [!Note]  
> I punti di codice surrogati autonomi hanno un surrogato alto senza un surrogato basso adiacente o viceversa. Questi punti di codice non sono validi e non sono supportati. Il loro comportamento non è definito.

 

Se si sviluppa un tipo di carattere o un provider IME, si noti che i sistemi operativi Windows XP disabilitano il supporto dei caratteri supplementari per impostazione predefinita. Windows XP e versioni successive abilitano i caratteri supplementari per impostazione predefinita. Se si specifica un tipo di carattere e un pacchetto IME che richiedono caratteri supplementari, l'applicazione deve impostare i valori del Registro di sistema seguenti:


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

 

 

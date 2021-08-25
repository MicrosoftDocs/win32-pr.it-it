---
title: Input da tastiera (Informazioni di base con Win32 e C++)
description: Input da tastiera
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3ed8ac1e8d7cd8e6ea35c9e9f58c10fd516cca010b5e5dce667817b32028c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822351"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a>Input da tastiera (Informazioni di base con Win32 e C++)

La tastiera viene usata per diversi tipi distinti di input, tra cui:

-   Input di caratteri. Testo che l'utente digitare in un documento o in una casella di modifica.
-   Tasti di scelta rapida. Tratti di tasto che richiamano le funzioni dell'applicazione; ad esempio CTRL+O per aprire un file.
-   Comandi di sistema. Tratti di tasto che richiamano funzioni di sistema; ad esempio ALT+TAB per passare da una finestra all'altro.

Quando si pensa all'input da tastiera, è importante ricordare che un tratto del tasto non è uguale a un carattere. Ad esempio, la pressione del tasto A può comportare uno dei caratteri seguenti.

-   a
-   A
-   à (se la tastiera supporta la combinazione di segni diacritici)

Inoltre, se il tasto ALT viene premuto, la pressione del tasto A produce ALT+A, che il sistema non considera affatto come un carattere, ma come un comando di sistema.

## <a name="key-codes"></a>Codici chiave

Quando si preme un tasto, l'hardware genera un *codice di analisi*. I codici di digitalizzazione variano da una tastiera all'altra e sono disponibili codici di analisi separati per gli eventi di tasti up e key-down. I codici di analisi non saranno quasi mai di attenzione. Il driver della tastiera converte i codici di analisi in *codici di tasti virtuali*. I codici di chiave virtuale sono indipendenti dal dispositivo. Premendo il tasto A su qualsiasi tastiera viene generato lo stesso codice del tasto virtuale.

In generale, i codici di chiave virtuale non corrispondono a codici ASCII o a qualsiasi altro standard di codifica dei caratteri. Questo è ovvio se ci si pensa, perché la stessa chiave può generare caratteri diversi (a, A, à) e alcune chiavi, ad esempio i tasti funzione, non corrispondono ad alcun carattere.

Ciò detto, i codici di chiave virtuale seguenti esegono il mapping agli equivalenti ASCII:

-   Da 0 a 9 chiavi = ASCII "0" – "9" (0x30 – 0x39)
-   Tasti da A a Z = ASCII "A" – "Z" (0x41 – 0x5A)

Per alcuni aspetti, questo mapping è molto importante, perché non è consigliabile pensare ai codici di chiave virtuale come a caratteri, per i motivi illustrati.

Il file di intestazione WinUser.h definisce le costanti per la maggior parte dei codici di chiave virtuale. Ad esempio, il codice del tasto virtuale per il tasto FRECCIA SINISTRA è **VK \_ LEFT** (0x25). Per l'elenco completo dei codici di chiave virtuale, vedere [**Codici di chiave virtuale.**](/windows/desktop/inputdev/virtual-key-codes) Non sono definite costanti per i codici di chiave virtuale che corrispondono a valori ASCII. Ad esempio, il codice della chiave virtuale per la chiave A è 0x41, ma non esiste alcuna costante **denominata VK \_ A**. Usare invece solo il valore numerico.

## <a name="key-down-and-key-up-messages"></a>Key-Down e Key-Up messaggi

Quando si preme un tasto, la finestra con lo stato attivo riceve uno dei messaggi seguenti.

-   [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)
-   [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)

Il [**messaggio \_ WM SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) indica un tasto *di* sistema , ovvero un tratto di tasto che richiama un comando di sistema. Esistono due tipi di chiave di sistema:

-   ALT + qualsiasi tasto
-   F10

Il tasto F10 attiva la barra dei menu di una finestra. Varie combinazioni di tasti ALT richiamano i comandi di sistema. Ad esempio, ALT+TAB passa a una nuova finestra. Inoltre, se in una finestra è presente un menu, è possibile usare alt per attivare le voci di menu. Alcune combinazioni di tasti ALT non e fanno nulla.

Tutti gli altri tratti di tasto sono considerati tasti non di sistema e producono il [**messaggio \_ WM KEYDOWN.**](/windows/desktop/inputdev/wm-keydown) Sono inclusi i tasti funzione diversi da F10.

Quando si rilascia una chiave, il sistema invia un messaggio di key-up corrispondente:

-   [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)
-   [**WM \_ SYSKEYUP**](/windows/desktop/inputdev/wm-syskeyup)

Se si tiene premuto un tasto per un tempo sufficiente per avviare la funzionalità di ripetizione della tastiera, il sistema invia più messaggi di tasti giù, seguiti da un singolo messaggio di tasti up.

In tutti e quattro i messaggi della tastiera illustrati finora, il *parametro wParam* contiene il codice del tasto virtuale del tasto. Il *parametro lParam* contiene alcune informazioni varie, suddivise in 32 bit. In genere non sono necessarie le informazioni in *lParam*. Un flag che potrebbe essere utile è il bit 30, il flag "stato chiave precedente", che è impostato su 1 per i messaggi di tasti di scelta ripetuti.

Come suggerisce il nome, i tratti dei tasti di sistema sono destinati principalmente all'uso da parte del sistema operativo. Se si intercetta il [**messaggio \_ WM SYSKEYDOWN,**](/windows/desktop/inputdev/wm-syskeydown) chiamare [**DefWindowProc in un secondo**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) momento. In caso contrario, il sistema operativo non gestirà il comando.

## <a name="character-messages"></a>Messaggi di tipo carattere

I tratti chiave vengono convertiti in caratteri dalla [**funzione TranslateMessage,**](/windows/desktop/api/winuser/nf-winuser-translatemessage) che è stata vista per la prima volta nel [modulo 1.](your-first-windows-program.md) Questa funzione esamina i messaggi key-down e li converte in caratteri. Per ogni carattere prodotto, la funzione **TranslateMessage** inserisce un messaggio [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) o [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) nella coda di messaggi della finestra. Il *parametro wParam* del messaggio contiene il carattere UTF-16.

Come si può immaginare, i [**messaggi WM \_ CHAR**](/windows/desktop/inputdev/wm-char) vengono generati dai messaggi [**WM \_ KEYDOWN,**](/windows/desktop/inputdev/wm-keydown) mentre i messaggi [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) vengono generati dai [**messaggi WM \_ SYSKEYDOWN.**](/windows/desktop/inputdev/wm-syskeydown) Si supponga, ad esempio, che l'utente premo il tasto MAIUSC seguito dal tasto A. Supponendo un layout di tastiera standard, si otterrà la sequenza di messaggi seguente:

**WM \_ KEYDOWN:** MAIUSC  
**WM \_ KEYDOWN:** A  
**WM \_ CHAR:**'A'  


D'altra parte, la combinazione ALT + P genera:

 **WM \_ SYSKEYDOWN:** MENU VK \_  
**WM \_ SYSKEYDOWN:** 0x50  
**WM \_ SYSCHAR:**'p'  
**WM \_ SYSKEYUP:** 0x50  
**WM \_ KEYUP:** MENU VK \_  


Il codice del tasto virtuale per il tasto ALT è denominato VK \_ MENU per motivi cronologici.

Il [**messaggio \_ SYSCHAR WM**](/windows/desktop/menurc/wm-syschar) indica un carattere di sistema. Come per [**WM \_ SYSKEYDOWN,**](/windows/desktop/inputdev/wm-syskeydown)in genere questo messaggio deve essere passato direttamente [**a DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) In caso contrario, è possibile interferire con i comandi di sistema standard. In particolare, non considerare **WM \_ SYSCHAR** come testo digitato dall'utente.

Il [**messaggio WM \_ CHAR**](/windows/desktop/inputdev/wm-char) è ciò che normalmente si pensa come input di caratteri. Il tipo di dati per il carattere **è wchar \_ t**, che rappresenta un carattere Unicode UTF-16. L'input di caratteri può includere caratteri non inclusi nell'intervallo ASCII, in particolare con layout di tastiera comunemente usati al di fuori del Stati Uniti. È possibile provare diversi layout di tastiera installando una tastiera regionale e quindi usando la funzionalità Tastiera su schermo.

Gli utenti possono anche installare un Input Method Editor (IME) per immettere script complessi, ad esempio caratteri giapponesi, con una tastiera standard. Ad esempio, se si usa un IME giapponese per immettere il carattere katakana カ (ka), è possibile che venga visualizzato il messaggio seguente:

**WM \_ KEYDOWN:** VK \_ PROCESSKEY (chiave IME PROCESS)  
**WM \_ KEYUP:** 0x4B  
**WM \_ KEYDOWN:** VK \_ PROCESSKEY  
**WM \_ KEYUP:** 0x41  
**WM \_ KEYDOWN:** VK \_ PROCESSKEY  
**WM \_ CHAR**: カ  
**WM \_ KEYUP:** VK \_ RETURN  


Alcune combinazioni di tasti CTRL vengono convertite in caratteri di controllo ASCII. Ad esempio, CTRL+A viene convertito nel carattere ASCII CTRL-A (SOH) (valore ASCII 0x01). Per l'input di testo, è in genere consigliabile filtrare i caratteri di controllo. Evitare inoltre di usare [**WM \_ CHAR per implementare**](/windows/desktop/inputdev/wm-char) i tasti di scelta rapida. Usare invece i [**messaggi WM \_ KEYDOWN.**](/windows/desktop/inputdev/wm-keydown) O meglio, usare una tabella dei tasti di scelta rapida. Le tabelle dei tasti di scelta rapida sono descritte nell'argomento successivo, [Tabelle dei tasti di scelta rapida](accelerator-tables.md).

Il codice seguente visualizza i messaggi principali della tastiera nel debugger. Provare a riprodurre con combinazioni di tasti diverse e vedere quali messaggi vengono generati.


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    wchar_t msg[32];
    switch (uMsg)
    {
    case WM_SYSKEYDOWN:
        swprintf_s(msg, L"WM_SYSKEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSCHAR:
        swprintf_s(msg, L"WM_SYSCHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSKEYUP:
        swprintf_s(msg, L"WM_SYSKEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYDOWN:
        swprintf_s(msg, L"WM_KEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYUP:
        swprintf_s(msg, L"WM_KEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_CHAR:
        swprintf_s(msg, L"WM_CHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    /* Handle other messages (not shown) */

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



## <a name="miscellaneous-keyboard-messages"></a>Messaggi vari della tastiera

Alcuni altri messaggi della tastiera possono essere ignorati dalla maggior parte delle applicazioni.

-   Il [**messaggio \_ DEADCHAR WM**](/windows/desktop/inputdev/wm-deadchar) viene inviato per una chiave di combinazione, ad esempio un diacritico. Ad esempio, in una tastiera in lingua spagnola, digitando l'accento (') seguito da E viene generato il carattere e. Wm **\_ DEADCHAR viene inviato** per il carattere accentato.
-   Il [**messaggio WM \_ UNICHAR**](/windows/desktop/inputdev/wm-unichar) è obsoleto. Consente ai programmi ANSI di ricevere l'input di caratteri Unicode.
-   Il [**carattere WM \_ IME \_ CHAR**](/windows/desktop/Intl/wm-ime-char) viene inviato quando un IME converte una sequenza di sequenze di tasti in caratteri. Viene inviato in aggiunta al normale [**messaggio WM \_ CHAR.**](/windows/desktop/inputdev/wm-char)

## <a name="keyboard-state"></a>Stato della tastiera

I messaggi della tastiera sono guidati da eventi. In altri casi, viene visualizzato un messaggio quando si verifica qualcosa di interessante, ad esempio una pressione di un tasto, e il messaggio indica cosa è appena successo. È tuttavia possibile testare lo stato di una chiave in qualsiasi momento chiamando la [**funzione GetKeyState.**](/windows/desktop/api/winuser/nf-winuser-getkeystate)

Si consideri, ad esempio, come si rileverebbe la combinazione di clic sinistro del mouse + tasto ALT. È possibile tenere traccia dello stato del tasto ALT in ascolto dei messaggi di key stroke e archiviare un flag, ma [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) consente di risparmiare il problema. Quando si riceve il [**messaggio WM \_ LBUTTONDOWN,**](/windows/desktop/inputdev/wm-lbuttondown) è sufficiente chiamare **GetKeyState** come segue:


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



Il [**messaggio GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) accetta un codice di chiave virtuale come input e restituisce un set di flag di bit (in realtà solo due flag). Il valore 0x8000 il flag di bit che verifica se il tasto è attualmente premuto.

La maggior parte delle tastiere ha due tasti ALT, sinistra e destra. Nell'esempio precedente viene verificata la pressione di uno di essi. È anche possibile usare [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) per distinguere tra le istanze sinistra e destra dei tasti ALT, MAIUSC o CTRL. Ad esempio, il codice seguente verifica se viene premuto il tasto ALT di destra.


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



La [**funzione GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) è interessante perché segnala uno stato *della tastiera* virtuale. Questo stato virtuale si basa sul contenuto della coda di messaggi e viene aggiornato quando si rimuovono messaggi dalla coda. Quando il programma elabora i messaggi della finestra, **GetKeyState** fornisce uno snapshot della tastiera nel momento in cui ogni messaggio è stato accodato. Ad esempio, se l'ultimo messaggio nella coda è [**WM \_ LBUTTONDOWN,**](/windows/desktop/inputdev/wm-lbuttondown) **GetKeyState** segnala lo stato della tastiera nel momento in cui l'utente ha fatto clic sul pulsante del mouse.

Poiché [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) è basato sulla coda di messaggi, ignora anche l'input da tastiera inviato a un altro programma. Se l'utente passa a un altro programma, qualsiasi pressione di tasti inviata a tale programma viene ignorata da **GetKeyState**. Se si vuole conoscere lo stato fisico immediato della tastiera, è disponibile una funzione per questo: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate). Per la maggior parte del codice dell'interfaccia utente, tuttavia, la funzione corretta è **GetKeyState**.

## <a name="next"></a>Prossima

[Tabelle dei tasti di scelta rapida](accelerator-tables.md)

 

 

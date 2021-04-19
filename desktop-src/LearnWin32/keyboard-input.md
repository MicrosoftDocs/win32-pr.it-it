---
title: Input da tastiera (introduzione a Win32 e C++)
description: Input da tastiera
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82065d4024428b48d4d3061da31a5384cab417d2
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "106320255"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a>Input da tastiera (introduzione a Win32 e C++)

La tastiera viene utilizzata per diversi tipi distinti di input, tra cui:

-   Input di caratteri. Testo che l'utente digita in un documento o in una casella di modifica.
-   Tasti di scelta rapida. Tratti chiave che richiamano le funzioni dell'applicazione; ad esempio, CTRL + O per aprire un file.
-   Comandi di sistema. Tratti chiave che richiamano funzioni di sistema; ad esempio, ALT + TAB per passare a Windows.

Quando si pensa all'input da tastiera, è importante ricordare che un tratto di chiave non è uguale a un carattere. Ad esempio, la pressione di un tasto può causare uno dei caratteri seguenti.

-   a
-   A
-   á (se la tastiera supporta la combinazione dei segni diacritici)

Inoltre, se il tasto ALT è premuto, premendo il tasto A viene prodotto ALT + A, che il sistema non considera come un carattere, ma piuttosto come un comando di sistema.

## <a name="key-codes"></a>Codici chiave

Quando si preme un tasto, l'hardware genera un *codice di analisi*. I codici di analisi variano da una tastiera all'altra e sono disponibili codici di analisi distinti per gli eventi di chiave e di discesa. I codici di analisi non vengono mai interessati. Il driver della tastiera converte i codici di analisi in *codici chiave virtuale*. I codici delle chiavi virtuali sono indipendenti dal dispositivo. Premendo il tasto A su qualsiasi tastiera viene generato lo stesso codice di chiave virtuale.

In generale, i codici delle chiavi virtuali non corrispondono a codici ASCII o a qualsiasi altro standard di codifica dei caratteri. Si tratta di un'operazione ovvia, perché la stessa chiave può generare caratteri diversi (a, A, á) e alcune chiavi, ad esempio i tasti funzione, non corrispondono a nessun carattere.

Detto ciò, i codici a chiave virtuale seguenti eseguono il mapping agli equivalenti ASCII:

-   da 0 a 9 chiavi = ASCII ' 0' –' 9' (0x30 – 0x39)
-   Da a a Z chiavi = ASCII ' A '-' Z ' (0x41 – 0x5A)

Per alcuni aspetti, questo mapping è sfortunato, perché i codici di chiave virtuale non devono mai essere considerati come caratteri, per i motivi illustrati.

Il file di intestazione WinUser. h definisce le costanti per la maggior parte dei codici della chiave virtuale. Ad esempio, il codice della chiave virtuale per il tasto freccia sinistra è **VK \_ Left** (0x25). Per l'elenco completo dei codici delle chiavi virtuali, vedere [**codici chiave virtuale**](/windows/desktop/inputdev/virtual-key-codes). Non sono definite costanti per i codici chiave virtuale che corrispondono ai valori ASCII. Il codice della chiave virtuale per la chiave A è ad esempio 0x41, ma non esiste una costante denominata **VK \_ A**. In alternativa, è sufficiente usare il valore numerico.

## <a name="key-down-and-key-up-messages"></a>Messaggi di Key-Down e Key-Up

Quando si preme un tasto, la finestra con lo stato attivo della tastiera riceve uno dei messaggi seguenti.

-   [**\_SYSKEYDOWN WM**](/windows/desktop/inputdev/wm-syskeydown)
-   [**KeyDown di WM \_**](/windows/desktop/inputdev/wm-keydown)

Il messaggio [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) indica una *chiave di sistema*, ovvero un tratto di chiave che richiama un comando di sistema. Esistono due tipi di chiave di sistema:

-   ALT + qualsiasi tasto
-   F10

Il tasto F10 attiva la barra dei menu di una finestra. Diverse combinazioni di tasti ALT richiamano i comandi di sistema. Ad esempio, ALT + TAB passa a una nuova finestra. Inoltre, se una finestra dispone di un menu, è possibile utilizzare il tasto ALT per attivare le voci di menu. Alcune combinazioni di tasti ALT non eseguono alcuna operazione.

Tutti gli altri tratti chiave sono considerati chiavi non di sistema e producono il messaggio del [**\_ KeyDown di WM**](/windows/desktop/inputdev/wm-keydown) . Sono inclusi i tasti funzione diversi da F10.

Quando si rilascia un tasto, il sistema invia un messaggio di chiave corrispondente:

-   [**KEYUP di WM \_**](/windows/desktop/inputdev/wm-keyup)
-   [**\_SYSKEYUP WM**](/windows/desktop/inputdev/wm-syskeyup)

Se si tiene premuto un tasto sufficientemente lungo per avviare la funzionalità di ripetizione della tastiera, il sistema invia più messaggi di chiave, seguiti da un singolo messaggio di chiave.

In tutti e quattro i messaggi della tastiera discussi finora, il parametro *wParam* contiene il codice della chiave virtuale della chiave. Il parametro *lParam* contiene alcune informazioni varie compresse in 32 bit. In genere non sono necessarie le informazioni in *lParam*. Un flag che può essere utile è il bit 30, il flag "stato della chiave precedente", che è impostato su 1 per i messaggi di chiave inattivo ripetuti.

Come suggerisce il nome, i tratti chiave di sistema sono destinati principalmente all'uso da parte del sistema operativo. Se si intercetta il messaggio [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) , chiamare [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) in seguito. In caso contrario, il sistema operativo non riuscirà a gestire il comando.

## <a name="character-messages"></a>Messaggi di tipo carattere

I tratti chiave vengono convertiti in caratteri dalla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) , che è stata esaminata prima nel [modulo 1](your-first-windows-program.md). Questa funzione esamina i messaggi di chiave e li converte in caratteri. Per ogni carattere prodotto, la funzione **TranslateMessage** inserisce un messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) o [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) nella coda di messaggi della finestra. Il parametro *wParam* del messaggio contiene il carattere UTF-16.

Come si può immaginare, i messaggi [**WM \_ char**](/windows/desktop/inputdev/wm-char) vengono generati da messaggi di [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) , mentre i messaggi [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) vengono generati da messaggi [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) . Si supponga, ad esempio, che l'utente prema il tasto MAIUSC seguito da un tasto A. Supponendo un layout di tastiera standard, si otterrebbe la seguente sequenza di messaggi:

**WM \_ KEYDOWN**: MAIUSC  
**WM \_ KEYDOWN**: A  
**WM \_ CHAR**:' A '  


D'altra parte, la combinazione ALT + P genererebbe:

 **WM \_ SYSKEYDOWN**: \_ menu VK  
**WM \_ SYSKEYDOWN**: 0x50  
**WM \_ SYSCHAR**: "p"  
**WM \_ SYSKEYUP**: 0x50  
**WM \_ MENU KEYUP**: VK \_  


Il codice della chiave virtuale per il tasto ALT è denominato VK \_ MENU per motivi cronologici.)

Il messaggio [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) indica un carattere di sistema. Come per [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), in genere è necessario passare questo messaggio direttamente a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). In caso contrario, è possibile interferire con i comandi di sistema standard. In particolare, non considerare **WM \_ SYSCHAR** come testo digitato dall'utente.

Il messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) è quello che si considera normalmente come input di caratteri. Il tipo di dati per il carattere è **WCHAR \_ t**, che rappresenta un carattere Unicode UTF-16. L'input di caratteri può includere caratteri non compresi nell'intervallo ASCII, specialmente con i layout di tastiera utilizzati in genere all'esterno del Stati Uniti. È possibile provare diversi layout di tastiera installando una tastiera a livello di area e quindi usando la funzionalità della tastiera su schermo.

Gli utenti possono anche installare un IME (Input Method Editor) per immettere script complessi, ad esempio caratteri giapponesi, con una tastiera standard. Ad esempio, se si usa un IME giapponese per immettere il carattere katakana カ (KA), è possibile che vengano visualizzati i messaggi seguenti:

**WM \_ KEYDOWN**: VK \_ PROCESSKEY (chiave di processo IME)  
**WM \_ KEYUP**: 0x4B  
**WM \_ KEYDOWN**: VK \_ PROCESSKEY  
**WM \_ KEYUP**: 0x41  
**WM \_ KEYDOWN**: VK \_ PROCESSKEY  
**WM \_ CHAR**: カ  
**WM \_ KEYUP**: \_ risultato VK  


Alcune combinazioni di tasti CTRL vengono convertite in caratteri di controllo ASCII. Ad esempio, CTRL + A viene convertito nel carattere ASCII CTRL-A (SOH) (valore ASCII 0x01). Per l'input di testo, è in genere necessario escludere i caratteri di controllo. Evitare inoltre di usare [**WM \_ char**](/windows/desktop/inputdev/wm-char) per implementare i tasti di scelta rapida. Usare invece i messaggi di [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) oppure, ancora meglio, usare una tabella di tasti di scelta rapida. Le tabelle degli acceleratori sono descritte nell'argomento successivo, [tabelle di tasti di scelta rapida](accelerator-tables.md).

Nel codice seguente vengono visualizzati i messaggi principali della tastiera nel debugger. Provare a giocare con diverse combinazioni di tasti e vedere quali messaggi vengono generati.


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



## <a name="miscellaneous-keyboard-messages"></a>Messaggi della tastiera vari

Alcuni altri messaggi della tastiera possono essere ignorati in modo sicuro dalla maggior parte delle applicazioni.

-   Il messaggio [**WM \_ DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) viene inviato per una chiave di combinazione, ad esempio un diacritici. Ad esempio, in una tastiera in lingua spagnola, digitando accento (') seguito da E viene prodotto il carattere è. Il **\_ DEADCHAR WM** viene inviato per il carattere accentato.
-   Il messaggio di [**WM \_ UNICHAR**](/windows/desktop/inputdev/wm-unichar) è obsoleto. Consente ai programmi ANSI di ricevere input di caratteri Unicode.
-   Il carattere [**WM \_ IME \_ char**](/windows/desktop/Intl/wm-ime-char) viene inviato quando un IME converte una sequenza di tasti in caratteri. Viene inviata oltre al normale messaggio [**WM \_ char**](/windows/desktop/inputdev/wm-char) .

## <a name="keyboard-state"></a>Stato della tastiera

I messaggi della tastiera sono basati sugli eventi. Ovvero, viene visualizzato un messaggio quando si verifica un evento interessante, ad esempio la pressione di un tasto, e il messaggio indica cosa si è appena verificato. Tuttavia, è anche possibile testare lo stato di una chiave in qualsiasi momento, chiamando la funzione [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) .

Si consideri ad esempio il modo in cui si rileva la combinazione di clic con il tasto sinistro del mouse + ALT. È possibile tenere traccia dello stato del tasto ALT ascoltando i messaggi della sequenza di tasti e archiviando un flag, ma [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) Salva il problema. Quando si riceve il messaggio [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) , è sufficiente chiamare **GetKeyState** come indicato di seguito:


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



Il messaggio [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) accetta come input un codice di chiave virtuale e restituisce un set di flag di bit, in realtà solo due flag. Il valore 0x8000 contiene il flag di bit che verifica se la chiave è attualmente premuta.

La maggior parte delle tastiere dispone di due tasti ALT, a sinistra e a destra. Nell'esempio precedente viene verificato se uno di questi elementi è stato premuto. È anche possibile usare [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) per distinguere tra le istanze di sinistra e destra dei tasti ALT, MAIUSC o CTRL. Il codice seguente, ad esempio, verifica se viene premuto il tasto ALT destro.


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



La funzione [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) è interessante perché segnala uno stato della tastiera *virtuale* . Questo stato virtuale si basa sul contenuto della coda di messaggi e viene aggiornato quando si rimuovono i messaggi dalla coda. Quando il programma elabora i messaggi della finestra, **GetKeyState** fornisce uno snapshot della tastiera nel momento in cui ogni messaggio è stato accodato. Se, ad esempio, l'ultimo messaggio della coda è [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** segnala lo stato della tastiera al momento in cui l'utente ha fatto clic sul pulsante del mouse.

Poiché [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) è basato sulla coda di messaggi, ignora anche l'input da tastiera inviato a un altro programma. Se l'utente passa a un altro programma, tutte le pressioni dei tasti inviate al programma vengono ignorate da **GetKeyState**. Se si desidera effettivamente ottenere lo stato fisico immediato della tastiera, è presente una funzione per: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate). Per la maggior parte del codice dell'interfaccia utente, tuttavia, la funzione corretta è **GetKeyState**.

## <a name="next"></a>Prossima

[Tabelle dei tasti di scelta rapida](accelerator-tables.md)

 

 

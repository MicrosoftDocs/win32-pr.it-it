---
title: Tabelle dei tasti di scelta rapida
description: Tabelle dei tasti di scelta rapida
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2951ee99a31a977e0909de5639fa3110cea10e0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090819"
---
# <a name="accelerator-tables"></a>Tabelle dei tasti di scelta rapida

Le applicazioni spesso definiscono tasti di scelta rapida, ad esempio CTRL+O per il comando Apri file. È possibile implementare i tasti di scelta rapida gestendo singoli [**messaggi WM \_ KEYDOWN,**](/windows/desktop/inputdev/wm-keydown) ma le tabelle dei tasti di scelta rapida offrono una soluzione migliore che:

-   Richiede meno codice.
-   Consolida tutti i collegamenti in un unico file di dati.
-   Supporta la localizzazione in altre lingue.
-   Consente ai tasti di scelta rapida e ai comandi di menu di usare la stessa logica dell'applicazione.

Una *tabella dei tasti di* scelta rapida è una risorsa dati che esegue il mapping delle combinazioni di tasti, ad esempio CTRL+O, ai comandi dell'applicazione. Prima di vedere come usare una tabella dei tasti di scelta rapida, è necessaria una rapida introduzione alle risorse. Una *risorsa* è un BLOB di dati incorporato in un file binario dell'applicazione (EXE o DLL). Le risorse archiviano i dati necessari per l'applicazione, ad esempio menu, cursori, icone, immagini, stringhe di testo o dati personalizzati dell'applicazione. L'applicazione carica i dati delle risorse dal file binario in fase di esecuzione. Per includere le risorse in un file binario, eseguire le operazioni seguenti:

1.  Creare un file di definizione di risorsa (RC). Questo file definisce i tipi di risorse e i relativi identificatori. Il file di definizione delle risorse può includere riferimenti ad altri file. Ad esempio, una risorsa icona viene dichiarata nel file RC, ma l'immagine dell'icona viene archiviata in un file separato.
2.  Usare il compilatore di risorse di Microsoft Windows (RC) per compilare il file di definizione della risorsa in un file di risorse compilato (con estensione res). Il compilatore RC viene fornito con Visual Studio e anche il Windows SDK.
3.  Collegare il file di risorse compilato al file binario.

Questi passaggi sono approssimativamente equivalenti al processo di compilazione/collegamento per i file di codice. Visual Studio un set di editor di risorse che semplificano la creazione e la modifica delle risorse. Questi strumenti non sono disponibili nelle edizioni Express di Visual Studio. Ma un file RC è semplicemente un file di testo e la sintassi è documentata in MSDN, quindi è possibile creare un file RC usando qualsiasi editor di testo. Per altre informazioni, vedere [Informazioni sui file di risorse](/windows/desktop/menurc/about-resource-files).

## <a name="defining-an-accelerator-table"></a>Definizione di una tabella dei tasti di scelta rapida

Una tabella dei tasti di scelta rapida è una tabella di tasti di scelta rapida. Ogni collegamento è definito da:

-   Identificatore numerico. Questo numero identifica il comando dell'applicazione che verrà richiamato dal collegamento.
-   Carattere ASCII o codice tasto virtuale del collegamento.
-   Tasti di modifica facoltativi: ALT, MAIUSC o CTRL.

La tabella dei tasti di scelta rapida ha un identificatore numerico che identifica la tabella nell'elenco delle risorse dell'applicazione. Si creerà ora una tabella dei tasti di scelta rapida per un semplice programma di disegno. Questo programma avrà due modalità, la modalità di disegno e la modalità di selezione. In modalità di disegno, l'utente può disegnare forme. In modalità di selezione, l'utente può selezionare le forme. Per questo programma, è necessario definire i tasti di scelta rapida seguenti.



| Tasto di scelta rapida | Comando                   |
|----------|---------------------------|
| CTRL+M   | Passare da una modalità all'altra.     |
| F1       | Passare alla modalità di disegno.      |
| F2       | Passare alla modalità di selezione. |



 

Definire prima di tutto gli identificatori numerici per la tabella e per i comandi dell'applicazione. Questi valori sono arbitrari. È possibile assegnare costanti simboliche per gli identificatori definendoli in un file di intestazione. Ad esempio:


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



In questo esempio il valore identifica `IDR_ACCEL1` la tabella dei tasti di scelta rapida e le tre costanti seguenti definiscono i comandi dell'applicazione. Per convenzione, un file di intestazione che definisce le costanti di risorsa è spesso denominato resource.h. L'elenco successivo mostra il file di definizione della risorsa.


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



I tasti di scelta rapida sono definiti tra parentesi graffe. Ogni collegamento contiene le voci seguenti.

-   Codice del tasto virtuale o carattere ASCII che richiama il tasto di scelta rapida.
-   Comando dell'applicazione. Si noti che nell'esempio vengono usate costanti simboliche. Il file di definizione delle risorse include resource.h, in cui sono definite queste costanti.
-   La parola **chiave VIRTKEY** indica che la prima voce è un codice di chiave virtuale. L'altra opzione è l'uso di caratteri ASCII.
-   Modificatori facoltativi: ALT, CONTROL o MAIUSC.

Se si usano caratteri ASCII per i tasti di scelta rapida, un carattere minuscolo sarà un tasto di scelta rapida diverso da un carattere maiuscolo. Ad esempio, la digitazione di "a" potrebbe richiamare un comando diverso rispetto alla digitazione di "A". Questo potrebbe confondere gli utenti, quindi è in genere consigliabile usare codici di chiave virtuale, anziché caratteri ASCII, per i tasti di scelta rapida.

## <a name="loading-the-accelerator-table"></a>Caricamento della tabella dei tasti di scelta rapida

La risorsa per la tabella dei tasti di scelta rapida deve essere caricata prima che il programma possa usarla. Per caricare una tabella dei tasti di scelta rapida, chiamare la [**funzione LoadAccelerators.**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa)


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



Chiamare questa funzione prima di immettere il ciclo di messaggi. Il primo parametro è l'handle per il modulo. Questo parametro viene passato alla [**funzione WinMain.**](/windows/desktop/api/winbase/nf-winbase-winmain) Per informazioni dettagliate, vedere [WinMain: Il punto di ingresso dell'applicazione.](winmain--the-application-entry-point.md) Il secondo parametro è l'identificatore di risorsa. La funzione restituisce un handle per la risorsa. Si noti che un handle è un tipo opaco che fa riferimento a un oggetto gestito dal sistema. Se la funzione ha esito negativo, restituisce **NULL.**

È possibile rilasciare una tabella dei tasti di scelta rapida [**chiamando DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable). Tuttavia, il sistema rilascia automaticamente la tabella all'uscita del programma, quindi è necessario chiamare questa funzione solo se si sostituisce una tabella con un'altra. È disponibile un esempio interessante di questo argomento nell'argomento [Creazione di acceleratori modificabili dall'utente](/windows/desktop/menurc/using-keyboard-accelerators).

## <a name="translating-key-strokes-into-commands"></a>Traduzione di tratti chiave in comandi

Una tabella dei tasti di scelta rapida funziona traducendo i tratti dei tasti in [**messaggi WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) Il *parametro wParam* di **WM \_ COMMAND** contiene l'identificatore numerico del comando. Ad esempio, usando la tabella illustrata in precedenza, il tasto CTRL+M viene convertito in un **messaggio WM \_ COMMAND** con il valore `ID_TOGGLE_MODE` . A tale scopo, modificare il ciclo di messaggi nel modo seguente:


```C++
    MSG msg;
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(win.Window(), hAccel, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```



Questo codice aggiunge una chiamata alla [**funzione TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) all'interno del ciclo di messaggi. La **funzione TranslateAccelerator** esamina ogni messaggio della finestra, cercando i messaggi key-down. Se l'utente preme una delle combinazioni di tasti elencate nella tabella dei tasti di scelta rapida, **TranslateAccelerator** invia un messaggio [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) alla finestra. La funzione invia **WM \_ COMMAND** richiamando direttamente la routine della finestra. Quando **TranslateAccelerator** converte correttamente un tratto di tasto, la funzione restituisce un valore diverso da zero, il che significa che è necessario ignorare la normale elaborazione del messaggio. In caso **contrario, TranslateAccelerator** restituisce zero. In tal caso, passare il messaggio della finestra [**a TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) e [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), come di consueto.

Ecco come il programma di disegno può gestire il [**messaggio WM \_ COMMAND:**](/windows/desktop/menurc/wm-command)


```C++
    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case ID_DRAW_MODE:
            SetMode(DrawMode);
            break;

        case ID_SELECT_MODE:
            SetMode(SelectMode);
            break;

        case ID_TOGGLE_MODE:
            if (mode == DrawMode)
            {
                SetMode(SelectMode);
            }
            else
            {
                SetMode(DrawMode);
            }
            break;
        }
        return 0;

```



Questo codice presuppone che sia `SetMode` una funzione definita dall'applicazione per passare da una modalità all'altra. I dettagli su come gestire ogni comando dipendono ovviamente dal programma.

## <a name="next"></a>Prossima

[Impostazione dell'immagine del cursore](setting-the-cursor-image.md)

 

 

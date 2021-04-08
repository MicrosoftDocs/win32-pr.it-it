---
title: Tabelle dei tasti di scelta rapida
description: .
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9929445809bee71f273b6bd2334e182de59edbfa
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046754"
---
# <a name="accelerator-tables"></a>Tabelle dei tasti di scelta rapida

Le applicazioni spesso definiscono scelte rapide da tastiera, ad esempio CTRL + O per il comando Apri file. È possibile implementare le scelte rapide da tastiera gestendo singoli messaggi di [**WM \_**](/windows/desktop/inputdev/wm-keydown) . Tuttavia, le tabelle degli acceleratori forniscono una soluzione migliore:

-   Richiede un minor numero di codice.
-   Consolida tutti i collegamenti in un unico file di dati.
-   Supporta la localizzazione in altre lingue.
-   Consente ai tasti di scelta rapida e ai comandi di menu di usare la stessa logica dell'applicazione.

Una *tabella di tasti di scelta rapida* è una risorsa di dati che esegue il mapping delle combinazioni di tasti, ad esempio CTRL + O, ai comandi dell'applicazione. Prima di vedere come usare una tabella di tasti di scelta rapida, è necessaria una rapida introduzione alle risorse. Una *risorsa* è un BLOB di dati incorporato in un file binario dell'applicazione (exe o dll). Le risorse archiviano i dati necessari per l'applicazione, ad esempio menu, cursori, icone, immagini, stringhe di testo o qualsiasi tipo di dati dell'applicazione personalizzata. L'applicazione carica i dati della risorsa dal file binario in fase di esecuzione. Per includere le risorse in un file binario, eseguire le operazioni seguenti:

1.  Creare un file di definizione di risorsa (RC). Questo file definisce i tipi di risorse e i relativi identificatori. Il file di definizione della risorsa può includere riferimenti ad altri file. Ad esempio, una risorsa icona viene dichiarata nel file RC, ma l'immagine dell'icona viene archiviata in un file separato.
2.  Usare il compilatore di risorse di Microsoft Windows (RC) per compilare il file di definizione di risorsa in un file di risorse compilato (res). Il compilatore RC viene fornito con Visual Studio e anche con la Windows SDK.
3.  Collegare il file di risorse compilato al file binario.

Questi passaggi sono approssimativamente equivalenti al processo di compilazione/collegamento per i file di codice. Visual Studio offre un set di editor di risorse che semplificano la creazione e la modifica delle risorse. Questi strumenti non sono disponibili nelle edizioni Express di Visual Studio. Tuttavia, un file RC è semplicemente un file di testo e la sintassi è documentata in MSDN, quindi è possibile creare un file RC usando un editor di testo. Per ulteriori informazioni, vedere [informazioni sui file di risorse](/windows/desktop/menurc/about-resource-files).

## <a name="defining-an-accelerator-table"></a>Definizione di una tabella dei tasti di scelta rapida

Una tabella di tasti di scelta rapida è una tabella di tasti di scelta rapida. Ogni collegamento è definito da:

-   Identificatore numerico. Questo numero identifica il comando dell'applicazione che verrà richiamato dal collegamento.
-   Il carattere ASCII o il codice della chiave virtuale del collegamento.
-   Tasti di modifica facoltativi: ALT, MAIUSC o CTRL.

La tabella dei tasti di scelta rapida contiene un identificatore numerico che identifica la tabella nell'elenco delle risorse dell'applicazione. Viene ora creata una tabella dei tasti di scelta rapida per un semplice programma di disegno. Questo programma disporrà di due modalità, modalità di visualizzazione e modalità di selezione. In modalità di estrazione, l'utente può creare forme. In modalità di selezione, l'utente può selezionare forme. Per questo programma si desidera definire i tasti di scelta rapida seguenti.



| Tasto di scelta rapida | Comando                   |
|----------|---------------------------|
| CTRL+M   | Consente di passare da una modalità all'altra.     |
| F1       | Passa alla modalità di estrazione.      |
| F2       | Passa alla modalità di selezione. |



 

Per prima cosa, definire gli identificatori numerici per la tabella e per i comandi dell'applicazione. Questi valori sono arbitrari. È possibile assegnare costanti simboliche per gli identificatori definendoli in un file di intestazione. Ad esempio:


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



In questo esempio, il valore `IDR_ACCEL1` identifica la tabella dei tasti di scelta rapida e le tre costanti successive definiscono i comandi dell'applicazione. Per convenzione, un file di intestazione che definisce le costanti di risorsa è spesso denominato Resource. h. L'elenco successivo Mostra il file di definizione di risorsa.


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



I tasti di scelta rapida vengono definiti tra parentesi graffe. Ogni collegamento contiene le voci seguenti.

-   Il codice della chiave virtuale o il carattere ASCII che richiama il collegamento.
-   Comando dell'applicazione. Si noti che nell'esempio vengono usate costanti simboliche. Il file di definizione della risorsa include Resource. h, in cui sono definite queste costanti.
-   La parola chiave **VIRTKEY** indica che la prima voce è un codice di chiave virtuale. L'altra opzione consiste nell'usare caratteri ASCII.
-   Modificatori facoltativi: ALT, CTRL o MAIUSC.

Se si usano caratteri ASCII per i collegamenti, un carattere minuscolo sarà un tasto di scelta rapida diverso da un carattere maiuscolo. (Ad esempio, la digitazione di ' a' potrebbe richiamare un comando diverso rispetto alla digitazione di ' A '). Questo potrebbe confondere gli utenti, quindi è in genere preferibile usare i codici a chiave virtuale, anziché i caratteri ASCII, per i collegamenti.

## <a name="loading-the-accelerator-table"></a>Caricamento della tabella dei tasti di scelta rapida

Per poter utilizzare il programma, è necessario caricare la risorsa per la tabella dei tasti di scelta rapida. Per caricare una tabella dei tasti di scelta rapida, chiamare la funzione [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) .


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



Chiamare questa funzione prima di immettere il ciclo di messaggi. Il primo parametro è l'handle per il modulo. Questo parametro viene passato alla funzione [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) . Per informazioni dettagliate, vedere [WinMain: punto di ingresso dell'applicazione](winmain--the-application-entry-point.md). Il secondo parametro è l'identificatore di risorsa. La funzione restituisce un handle per la risorsa. Si ricordi che un handle è un tipo opaco che fa riferimento a un oggetto gestito dal sistema. Se la funzione ha esito negativo, restituisce **null**.

È possibile rilasciare una tabella dei tasti di scelta rapida chiamando [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable). Tuttavia, il sistema rilascia automaticamente la tabella quando il programma viene chiuso, quindi è necessario chiamare questa funzione solo se si sostituisce una tabella con un'altra. Questo è un esempio interessante nell'argomento [creazione di acceleratori modificabili dall'utente](/windows/desktop/menurc/using-keyboard-accelerators).

## <a name="translating-key-strokes-into-commands"></a>Conversione dei tratti chiave in comandi

Una tabella di tasti di scelta rapida funziona convertendo i tratti chiave in messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) . Il parametro *wParam* del **\_ comando WM** contiene l'identificatore numerico del comando. Ad esempio, usando la tabella illustrata in precedenza, il tratto della chiave CTRL + M viene convertito in un messaggio di **\_ comando WM** con il valore `ID_TOGGLE_MODE` . Per eseguire questa operazione, modificare il ciclo di messaggi nel modo seguente:


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



Questo codice aggiunge una chiamata alla funzione [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) all'interno del ciclo di messaggi. La funzione **TranslateAccelerator** esamina ogni messaggio della finestra, cercando i messaggi di chiave inattiva. Se l'utente preme una delle combinazioni di tasti elencate nella tabella dei tasti di scelta rapida, **TranslateAccelerator** Invia un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) alla finestra. La funzione Invia **il \_ comando WM** richiamando direttamente la routine della finestra. Quando **TranslateAccelerator** converte correttamente un tratto di chiave, la funzione restituisce un valore diverso da zero, il che significa che è necessario ignorare la normale elaborazione del messaggio. In caso contrario, **TranslateAccelerator** restituisce zero. In tal caso, passare il messaggio della finestra a [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) e [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), come di consueto.

Ecco il modo in cui il programma di disegno può gestire il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) :


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



Questo codice presuppone che `SetMode` sia una funzione definita dall'applicazione per passare tra le due modalità. I dettagli su come gestire ogni comando dipendono ovviamente dal programma.

## <a name="next"></a>Prossima

[Impostazione dell'immagine del cursore](setting-the-cursor-image.md)

 

 
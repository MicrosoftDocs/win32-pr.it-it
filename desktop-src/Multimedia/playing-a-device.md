---
title: Riproduzione di un dispositivo
description: Riproduzione di un dispositivo
ms.assetid: 48d83e06-9e6e-498b-ad9b-0b66f235db25
keywords:
- MCI_PLAY comando
- Finestra di riproduzione di MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9efc06b3d5f33dfb798aa4c47bf7d5a7a8bab45842de1da170c860d2a4a5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372642"
---
# <a name="playing-a-device"></a>Riproduzione di un dispositivo

Il [**comando play**](play.md) ([**MCI \_ PLAY**](mci-play.md)) avvia la riproduzione di un dispositivo. Senza flag, questo comando inizia la riproduzione dalla posizione corrente e viene riprodotto fino a quando il comando non viene interrotto o fino a quando non viene raggiunta la fine del file o del file multimediale. Dopo la riproduzione, la posizione corrente si trova alla fine del contenuto multimediale. È anche possibile usare [**il comando seek**](seek.md) ([**MCI \_ SEEK**](mci-seek.md)) per modificare la posizione corrente.

La maggior parte dei **dispositivi** che supportano il comando play supporta anche i flag "from" (MCI FROM) e \_ "to" (MCI \_ TO). Questi flag indicano la posizione in cui deve essere avviata e interrotta la riproduzione del dispositivo. Ad esempio, il comando seguente riproduce un disco audio CD dall'inizio della prima traccia usando la [**funzione mciSendString:**](/previous-versions//dd757161(v=vs.85))


```C++
mciSendString("play cdaudio from 0", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Alcuni tipi di dispositivo estendono questo comando per sfruttare le funzionalità di un particolare dispositivo. Ad esempio, il comando [**play**](play.md) per il tipo di dispositivo **videodisc** include i flag "fast" (MCI \_ \_ VD PLAY \_ FAST), "slow" (MCI \_ VD PLAY SLOW) e \_ \_ "scan" (MCI \_ VD PLAY \_ \_ SCAN).

> [!Note]  
> Le unità assegnate al valore di posizione dipendono dal formato dell'ora usato dal dispositivo. Ogni dispositivo ha un formato di ora predefinito, ma è necessario specificare il formato dell'ora usando il [**comando set**](set.md) ([**MCI \_ SET**](mci-set.md)) prima di eseguire tutti i comandi che usano valori di posizione.

 

## <a name="playing-an-avi-file"></a>Riproduzione di un file AVI

I file video Windows sono costituito da almeno due flussi di dati interleaved: un flusso video (grafico) e un flusso audio. È possibile riprodurre facilmente questi file audio-video interleaved (AVI) usando i comandi MCI. Le sezioni seguenti illustrano la riproduzione di file AVI.

## <a name="setting-up-an-mciavi-playback-window"></a>Configurazione di una finestra di riproduzione MCIAVI

L'applicazione può specificare le opzioni seguenti per definire la finestra di riproduzione per la riproduzione di un file AVI:

-   Usare la finestra popup predefinita del driver MCIAVI.
-   Specificare una finestra padre e uno stile di finestra che il driver MCIAVI può usare per creare la finestra di riproduzione.
-   Specificare una finestra di riproduzione per il driver MCIAVI da usare per la riproduzione.
-   Riprodurre il file AVI su schermo intero.

Se l'applicazione non specifica alcuna opzione di finestra, il driver MCIAVI crea una finestra predefinita per la riproduzione della sequenza. Il driver crea questa finestra di riproduzione per il comando open [**(**](open.md) [**MCI \_ OPEN),**](mci-open.md)ma non visualizza la finestra fino a quando l'applicazione non invia un comando per visualizzare la finestra o riprodurre il file. Questa finestra di riproduzione predefinita è una finestra popup con un bordo di ridimensionamento, una barra del titolo, una cornice densa, un **menu** della finestra e un pulsante Riduci a icona.

L'applicazione può anche specificare un handle di finestra padre e uno stile di finestra quando esegue il **comando open.** In questo caso, il driver MCIAVI crea una finestra basata su queste specifiche anziché sulla finestra popup predefinita. L'applicazione può specificare qualsiasi stile di finestra disponibile per la [funzione CreateWindow.](/windows/win32/api/winuser/nf-winuser-createwindowa) Gli stili che richiedono una finestra padre, ad esempio WS \_ CHILD, devono includere un handle di finestra padre.

L'applicazione può anche creare una propria finestra e fornire l'handle al driver MCIAVI usando il [**comando window**](window.md) ([**MCI \_ WINDOW**](mci-window.md)). Il driver MCIAVI usa questa finestra invece di crearne una propria.

Quando il driver MCIAVI crea la finestra di riproduzione o ottiene un handle di finestra dall'applicazione, non visualizza la finestra finché l'applicazione non riproduce la sequenza o invia un comando per visualizzare la finestra. L'applicazione può usare il **comando** window per visualizzare la finestra senza riprodurre la sequenza. Ad esempio, il comando seguente visualizza la finestra [**usando mciSendString**](/previous-versions//dd757161(v=vs.85)):


```C++
mciSendString("window movie state show", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



In questo esempio "movie" è un alias per il dispositivo video digitale.

L'applicazione può anche riprodurre un file AVI a schermo intero. Per riprodurre a schermo intero, modificare il comando [**play**](play.md) ([**MCI \_ PLAY**](mci-play.md)) con il flag "fullscreen" (MCI \_ MCIAVI \_ PLAY \_ FULLSCREEN). Quando l'applicazione usa questo flag, il driver MCIAVI usa un formato a schermo intero da 320x240 pixel per la riproduzione della sequenza. Ad esempio, il comando seguente riproduce il file aperto a schermo intero (usando "movie" come alias):


```C++
mciSendString("play movie fullscreen", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



## <a name="changing-the-playback-state-for-an-avi-file"></a>Modifica dello stato di riproduzione per un file AVI

L'applicazione può usare il comando [**seek**](seek.md) ([**MCI \_ SEEK**](mci-seek.md)) per spostare la posizione corrente all'inizio, alla fine o a una posizione arbitraria in un file AVI. Esistono due modalità di ricerca per il driver MCIAVI: esatta e inesatta. L'applicazione può modificare la modalità di ricerca usando [**il comando set**](set.md) ([**MCI \_ SET**](mci-set.md)). Quando si usa **set** "seek exactly on", il driver MCIAVI cerca esattamente il frame specificato dall'applicazione. Ciò potrebbe causare un ritardo se il file è compresso a livello temporale e l'applicazione non specifica un fotogramma chiave. Quando si **usa set** "seek exactly off", il driver MCIAVI cerca il fotogramma chiave più vicino in un file compresso a livello temporale.

Alcuni comandi MCI consentono all'applicazione di modificare la riproduzione di un file AVI in altri modi. Ad esempio, un file AVI, per impostazione predefinita, viene riprodotto alla velocità normale, ma l'applicazione può aumentare o diminuire questa velocità usando il flag "speed" con il **comando set.** Per i file AVI, un valore di velocità di 1000 è tipico. Pertanto, per riprodurre un film a metà della velocità tipica, l'applicazione può usare il **set** di comandi "movie speed 500"; in alternativa, può usare **impostare** "movie speed 2000" per riprodurre la sequenza al doppio della velocità normale.

Il [**comando setaudio**](setaudio.md) ([**MCI \_ SETAUDIO**](mci-setaudio.md)) consente all'applicazione di controllare la parte audio di un file AVI. L'applicazione può disattivare l'audio durante la riproduzione o, nel caso di più file di flusso audio, selezionare il flusso audio riprodotto.

Il driver MCIAVI dispone di una finestra di dialogo per controllare alcune delle opzioni di riproduzione. Alcune delle opzioni disponibili per l'utente includono la selezione della riproduzione orientata alla finestra o a schermo intero, la selezione della modalità di ricerca e lo zoom dell'immagine. L'applicazione può fare in modo che MCIAVI visualizza questa finestra di dialogo usando [**il comando configure**](configure.md) ([**MCI \_ CONFIGURE).**](mci-configure.md)

## <a name="stream-handlers"></a>Gestori di flusso

I dati in un file AVI vengono trattati come una serie di flussi. Un file AVI contiene in genere un flusso audio e video e potrebbe essere presente anche un flusso personalizzato che contiene testo o altri dati personalizzati. Il driver MCIAVI può usare gestori diversi per questi flussi di dati. Per altre informazioni sui file AVI personalizzati, vedere [Gestori di file e flussi personalizzati.](custom-file-and-stream-handlers.md)

 

 
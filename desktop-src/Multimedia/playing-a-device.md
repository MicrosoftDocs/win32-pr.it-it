---
title: Riproduzione di un dispositivo
description: Riproduzione di un dispositivo
ms.assetid: 48d83e06-9e6e-498b-ad9b-0b66f235db25
keywords:
- Comando MCI_PLAY
- Finestra di riproduzione MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73d8b6539e842a1ffa632ed1efae5c2c8d3cda1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963082"
---
# <a name="playing-a-device"></a>Riproduzione di un dispositivo

Il comando [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)) avvia la riproduzione di un dispositivo. Senza flag, questo comando inizia la riproduzione dalla posizione corrente e viene riprodotto fino a quando il comando non viene interrotto o fino a quando non viene raggiunta la fine del file multimediale o del file. Dopo la riproduzione, la posizione corrente si trova alla fine del supporto. È inoltre possibile utilizzare il comando [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)) per modificare la posizione corrente.

La maggior parte dei dispositivi che supportano il comando **Play** supporta anche i flag "from" (MCI \_ from) e "to" (MCI \_ to). Questi flag indicano la posizione in cui il dispositivo deve avviare e arrestare la riproduzione. Ad esempio, il comando seguente riproduce un disco audio CD dall'inizio della prima traccia usando la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


```C++
mciSendString("play cdaudio from 0", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Alcuni tipi di dispositivi estendono questo comando per sfruttare le funzionalità di un determinato dispositivo. Ad esempio, il comando [**Play**](play.md) per il tipo di dispositivo **videodisco** include i flag "Fast" (MCI \_ VD \_ Play \_ Fast), "Slow" (MCI \_ VD \_ Play \_ Slow) e "Scan" (MCI \_ VD \_ Play \_ Scan).

> [!Note]  
> Le unità assegnate al valore di posizione dipendono dal formato dell'ora usato dal dispositivo. Ogni dispositivo ha un formato di ora predefinito, ma è necessario specificare il formato dell'ora usando il comando [**set**](set.md) ([**MCI \_ set**](mci-set.md)) prima di emettere tutti i comandi che usano i valori di posizione.

 

## <a name="playing-an-avi-file"></a>Riproduzione di un file AVI

I file video in Windows sono costituiti da almeno due flussi di dati con interfoliazione: un flusso video (pittorico) e un flusso audio. È possibile riprodurre facilmente i file audio-video con interfoliazione (AVI) usando i comandi MCI. Le sezioni seguenti illustrano la riproduzione di file AVI.

## <a name="setting-up-an-mciavi-playback-window"></a>Impostazione di una finestra di riproduzione MCIAVI

L'applicazione può specificare le opzioni seguenti per definire la finestra di riproduzione per la riproduzione di un file AVI:

-   Usare la finestra popup predefinita del driver MCIAVI.
-   Specificare una finestra padre e uno stile finestra che il driver MCIAVI può usare per creare la finestra di riproduzione.
-   Specificare una finestra di riproduzione per il driver MCIAVI da usare per la riproduzione.
-   Riprodurre il file AVI in una visualizzazione a schermo intero.

Se l'applicazione non specifica alcuna opzione della finestra, il driver MCIAVI crea una finestra predefinita per la riproduzione della sequenza. Il driver crea questa finestra di riproduzione per il comando [**Apri**](open.md) ([**MCI \_ Open**](mci-open.md)), ma non Visualizza la finestra finché l'applicazione non invia un comando per visualizzare la finestra o riprodurre il file. Questa finestra di riproduzione predefinita è una finestra popup con un bordo di ridimensionamento, una barra del titolo, un frame spessa, un menu **finestra** e un pulsante Riduci a icona.

L'applicazione può inoltre specificare un handle della finestra padre e uno stile della finestra quando emette il comando **Apri** . In questo caso, il driver MCIAVI crea una finestra basata su queste specifiche anziché sulla finestra popup predefinita. L'applicazione può specificare qualsiasi stile di finestra disponibile per la funzione [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) . Gli stili che richiedono una finestra padre, ad esempio WS \_ child, devono includere un handle della finestra padre.

L'applicazione può anche creare una propria finestra e fornire l'handle al driver MCIAVI usando il comando [**finestra**](window.md) ([**\_ finestra MCI**](mci-window.md)). Il driver MCIAVI usa questa finestra anziché crearne una propria.

Quando il driver MCIAVI crea la finestra di riproduzione o ottiene un handle di finestra dall'applicazione, non Visualizza la finestra finché l'applicazione non riproduce la sequenza o Invia un comando per visualizzare la finestra. L'applicazione può usare il comando **finestra** per visualizzare la finestra senza riprodurre la sequenza. Ad esempio, il comando seguente Visualizza la finestra usando [**mciSendString**](/previous-versions//dd757161(v=vs.85)):


```C++
mciSendString("window movie state show", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



In questo esempio, "Movie" è un alias per il dispositivo Digital-video.

L'applicazione può anche riprodurre un file AVI a schermo intero. Per riprodurre a schermo intero, modificare il comando [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)) con il flag "fullscreen \_ MCIAVI \_ Play fullscreen" \_ . Quando l'applicazione usa questo flag, il driver MCIAVI usa un formato a schermo intero 320 per 240 pixel per la riproduzione della sequenza. Ad esempio, il comando seguente riproduce il file aperto a schermo intero (usando "Movie" come alias):


```C++
mciSendString("play movie fullscreen", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



## <a name="changing-the-playback-state-for-an-avi-file"></a>Modifica dello stato di riproduzione per un file AVI

L'applicazione può usare il comando [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)) per spostare la posizione corrente all'inizio, alla fine o a una posizione arbitraria in un file AVI. Sono disponibili due modalità di ricerca per il driver MCIAVI: esatta e inesatta. L'applicazione può modificare la modalità di ricerca usando il comando [**set**](set.md) ([**MCI \_ set**](mci-set.md)). Quando si usa il **set** "seek exactly on", il driver MCIAVI cerca esattamente il frame specificato dall'applicazione. Questo potrebbe causare un ritardo se il file viene compresso temporaneamente e l'applicazione non specifica un fotogramma chiave. Quando si usa **set** "seek exactly off", il driver MCIAVI Cerca il fotogramma chiave più vicino in un file compresso temporaneamente.

Alcuni comandi MCI consentono all'applicazione di modificare in altri modi la riproduzione di un file AVI. Ad esempio, un file AVI, per impostazione predefinita, riproduce la velocità normale, ma l'applicazione può aumentare o diminuire questa velocità usando il flag "Speed" con il comando **set** . Per i file AVI, un valore di velocità pari a 1000 è tipico. Quindi, per riprodurre un film a metà della velocità tipica, l'applicazione può usare il **set** di comandi "movie Speed 500"; in alternativa, è possibile usare l' **impostazione** "movie Speed 2000" per riprodurre la sequenza al doppio della velocità normale.

Il comando [**seaudio**](setaudio.md) ([**MCI \_ sefonica**](mci-setaudio.md)) consente all'applicazione di controllare la parte audio di un file AVI. Nell'applicazione è possibile disattivare l'audio durante la riproduzione o, nel caso di più file di flusso audio, selezionare il flusso audio che viene riprodotto.

Il driver MCIAVI dispone di una finestra di dialogo per controllare alcune opzioni di riproduzione. Alcune opzioni disponibili per l'utente includono la selezione della riproduzione orientata a finestre o a schermo intero, la selezione della modalità di ricerca e l'ingrandimento dell'immagine. L'applicazione può disporre di MCIAVI per visualizzare questa finestra di dialogo tramite il comando [**Configura**](configure.md) ([**MCI \_ Configure**](mci-configure.md)).

## <a name="stream-handlers"></a>Gestori di flusso

I dati in un file AVI vengono considerati come una serie di flussi. Un file AVI contiene in genere un flusso audio e video e potrebbe essere presente anche un flusso personalizzato che contiene testo o altri dati personalizzati. Il driver MCIAVI può usare gestori diversi per questi flussi di dati. Per altre informazioni sui file AVI personalizzati, vedere [gestori di file e flussi personalizzati](custom-file-and-stream-handlers.md).

 

 
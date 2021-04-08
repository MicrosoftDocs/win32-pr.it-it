---
title: Apertura di un dispositivo
description: Apertura di un dispositivo
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- Comando MCI_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd975b0dd5004fb4b1209003568b7fd5901cfc4e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046593"
---
# <a name="opening-a-device"></a>Apertura di un dispositivo

Prima di usare un dispositivo, è necessario inizializzarlo usando il comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)). Questo comando carica il driver in memoria (se non è già caricato) e recupera l'identificatore del dispositivo che verrà usato per identificare il dispositivo nei successivi comandi MCI. È necessario controllare il valore restituito della funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) o [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) prima di usare un nuovo identificatore di dispositivo per assicurarsi che l'identificatore sia valido. È anche possibile recuperare un identificatore di dispositivo tramite la funzione [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) .

Come tutti i messaggi di comando MCI, **MCI \_ Open** ha una struttura associata. Queste strutture sono talvolta denominate *blocchi di parametri*. La struttura predefinita per **MCI \_ Open** è [**MCI \_ Open \_ parametri**](mci-open-parms.md). Alcuni dispositivi, ad esempio la *forma d'onda* e la *sovrapposizione*, hanno strutture estese, ad esempio [**MCI \_ Wave \_ Open \_ parametri**](mci-wave-open-parms.md) e [**MCI \_ OVLY \_ Open \_ parametri**](mci-ovly-open-parms.md), per contenere parametri facoltativi aggiuntivi. A meno che non sia necessario usare questi parametri aggiuntivi, è possibile usare la struttura **MCI \_ Open \_ parametri** con qualsiasi dispositivo MCI.

Il numero di dispositivi che è possibile aprire è limitato solo dalla quantità di memoria disponibile.

## <a name="using-an-alias"></a>Uso di un alias

Quando si apre un dispositivo, è possibile usare il flag "alias" per specificare un identificatore del dispositivo per il dispositivo. Questo flag consente di assegnare un breve identificatore di dispositivo per i dispositivi composti con nomi di file lunghi e consente di aprire più istanze dello stesso file o dispositivo.

Ad esempio, il comando seguente assegna l'identificatore di dispositivo "birdcall" al nome file di lunghezza C: \\ NABIRDS \\ suoni \\ MOCKMTNG. WAV


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Nell'interfaccia del messaggio di comando è possibile specificare un alias usando il membro **lpstrAlias** della struttura [**\_ \_ parametri aperta di MCI**](mci-open-parms.md) .

## <a name="specifying-a-device-type"></a>Specifica di un tipo di dispositivo

Quando si apre un dispositivo, è possibile usare il flag "Type" per fare riferimento a un tipo di dispositivo, anziché a un driver di dispositivo specifico. Nell'esempio seguente viene aperto il file Waveform-Audio file C: \\ Windows \\ Chimes. WAV (usando il flag "Type" per specificare il tipo di dispositivo **WaveAudio** ) e assegna l'alias "Chimes":


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Nell'interfaccia del messaggio di comando, la funzionalità del flag "Type" viene fornita dal membro **lpstrDeviceType** della struttura [**\_ \_ parametri aperta di MCI**](mci-open-parms.md) .

## <a name="simple-and-compound-devices"></a>Dispositivi semplici e composti

MCI classifica i driver di dispositivo come *composti* o *semplici*. I driver per i dispositivi composti richiedono il nome di un file di dati per la riproduzione. i driver per i dispositivi semplici non lo sono.

I dispositivi semplici includono i dispositivi **CDAudio** e **videodisco** . Esistono due modi per aprire i dispositivi semplici:

-   Specificare un puntatore a una stringa con terminazione null contenente il nome del dispositivo dal registro di sistema o dal file di SYSTEM.INI.

    Ad esempio, è possibile aprire un dispositivo **videodisco** usando il comando seguente:


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



In questo caso, "videodisco" è il nome del dispositivo dal registro di sistema o dalla \[ \] sezione mci del SYSTEM.INI.

-   Specificare il nome effettivo del driver di dispositivo. L'apertura di un dispositivo con il nome file del driver di dispositivo, tuttavia, rende l'applicazione specifica del dispositivo e può impedire l'esecuzione dell'applicazione in caso di modifica della configurazione di sistema. Se si usa un nome di file, non è necessario specificare il percorso completo o l'estensione del nome file. MCI presuppone che i driver si trovino in una directory di sistema e dispongano di. Estensione DRV filename.

I dispositivi composti includono i dispositivi **WaveAudio** e **sequencer** . I dati per un dispositivo composto vengono talvolta definiti *elementi del dispositivo*. Questo documento, tuttavia, in genere fa riferimento a questi dati come file, anche se in alcuni casi i dati potrebbero non essere archiviati come file.

Sono disponibili tre modi per aprire un dispositivo composto:

-   Specificare solo il nome del dispositivo. In questo modo è possibile aprire un dispositivo composto senza associare un nome di file. La maggior parte dei dispositivi composti elabora solo i comandi [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) e [**Close**](close.md) ([**MCI \_ Close**](mci-close.md)) quando vengono aperti in questo modo.
-   Specificare solo il nome del file. Il nome del dispositivo è determinato dalle associazioni nel registro di sistema.
-   Specificare il nome del file e il nome del dispositivo. MCI ignora le voci nel registro di sistema e apre il nome del dispositivo specificato.

Per associare un file di dati a un dispositivo specifico, è possibile specificare il nome file e il nome del dispositivo. Il comando seguente, ad esempio, apre il dispositivo **WaveAudio** con il nome file. SND


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Nell'interfaccia della stringa di comando è inoltre possibile abbreviare la specifica del nome del dispositivo utilizzando il formato punto esclamativo alternativo, come documentato con il comando [**Apri**](open.md) .

## <a name="opening-a-device-using-the-filename-extension"></a>Apertura di un dispositivo usando l'estensione filename

Se il comando [**Apri**](open.md) ([**MCI \_ Open**](mci-open.md)) specifica solo il nome del file, MCI usa l'estensione del nome file per selezionare il dispositivo appropriato nell'elenco nel registro di sistema o nella \[ sezione estensioni MCI \] del file SYSTEM.INI. Le voci nella \[ sezione estensioni MCI \] usano il formato seguente:

*\_*  =  *\_ nome del dispositivo* di estensione del nome file

MCI utilizza in modo implicito il *\_ nome del dispositivo* se l'estensione viene trovata e se non è stato specificato un nome di dispositivo nel comando **Apri** .

Nell'esempio seguente viene illustrata una \[ sezione delle estensioni MCI tipiche \] :


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



Usando queste definizioni, MCI apre il dispositivo **WaveAudio** se viene eseguito il comando seguente:


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a>Nuovi file di dati

Per creare un nuovo file di dati, è sufficiente specificare un nome file vuoto. MCI non salva un nuovo file fino a quando non lo si salva usando il comando [**Save**](save.md) ([**MCI \_ Save**](mci-save.md)). Quando si crea un nuovo file, è necessario includere un alias del dispositivo con il comando [**Apri**](open.md) ([**MCI \_ Open**](mci-open.md)).

Nell'esempio seguente viene aperto un nuovo file **WaveAudio** , viene avviata e arrestata la registrazione, quindi il file viene salvato e chiuso:


```C++
mciSendString("open new type waveaudio alias capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("record capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("stop capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("save capture orca.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="sharable-devices"></a>Dispositivi condivisibili

Il flag "condivisibile" (MCI \_ aperto) \_ del comando [**Apri**](open.md) ([**MCI \_ Open**](mci-open.md)) consente a più applicazioni di accedere simultaneamente allo stesso dispositivo (o file) e all'istanza del dispositivo. Se l'applicazione apre un dispositivo o un file come condivisibile, anche altre applicazioni possono accedervi aprendolo come condivisibile. Il file o il dispositivo condiviso fornisce a ogni applicazione la possibilità di modificare i parametri che ne controllano lo stato operativo. Ogni volta che un dispositivo o un file viene aperto come condivisibile, MCI restituisce un identificatore univoco del dispositivo, anche se gli identificatori fanno riferimento alla stessa istanza.

Se l'applicazione apre un dispositivo o un file senza specificarne lo stato condivisibile, nessun'altra applicazione potrà accedervi fino a quando l'applicazione non la chiude. Inoltre, se un dispositivo supporta solo un'istanza aperta, il comando **Apri** avrà esito negativo se si specifica il flag condivisibile.

Se l'applicazione apre un dispositivo e specifica che è condivisibile, l'applicazione non deve fare supposizioni sullo stato del dispositivo. L'applicazione potrebbe dover compensare le modifiche apportate da altre applicazioni che accedono al dispositivo.

La maggior parte dei file composti non è condivisibile. Tuttavia, è possibile aprire più file oppure è possibile aprire più volte un singolo file. Se si apre un singolo file più volte, MCI crea un'istanza indipendente per ogni istanza con uno stato operativo univoco.

Se si aprono più istanze di un file, è necessario assegnare a ognuno un identificatore univoco del dispositivo. È possibile usare un alias, come descritto nella sezione seguente, per assegnare un nome univoco per ogni file.

 

 
---
title: Apertura di un dispositivo
description: Apertura di un dispositivo
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- MCI_OPEN comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34408cef4e85ed7200b91c610e60ca546ff488ce5ad45edee12159a664f319fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802318"
---
# <a name="opening-a-device"></a>Apertura di un dispositivo

Prima di usare un dispositivo, è necessario inizializzarlo usando il [**comando open**](open.md) ([**MCI \_ OPEN).**](mci-open.md) Questo comando carica il driver in memoria (se non è già caricato) e recupera l'identificatore di dispositivo che verrà utilizzato per identificare il dispositivo nei comandi MCI successivi. È necessario controllare il valore restituito della [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) o [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) prima di usare un nuovo identificatore di dispositivo per assicurarsi che l'identificatore sia valido. È anche possibile recuperare un identificatore di dispositivo usando la [**funzione mciGetDeviceID.**](/previous-versions//dd757156(v=vs.85))

Come tutti i messaggi di comando **MCI, MCI \_ OPEN** ha una struttura associata. Queste strutture sono talvolta denominate *blocchi di parametri*. La struttura predefinita per **MCI \_ OPEN** è [**MCI \_ OPEN \_ PARMS.**](mci-open-parms.md) Alcuni dispositivi (  ad esempio forma d'onda e sovrapposizione *)* hanno strutture estese (ad esempio [**MCI WAVE \_ OPEN \_ \_ PARMS**](mci-wave-open-parms.md) e [**MCI \_ OVLY \_ OPEN \_ PARMS)**](mci-ovly-open-parms.md)per supportare parametri facoltativi aggiuntivi. A meno che non sia necessario usare questi parametri aggiuntivi, è possibile usare la **struttura MCI \_ OPEN \_ PARMS** con qualsiasi dispositivo MCI.

Il numero di dispositivi aperti è limitato solo dalla quantità di memoria disponibile.

## <a name="using-an-alias"></a>Uso di un alias

Quando si apre un dispositivo, è possibile usare il flag "alias" per specificare un identificatore di dispositivo per il dispositivo. Questo flag consente di assegnare un identificatore di dispositivo breve per i dispositivi composti con nomi di file lunghi e consente di aprire più istanze dello stesso file o dispositivo.

Ad esempio, il comando seguente assegna l'identificatore di dispositivo "birdcall" al nome file lungo C: \\ NABIRDS \\ SOUNDS \\ MOCKMTNG. Wav:


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Nell'interfaccia command-message specificare un alias usando il membro **lpstrAlias** della [**struttura MCI \_ OPEN \_ PARMS.**](mci-open-parms.md)

## <a name="specifying-a-device-type"></a>Specifica di un tipo di dispositivo

Quando si apre un dispositivo, è possibile usare il flag "type" per fare riferimento a un tipo di dispositivo, anziché a un driver di dispositivo specifico. Nell'esempio seguente viene aperto il file waveform-audio C: \\ WINDOWS \\ CHIMES. WAV (usando il flag "type" per specificare il **tipo di dispositivo waveaudio)** e assegna l'alias "chimes":


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



Nell'interfaccia command-message la funzionalità del flag "type" viene fornita dal membro **lpstrDeviceType** della struttura [**MCI \_ OPEN \_ PARMS.**](mci-open-parms.md)

## <a name="simple-and-compound-devices"></a>Dispositivi semplici e composti

MCI classifica i driver di dispositivo *come composti* *o semplici.* I driver per i dispositivi composti richiedono il nome di un file di dati per la riproduzione; i driver per i dispositivi semplici non lo fanno.

I dispositivi semplici **includono i dispositivi cdaudio** **e videodisc.** Esistono due modi per aprire dispositivi semplici:

-   Specificare un puntatore a una stringa con terminazione Null contenente il nome del dispositivo dal Registro di sistema o dal SYSTEM.INI file.

    Ad esempio, è possibile aprire un **dispositivo videodisc** usando il comando seguente:


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



In questo caso, "videodisc" è il nome del dispositivo dal Registro di sistema o la sezione \[ mci \] di SYSTEM.INI.

-   Specificare il nome effettivo del driver di dispositivo. L'apertura di un dispositivo con il nome file del driver di dispositivo rende tuttavia l'applicazione specifica del dispositivo e può impedire l'esecuzione dell'applicazione se la configurazione del sistema cambia. Se si usa un nome file, non è necessario specificare il percorso completo o l'estensione del nome file. MCI presuppone che i driver si trovino in una directory di sistema e dispongono di . Estensione del nome file DRV.

I dispositivi composti **includono i dispositivi waveaudio** **e sequencer.** I dati per un dispositivo composto vengono talvolta chiamati elemento *dispositivo*. Questo documento, tuttavia, in genere fa riferimento a questi dati come file, anche se in alcuni casi i dati potrebbero non essere archiviati come file.

Esistono tre modi per aprire un dispositivo composto:

-   Specificare solo il nome del dispositivo. In questo modo è possibile aprire un dispositivo composto senza associare un nome file. La maggior parte dei dispositivi composti elabora solo la funzionalità [**(**](capability.md) [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) e i comandi [**close**](close.md) ([**MCI \_ CLOSE**](mci-close.md)) quando vengono aperti in questo modo.
-   Specificare solo il nome file. Il nome del dispositivo è determinato dalle associazioni nel Registro di sistema.
-   Specificare il nome file e il nome del dispositivo. MCI ignora le voci nel Registro di sistema e apre il nome del dispositivo specificato.

Per associare un file di dati a un dispositivo specifico, è possibile specificare il nome file e il nome del dispositivo. Ad esempio, il comando seguente apre il **dispositivo waveaudio** con il nome file MYVOICE. Snd:


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Nell'interfaccia della stringa di comando è anche possibile abbreviare la specifica del nome del dispositivo usando il formato alternativo del punto esclamativo, come documentato con il [**comando open.**](open.md)

## <a name="opening-a-device-using-the-filename-extension"></a>Apertura di un dispositivo tramite l'estensione filename

Se il [**comando open**](open.md) ([**MCI \_ OPEN**](mci-open.md)) specifica solo il nome file, MCI usa l'estensione del nome file per selezionare il dispositivo appropriato dall'elenco nel Registro di sistema o nella sezione mci extensions del \[ file \] SYSTEM.INI. Le voci nella sezione \[ estensioni mci \] usano il formato seguente:

*nome \_ del dispositivo dell'estensione*  =  *del nome \_ file*

MCI usa in modo *implicito il \_* nome del dispositivo se viene trovata l'estensione e se non è stato specificato un nome di dispositivo nel **comando open.**

L'esempio seguente illustra una sezione \[ tipica delle estensioni \] mci:


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



Usando queste definizioni, MCI apre il **dispositivo waveaudio** se viene eseguito il comando seguente:


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a>Nuovi file di dati

Per creare un nuovo file di dati, è sufficiente specificare un nome file vuoto. MCI non salva un nuovo file fino a quando non lo si salva usando il [**comando save**](save.md) ([**MCI \_ SAVE).**](mci-save.md) Quando si crea un nuovo file, è necessario includere un alias di dispositivo con il [**comando open**](open.md) ([**MCI \_ OPEN).**](mci-open.md)

L'esempio seguente apre un nuovo file **waveaudio,** avvia e arresta la registrazione, quindi salva e chiude il file:


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



## <a name="sharable-devices"></a>Dispositivi sharable

Il flag "condivisibile" (MCI OPEN SHAREABLE) del comando open ( MCI OPEN ) consente a più applicazioni di accedere contemporaneamente allo stesso dispositivo \_ (o file) e all'istanza \_ del dispositivo.[**\_**](mci-open.md) [](open.md) Se l'applicazione apre un dispositivo o un file come condivisione, anche altre applicazioni possono accedervi aprendolo come condivisione. Il dispositivo o il file condiviso offre a ogni applicazione la possibilità di modificare i parametri che ne regolano lo stato operativo. Ogni volta che un dispositivo o un file viene aperto come condivisione, MCI restituisce un identificatore di dispositivo univoco, anche se gli identificatori fanno riferimento alla stessa istanza.

Se l'applicazione apre un dispositivo o un file senza specificarne la condivisione, nessun'altra applicazione può accedervi fino a quando l'applicazione non lo chiude. Inoltre, se un dispositivo supporta una sola istanza aperta, il **comando open** avrà esito negativo se si specifica il flag di condivisione.

Se l'applicazione apre un dispositivo e specifica che è sharable, l'applicazione non deve fare supposizioni sullo stato del dispositivo. L'applicazione potrebbe dover compensare le modifiche apportate da altre applicazioni che accedono al dispositivo.

La maggior parte dei file compositi non è gestibile. tuttavia, è possibile aprire più file oppure un singolo file più volte. Se si apre un singolo file più volte, MCI crea un'istanza indipendente per ogni istanza, con uno stato operativo univoco.

Se si aprono più istanze di un file, è necessario assegnare un identificatore di dispositivo univoco a ognuna. È possibile usare un alias, come descritto nella sezione seguente, per assegnare un nome univoco per ogni file.

 

 
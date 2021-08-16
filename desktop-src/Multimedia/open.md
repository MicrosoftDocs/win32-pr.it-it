---
title: Comando open (Corecrt \_ io.h)
description: Il comando open inizializza un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- Comando open Windows Multimedia
topic_type:
- apiref
api_name:
- open
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d2e585a44c19093fa0d20ab4870f579c67cd568c3a693523242b84910e6589d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373270"
---
# <a name="open-command"></a>comando open

Il comando open inizializza un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("open %s %s %s"), 
  lpszDevice, 
  lpszOpenFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*
</dt> <dd>

Identificatore di un dispositivo o driver di dispositivo MCI. Può trattarsi di un nome di dispositivo (come specificato nel Registro di sistema o nel file SYSTEM.INI) o del nome file del driver di dispositivo. Se si specifica il nome file del driver di dispositivo, è possibile includere facoltativamente . Estensione DRV, ma non includere il percorso del file.

</dd> <dt>

<span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*
</dt> <dd>

Flag che identifica gli elementi da inizializzare. La tabella seguente elenca i tipi di dispositivo che **riconoscono il comando open** e i flag usati da ogni tipo.



| Valore        | Significato                                                        | Significato                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| cdaudio      | alias *device \_ alias* sharable                                  | tipo *di \_ dispositivo*                                                             |
| digitalvideo | alias *device \_ aliaselementname* nostatic parent *hwnd* sharable | style child style overlapped style popup style *type \_* device *\_ type* |
| overlay      | alias *device \_ alias* parent *hwnd* sharable style child         | stile sovrapposto stile popup tipo *di \_* dispositivo tipo *di \_ dispositivo*             |
| sequencer    | alias *device \_ alias* sharable                                 | tipo *di \_ dispositivo*                                                             |
| Vcr          | alias *device \_ alias* sharable                                  | tipo *di \_ dispositivo*                                                             |
| videodisk    | alias *device \_ alias* sharable                                  | tipo *di \_ dispositivo*                                                             |
| Waveaudio    | alias *device \_ alias buffer* buffer *\_ size*                     | Tipo di dispositivo di *tipo condivisione \_*                                                    |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel **parametro lpszOpenFlags** e i relativi significati.



| Valore                 | Significato                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| alias *device \_ alias* | Specifica un nome alternativo per il dispositivo specificato. Se specificato, deve essere usato come *\_ ID dispositivo* nei comandi successivi.                                                                                                                                                                                                                                          |
| *Elementname*         | Specifica il nome dell'elemento dispositivo (file) caricato all'apertura del dispositivo.                                                                                                                                                                                                                                                                                        |
| dimensioni *\_ buffer buffer* | Imposta le dimensioni, in secondi, del buffer usato dal dispositivo audio waveform. Le dimensioni predefinite del buffer vengono impostate quando il dispositivo audio waveform viene installato o configurato. In genere le dimensioni del buffer sono impostate su 4 secondi. Con il dispositivo MCIWAVE, la dimensione minima è di 2 secondi e la dimensione massima è di 9 secondi.                                                |
| *hwnd padre*         | Specifica l'handle di finestra della finestra padre.                                                                                                                                                                                                                                                                                                                    |
| Condivisibile              | Inizializza il dispositivo o il file come condivisione. I tentativi successivi di aprire il dispositivo o il file hanno esito negativo, a meno che non si specifica "sharable" nei comandi di apertura originali **e** successivi. McI restituisce un errore di dispositivo non valido se il dispositivo è già aperto e non può essere condivisione.<br/> I dispositivi MCISEQ Sequencer e MCIWAVE non supportano i file condivisi.<br/> |
| style child           | Apre una finestra con uno stile di finestra figlio.                                                                                                                                                                                                                                                                                                                            |
| stile sovrapposto      | Apre una finestra con uno stile di finestra sovrapposta.                                                                                                                                                                                                                                                                                                                      |
| popup di stile           | Apre una finestra con uno stile di finestra popup.                                                                                                                                                                                                                                                                                                                           |
| tipo *di stile di \_ stile*   | Indica uno stile di finestra.                                                                                                                                                                                                                                                                                                                                            |
| tipo *di \_ dispositivo*   | Specifica il tipo di dispositivo di un file.                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

MCI riserva "cdaudio" per il tipo di dispositivo audio CD, "videodisc" per il tipo di dispositivo videodisc, "sequencer" per il tipo di dispositivo sequencer MIDI, "AVIVideo" per il tipo di dispositivo video digitale e "waveaudio" per il tipo di dispositivo waveform-audio.

In alternativa al flag "type", MCI può selezionare il dispositivo in base all'estensione usata dal file, come registrato nel Registro di sistema o nella sezione mci extension del \[ \] file SYSTEM.INI.

McI può aprire i file AVI usando un puntatore a interfaccia file o un puntatore a interfaccia di flusso. Per aprire un file usando uno dei due tipi di puntatore a interfaccia, specificare un simbolo di at (@) seguito dal puntatore di interfaccia al posto del nome del file o del dispositivo per *il parametro lpszDevice.* Per altre informazioni sulle interfacce di file e di flusso, vedere ["Funzioni e macro AVIFile".](avifile-functions-and-macros.md)

Il comando seguente apre il dispositivo "mysound".

``` syntax
open new type waveaudio alias mysound buffer 6
```

Con il nome di dispositivo "new", il driver waveform prepara una nuova risorsa waveform. Il comando assegna l'alias del dispositivo "mysound" e specifica un buffer di 6 secondi.

È possibile eliminare il flag "type" se si combina il nome del dispositivo con il nome del file. McI riconosce questa combinazione quando si usa la sintassi seguente:

*nome \_ dispositivo* ! *nome \_ dell'elemento*

Il punto esclamativo separa il nome del dispositivo dal nome del file. Il punto esclamativo non deve essere delimitato da spazi vuoti.

Nell'esempio seguente viene aperto RIGHT. File WAV che usa il dispositivo "waveaudio".

``` syntax
open waveaudio!right.wav
```

Il driver MCIWAVE richiede un dispositivo audio waveform asincrono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Corecrt \_ io.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> </dl>

 


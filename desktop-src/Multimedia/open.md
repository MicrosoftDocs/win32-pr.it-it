---
title: comando Apri (Corecrt \_ io. h)
description: Il comando Apri Inizializza un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- Apri comando Windows Multimedia
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
ms.openlocfilehash: ac8d31f1806a9c12f764c679548564aa053c3041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741431"
---
# <a name="open-command"></a>Apri comando

Il comando Apri Inizializza un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI o di un driver di dispositivo. Può essere un nome di dispositivo (come indicato nel registro di sistema o il file di SYSTEM.INI) o il nome del file del driver di dispositivo. Se si specifica il nome del file del driver di dispositivo, è possibile includere facoltativamente. Estensione DRV, ma è consigliabile non includere il percorso del file.

</dd> <dt>

<span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*
</dt> <dd>

Flag che identifica gli elementi da inizializzare. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Apri** e i flag utilizzati da ogni tipo.



| Valore        | Significato                                                        | Significato                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| cdaudio      | alias del *dispositivo \_ alias* condivisibile                                  | Digitare *il \_ tipo di dispositivo*                                                             |
| digitalvideo | alias *Device \_ aliaselementname* Nostatic *HWND* padre condivisibile | tipo *di tipo di \_* *dispositivo \_* stile di popup stile sovrapposto stile figlio stile |
| overlay      | alias *dispositivo \_* *alias padre* alias del dispositivo figlio stile condivisibile         | tipo di tipo di dispositivo *tipo \_ stile* di *popup \_* stile sovrapposto stile             |
| sequencer    | alias del *dispositivo \_ alias* condivisibile                                 | Digitare *il \_ tipo di dispositivo*                                                             |
| VCR          | alias del *dispositivo \_ alias* condivisibile                                  | Digitare *il \_ tipo di dispositivo*                                                             |
| videodisk    | alias del *dispositivo \_ alias* condivisibile                                  | Digitare *il \_ tipo di dispositivo*                                                             |
| WaveAudio    | *\_ dimensioni del buffer* di alias del *dispositivo \_* alias                     | tipo di *dispositivo \_* condivisibile                                                    |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszOpenFlags** e i relativi significati.



| Valore                 | Significato                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| alias *dispositivo \_* alias | Specifica un nome alternativo per il dispositivo specificato. Se specificato, deve essere usato come ID del *dispositivo \_* nei comandi successivi.                                                                                                                                                                                                                                          |
| *ElementName*         | Specifica il nome dell'elemento del dispositivo (file) caricato all'apertura del dispositivo.                                                                                                                                                                                                                                                                                        |
| *\_ dimensioni buffer* buffer | Imposta la dimensione, in secondi, del buffer utilizzato dal dispositivo Waveform-Audio. Le dimensioni predefinite del buffer vengono impostate quando il dispositivo Waveform-Audio è installato o configurato. In genere, le dimensioni del buffer sono impostate su 4 secondi. Con il dispositivo MCIWAVE, le dimensioni minime sono pari a 2 secondi e le dimensioni massime sono di 9 secondi.                                                |
| *HWND* padre         | Specifica l'handle della finestra padre.                                                                                                                                                                                                                                                                                                                    |
| condivisibile              | Inizializza il dispositivo o il file come condivisibile. I successivi tentativi di apertura del dispositivo o del file avranno esito negativo a meno che non si specifichi "condivisibile" sia nei comandi **aperti** originali che in quelli successivi. MCI restituisce un errore di dispositivo non valido se il dispositivo è già aperto e non condivisibile.<br/> I dispositivi MCISEQ sequencer e MCIWAVE non supportano i file condivisi.<br/> |
| figlio stile           | Apre una finestra con uno stile finestra figlio.                                                                                                                                                                                                                                                                                                                            |
| stile sovrapposto      | Apre una finestra con uno stile di finestra sovrapposto.                                                                                                                                                                                                                                                                                                                      |
| popup stile           | Apre una finestra con uno stile finestra popup.                                                                                                                                                                                                                                                                                                                           |
| *\_ tipo stile*   | Indica uno stile della finestra.                                                                                                                                                                                                                                                                                                                                            |
| Digitare *il \_ tipo di dispositivo*   | Specifica il tipo di dispositivo di un file.                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

MCI riserva "CDAudio" per il tipo di dispositivo audio CD "videodisco" per il tipo di dispositivo videodisco, "Sequencer" per il tipo di dispositivo MIDI sequencer, "AVIVideo" per il tipo di dispositivo Digital-video e "WaveAudio" per il tipo di dispositivo Waveform-Audio.

In alternativa al flag "Type", MCI può selezionare il dispositivo in base all'estensione usata dal file, come registrato nel registro di sistema o nella \[ sezione relativa all'estensione MCI \] del file di SYSTEM.INI.

MCI può aprire i file AVI usando un puntatore a interfaccia di file o un puntatore a interfaccia di flusso. Per aprire un file usando entrambi i tipi di puntatore a interfaccia, specificare un simbolo di chiocciola (@) seguito dal puntatore a interfaccia al posto del nome del file o del dispositivo per il parametro *lpszDevice* . Per ulteriori informazioni sulle interfacce di file e di flusso, vedere " [funzioni e macro di avifile](avifile-functions-and-macros.md)".

Il comando che segue apre il dispositivo "audio".

``` syntax
open new type waveaudio alias mysound buffer 6
```

Con il nome del dispositivo "nuovo", il driver della forma d'onda prepara una nuova risorsa di forma d'onda. Il comando assegna l'alias del dispositivo "audio" e specifica un buffer di 6 secondi.

È possibile eliminare il flag "Type" Se si combina il nome del dispositivo con il nome file. MCI riconosce questa combinazione quando si usa la sintassi seguente:

*\_ nome dispositivo* . *\_nome elemento*

Il punto esclamativo separa il nome del dispositivo dal nome del file. Il punto esclamativo non deve essere delimitato da spazi vuoti.

Nell'esempio seguente viene aperto il diritto. File WAV che usa il dispositivo "WaveAudio".

``` syntax
open waveaudio!right.wav
```

Il driver MCIWAVE richiede un dispositivo audio e una forma d'onda asincrona.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>\_Io. h Corecrt</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> </dl>

 


---
title: Metodo Speak
description: Metodo Speak
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8798809dc4cdfa38438bee2fa9449f879871e4018b0e6b046d95a73583b03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475343"
---
# <a name="speak-method"></a>Metodo Speak

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Pronuncia il testo o il file audio specificato per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Speak_ *  \[ *Text* \] , \[ *URL*\]



| Parte   | Descrizione                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Text* | facoltativo. Stringa che specifica le informazioni del carattere.                                                                                                                                                                                                   |
| *Url*  | facoltativo. Espressione stringa che specifica il percorso di un file audio (. WAV o . formato LWV). Il percorso può essere specificato come file (inclusa una specifica di percorso UNC) o URL (quando i dati di animazione dei caratteri vengono recuperati anche tramite il protocollo HTTP). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Anche se *i parametri Text* e *Url* sono facoltativi, è necessario specificare uno di essi. Per usare questo metodo con un carattere configurato per parlare solo nel fumetto della parola o usando un motore di sintesi vocale (TTS), è sufficiente specificare il *parametro Text.* Includere uno spazio tra le parole per definire le interruzioni di parola appropriate nel fumetto, anche per le lingue che in genere non includono spazi.

È anche possibile includere caratteri a barre verticali ( ) nel parametro Text per designare stringhe alternative, in modo che il server scegli in modo casuale una stringa diversa ogni volta che \| elabora il metodo. 

Il supporto dei caratteri dell'output TTS viene definito quando il carattere viene compilato usando l'editor di caratteri di Microsoft Agent. Per generare l'output TTS, è necessario che sia già installato un motore TTS compatibile prima di chiamare questo metodo. Per altre informazioni, vedere [Accesso ai servizi voce](accessing-speech-services.md).

Se si usa il file audio registrato (. WAV o . Solo formato LWV) per il carattere, specificare il percorso del file nel *parametro Url.* Questa specifica di file può includere un percorso locale (assoluto o relativo) o un percorso UNC (Universal Naming Convention). Il nome file non può includere caratteri non inclusi nella tabella codici 1252 degli Stati Uniti. Tuttavia, se si usa il protocollo HTTP per accedere ai dati di animazione dei caratteri, usare il [**metodo Get**](get-method.md) per caricare l'animazione prima di chiamare il **metodo Speak.** Per informazioni sulla creatività, vedere Uso di [Microsoft Linguistic Information Sound Editing Tool.](using-the-microsoft-linguistic-information-sound-editing-tool.md) File LWV.

Quando si usa l'output del file audio registrato, è comunque possibile usare il parametro *Text* per specificare le parole visualizzate nel fumetto delle parole del carattere. Tuttavia, se si specifica un file audio linguisticamente avanzato (. LWV) per il *parametro Url* e non specificano testo per il fumetto, il *parametro Text* usa il testo archiviato nel file.

È anche possibile variare i parametri dell'output vocale con tag speciali inclusi nel *parametro* Text. Per altre informazioni, vedere [Tag di output del riconoscimento vocale di Microsoft Agent.](microsoft-agent-speech-output-tags.md)

Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito [**un oggetto Request.**](/windows/desktop/lwef/the-request-object) È possibile usarlo per sincronizzare altre parti del codice con l'output parlato del carattere, come nell'esempio seguente:


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here it is.")
...
   Sub Agent1_RequestComplete (ByVal Request as Object)
   ' Make certain the request exists
   If SpeakRequest Not Nothing Then
      ' See if it was this request
      If Request = SpeakRequest Then
         ' Display the message box 
         Msgbox "Ta da!"
      End If
   End If
   End Sub
```



È anche possibile usare un [**oggetto Request**](/windows/desktop/lwef/the-request-object) per verificare la presenza di determinate condizioni di errore. Ad esempio, se si usa il metodo **Speak** per parlare e non è  installato un [](status-property.md) motore TTS compatibile, il server imposta la proprietà Status dell'oggetto Request su "failed" con la relativa proprietà [**Description**](description-property.md) su "Class not registered" o "Unknown or object returned error". Per determinare se è installato un motore TTS, usare la [**proprietà TTSModeID.**](ttsmodeid-property.md)

Analogamente, se il carattere tenta di pronunciare un file audio e se il file non è stato caricato o [](/windows/desktop/lwef/the-request-object) si verifica un problema con il dispositivo audio, il server imposta anche la proprietà [**Status**](status-property.md) dell'oggetto Request su "failed" con un numero di codice di errore appropriato.

È anche possibile includere tag voce segnalibro nel testo Parla per sincronizzare il codice:


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here \mrk=100\it is.")
...
   Sub Agent1_Bookmark (ByVal BookmarkID As Long)
   If BookmarkID = 100 Then
      ' Display the message box 
         Msgbox "Tada!"
      End If
   End Sub
```



Per altre informazioni sul tag di riconoscimento vocale segnalibro, vedere [Tag di output del riconoscimento vocale.](mrk-tag.md)

Il **metodo Speak** usa l'ultima azione riprodotta per determinare l'animazione parlata da riprodurre. Ad esempio, se il comando **Speak** è stato preceduto da [**play**](play-method.md) "**GestureRight**", il server riprodurrà **GestureRight** e quindi l'animazione **GestureRight** speaking. Se l'ultima animazione riprodotta non ha un'animazione parlata, Agent riproduce l'animazione assegnata allo stato **Speaking del** carattere.

Se si chiama **Parla** e il canale audio è occupato, l'output audio del carattere non verrà ascoltato, ma il testo verrà visualizzato nel fumetto della parola.

L'interruzione automatica delle parole di Agent nel fumetto di parole interrompe le parole usando spazi vuoti,ad esempio Spazio o Tab. Tuttavia, se non è possibile, potrebbe interrompere una parola per adattarla al fumetto. In lingue come il giapponese, il cinese e il tailandese, in cui gli spazi non vengono usati per interrompere le parole, inserire uno spazio unicode a larghezza zero (0x200B) tra i caratteri per definire interruzioni di parola logiche.

> [!Note]  
> Anche la proprietà [**Enabled del fumetto**](enabled-property.md) deve essere **Impostata** su True per visualizzare il testo.

 

> [!Note]  
> Impostare l'ID lingua del carattere ( impostando **languageID** del carattere prima di usare il **metodo Speak** per garantire la visualizzazione del testo appropriato all'interno del fumetto della parola.

 

## <a name="see-also"></a>Vedere anche

[**Evento Bookmark,**](bookmark-event.md) [**evento RequestStart,**](requeststart-event.md) [**evento RequestComplete**](requestcomplete-event.md)


 

 
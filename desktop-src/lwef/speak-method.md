---
title: Speak (metodo)
description: Speak (metodo)
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88792a53fac80c68154f938e91fb9bfe63b2b8e3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472923"
---
# <a name="speak-method"></a>Speak (metodo)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Pronuncia il testo o il file audio specificato per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). Pronuncia* *  \[ *testo* \] , \[ *URL*\]



| Parte   | Descrizione                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Text* | facoltativo. Stringa che specifica l'elemento indicato dal carattere.                                                                                                                                                                                                   |
| *Url*  | facoltativo. Espressione stringa che specifica il percorso di un file audio (. WAV o. Formato LWV). Il percorso può essere specificato come file (inclusa una specifica del percorso UNC) o un URL (quando vengono recuperati anche i dati di animazione dei caratteri tramite il protocollo HTTP). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Sebbene i parametri *Text* e *URL* siano facoltativi, è necessario specificare uno di essi. Per usare questo metodo con un carattere configurato per parlare solo nella relativa bolla di parola o usando un motore di sintesi vocale, è sufficiente fornire il parametro di *testo* . Includere uno spazio tra le parole per definire le interruzioni di parola appropriate nel fumetto di parole, anche per le lingue in cui non sono tradizionalmente inclusi gli spazi.

È anche possibile includere caratteri barra verticale ( \| ) nel parametro di *testo* per designare stringhe alternative, in modo che il server scelga in modo casuale una stringa diversa ogni volta che elabora il metodo.

Il supporto dei caratteri dell'output TTS viene definito quando il carattere viene compilato tramite l'editor dei caratteri di Microsoft Agent. Per generare l'output TTS, è necessario che sia già installato un motore TTS compatibile prima di chiamare questo metodo. Per ulteriori informazioni, vedere [accesso ai servizi di riconoscimento vocale](accessing-speech-services.md).

Se si usa il file audio registrato (. WAV o. Output del formato LWV) per il carattere, specificare il percorso del file nel parametro *URL* . Questa specifica di file può includere un percorso locale (assoluto o relativo) o UNC (Universal Naming Convention). Il nome file non può includere caratteri non inclusi nella tabella codici degli Stati Uniti 1252. Tuttavia, se si utilizza il protocollo HTTP per accedere ai dati di animazione dei caratteri, utilizzare il metodo [**Get**](get-method.md) per caricare l'animazione prima di chiamare il metodo **Speak** . Per informazioni su Creative, vedere [uso dello strumento di modifica audio per informazioni linguistiche di Microsoft](using-the-microsoft-linguistic-information-sound-editing-tool.md) . File LWV.

Quando si usa l'output del file audio registrato, è comunque possibile usare il parametro *Text* per specificare le parole visualizzate nell'aerostato di parole del carattere. Tuttavia, se si specifica un file audio con funzionalità avanzate linguisticamente (. LWV) per il parametro *URL* e non specificare il testo per la parola Balloon, il parametro *Text* usa il testo archiviato nel file.

È anche possibile variare i parametri dell'output vocale con tag speciali inclusi nel parametro di *testo* . Per ulteriori informazioni, vedere [tag di output di sintesi vocale di Microsoft Agent](microsoft-agent-speech-output-tags.md).

Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) . È possibile usarlo per sincronizzare altre parti del codice con l'output parlato del carattere, come nell'esempio seguente:


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



È anche possibile usare un oggetto [**Request**](/windows/desktop/lwef/the-request-object) per verificare la presenza di determinate condizioni di errore. Se, ad esempio, si usa il metodo **Speak** per parlare e non è installato un motore TTS compatibile, il server imposta la proprietà [**status**](status-property.md) dell'oggetto **Request** su "failed" con la relativa proprietà [**Description**](description-property.md) su "classe non registrata" o "errore sconosciuto o restituito oggetto". Per determinare se è installato un motore TTS, utilizzare la proprietà [**TTSModeID**](ttsmodeid-property.md) .

Analogamente, se il carattere tenta di pronunciare un file audio e se il file non è stato caricato o se si verifica un problema con il dispositivo audio, il server imposta anche la proprietà [**status**](status-property.md) dell'oggetto [**Request**](/windows/desktop/lwef/the-request-object) su "failed" con un numero di codice di errore appropriato.

Per sincronizzare il codice, è anche possibile includere tag di riconoscimento vocale nel testo Speak:


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



Per altre informazioni sul tag vocale del segnalibro, vedere [tag di output vocale](mrk-tag.md).

Il metodo **Speak** usa l'ultima azione riprodotta per determinare quale animazione di pronuncia riprodurre. Se, ad esempio, il comando **Speak** è stato preceduto da [**Play**](play-method.md) "**GestureRight**", il server eseguirà **GestureRight** e quindi l'animazione **GestureRight** Speaking. Se l'ultima animazione riprodotta non ha un'animazione di pronuncia, Agent riproduce l'animazione assegnata allo stato di **pronuncia** del carattere.

Se si chiama **Speak** e il canale audio è occupato, l'output audio del carattere non verrà udito, ma il testo verrà visualizzato nella parola Balloon.

Il Word Breaking automatico dell'agente in Word Balloon interrompe le parole usando spazi vuoti (ad esempio, spazio o tabulazione). Tuttavia, se non è possibile, potrebbe interrompere una parola per adattarla al fumetto. In lingue quali giapponese, cinese e tailandese, in cui gli spazi non vengono usati per interrompere le parole, inserire un carattere di spazio a larghezza zero Unicode (0x200B) tra i caratteri per definire interruzioni di parola logiche.

> [!Note]  
> Anche la proprietà [**Enabled**](enabled-property.md) del fumetto di Word deve essere **true** per visualizzare il testo.

 

> [!Note]  
> Impostare l'ID lingua del carattere (impostando il **LanguageID** del carattere prima di usare il metodo **Speak** per garantire la visualizzazione del testo appropriata all'interno del fumetto di Word.

 

## <a name="see-also"></a>Vedere anche

[**Evento segnalibro**](bookmark-event.md), [**evento RequestStart**](requeststart-event.md), [**evento RequestComplete**](requestcomplete-event.md)


 

 
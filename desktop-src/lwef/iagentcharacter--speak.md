---
title: IAgentCharacter parla
description: IAgentCharacter parla
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e290ab9037ee6f261445d4dfd00a206213cd26
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516768"
---
# <a name="iagentcharacterspeak"></a>IAgentCharacter:: Speak

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

Pronuncia il testo o il file audio.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

Testo da pronunciare per il carattere.

</dd> <dt>

<span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*
</dt> <dd>

URL (o specifica del file) di un file audio da usare per l'output parlato. Può trattarsi di un file audio standard (. WAV) o file audio con funzionalità avanzate linguisticamente (. LWV).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID della richiesta [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) .

</dd> </dl>

Per usare questo metodo con un carattere configurato per parlare usando un motore di sintesi vocale; è sufficiente specificare il parametro *bszText* . È possibile includere caratteri barra verticale ( \| ) nel parametro *bszText* per designare stringhe alternative, in modo che ogni volta che il server elabora il metodo, scelga in modo casuale una stringa diversa. Il supporto dell'output TTS viene definito quando il carattere viene compilato mediante l'editor dei caratteri di Microsoft Agent.

Se si vuole usare l'output del file audio per il carattere, specificare il percorso del file nel parametro *bszURL* . Quando si utilizza il protocollo HTTP per scaricare un file audio, utilizzare il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per garantire la disponibilità del file prima di utilizzare questo metodo. È possibile usare il parametro *bszText* per specificare le parole visualizzate nell'aerostato di parola del carattere. Se si specifica un file audio con funzionalità avanzate linguisticamente (. LWV) per il parametro *bszURL* e non specificare il testo, il parametro *bszText* usa il testo archiviato nel file.

Il metodo [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) usa l'ultima animazione riprodotta per determinare quale animazione di pronuncia riprodurre. Se, ad esempio, si precede il comando **Speak** con [**IAgentCharacter::P Lay**](iagentcharacter--play.md) "**GestureRight**", il server riprodurrà **GestureRight** e quindi l'animazione **GestureRight** Speaking. Se l'ultima animazione riprodotta non ha un'animazione di pronuncia, Microsoft Agent esegue l'animazione assegnata allo stato di **pronuncia** del carattere.

Se si chiama [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) e il canale audio è occupato, l'output audio del carattere non verrà udito, ma il testo verrà visualizzato nella parola Balloon. Anche la proprietà [Enabled](enabled-property.md) del fumetto di Word deve essere **true** per visualizzare il testo.

Il Word Breaking automatico dell'agente Microsoft in Word Balloon interrompe le parole usando spazi vuoti (ad esempio, spazio e tabulazione). Tuttavia, potrebbe suddividere una parola in modo da adattarla anche al fumetto. In lingue quali giapponese, cinese e tailandese, in cui gli spazi non vengono usati per interrompere le parole, inserire un carattere di spazio a larghezza zero Unicode (0x200B) tra i caratteri per definire interruzioni di parola logiche.

> [!Note]  
> Impostare l'ID lingua del carattere (usando [**IAgentCharacterEx:: SetLanguageID**](iagentcharacterex--setlanguageid.md) prima di usare il metodo [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) per garantire la visualizzazione del testo appropriata all'interno del fumetto di Word.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::P Lay**](iagentcharacter--play.md), [**IAgentBalloon:: GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::P ripare**](iagentcharacter--prepare.md)


 

 
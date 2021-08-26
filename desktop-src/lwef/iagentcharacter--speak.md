---
title: IAgentCharacter Speak
description: IAgentCharacter Speak
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693b40a00b34173976410391249d3fac1a7f0684e34a6e2ae82afbd8b8169ce0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014211"
---
# <a name="iagentcharacterspeak"></a>IAgentCharacter::Speak

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

Pronuncia il file di testo o audio.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

Testo che il carattere deve pronunciare.

</dd> <dt>

<span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*
</dt> <dd>

URL (o specifica del file) di un file audio da usare per l'output parlato. Può trattarsi di un file audio standard (. WAV) o file audio linguisticamente avanzato (. LWV).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID [**richiesta Speak.**](/windows/desktop/lwef/iagentcharacter--speak)

</dd> </dl>

Per usare questo metodo con un carattere configurato per parlare usando un motore di sintesi vocale (TTS). è sufficiente specificare il *parametro bszText.* È possibile includere caratteri barra verticali ( ) nel parametro \| *bszText* per designare stringhe alternative, in modo che ogni volta che il server elabora il metodo, scegli in modo casuale una stringa diversa. Il supporto dell'output TTS viene definito quando il carattere viene compilato usando l'editor di caratteri di Microsoft Agent.

Se si vuole usare l'output del file audio per il carattere, specificare il percorso del file nel *parametro bszURL.* Quando si usa il protocollo HTTP per scaricare un file audio, usare il [**metodo Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per garantire la disponibilità del file prima di usare questo metodo. È possibile usare il *parametro bszText* per specificare le parole visualizzate nel fumetto delle parole del carattere. Se si specifica un file audio linguisticamente avanzato (. LWV) per *il parametro bszURL* e non specificano testo, il *parametro bszText* usa il testo archiviato nel file.

Il [**metodo Speak**](/windows/desktop/lwef/iagentcharacter--speak) usa l'ultima animazione riprodotta per determinare l'animazione parlata da riprodurre. Ad esempio, se si precede il comando **Speak** con [**un oggetto IAgentCharacter::P lay**](iagentcharacter--play.md) "**GestureRight**", il server riprodurrà **GestureRight** e quindi l'animazione **GestureRight** speaking. Se l'ultima animazione riprodotta non ha un'animazione parlata, Microsoft Agent riproduce l'animazione assegnata allo stato **Speaking del** carattere.

Se si chiama [**Parla**](/windows/desktop/lwef/iagentcharacter--speak) e il canale audio è occupato, l'output audio del carattere non verrà ascoltato, ma il testo verrà visualizzato nel fumetto della parola. Anche la proprietà Enabled del [fumetto](enabled-property.md) deve essere **Impostata** su True per visualizzare il testo.

L'interruzione automatica delle parole di Microsoft Agent nel fumetto di parole, interrompe le parole usando spazi vuoti (ad esempio, spazio e tabulazione). Tuttavia, può anche interrompere una parola per adattarla al fumetto. In lingue come il giapponese, il cinese e il tailandese, in cui gli spazi non vengono usati per interrompere le parole, inserire uno spazio unicode a larghezza zero (0x200B) tra i caratteri per definire interruzioni di parola logiche.

> [!Note]  
> Impostare l'ID lingua del carattere (usando [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) prima di usare il [**metodo Speak**](/windows/desktop/lwef/iagentcharacter--speak) per garantire la visualizzazione del testo appropriato all'interno del fumetto delle parole.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::P lay,**](iagentcharacter--play.md) [**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::P repare**](iagentcharacter--prepare.md)


 

 
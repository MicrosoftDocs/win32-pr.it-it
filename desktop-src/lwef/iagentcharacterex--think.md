---
title: IAgentCharacterEx think
description: IAgentCharacterEx think
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd1bedfc2665c80d522ccb38c7c3073580136db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046648"
---
# <a name="iagentcharacterexthink"></a>IAgentCharacterEx:: Think

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

Consente di visualizzare il testo del fumetto con il testo specificato.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

Testo da visualizzare nel fumetto di pensiero del carattere.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID della richiesta di **interazione** .

</dd> </dl>

Come il metodo [**IAgentCharacter:: Speak**](iagentcharacter--speak.md) , il metodo **think** è una richiesta in coda che Visualizza il testo in un fumetto di Word, ad eccezione del fatto che i pensieri vengono visualizzati in un fumetto di pensiero speciale. Il fumetto di pensiero supporta solo il tag di controllo vocale segnalibro (**\\ MRK**) e ignora tutti gli altri tag di controllo vocale. A differenza di **IAgentCharacter:: Speak**, il metodo **think** non modifica lo stato di animazione del carattere.

Le impostazioni di [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) si applicano anche allo stile dell'aspetto del fumetto di riflessione. Ad esempio, è necessario che la proprietà [**Enabled**](enabled-property.md) del fumetto sia **valida** anche per il testo da visualizzare.

Il Word Breaking automatico dell'agente Microsoft in Word Balloon interrompe le parole usando spazi vuoti (ad esempio, spazio e tabulazione). Tuttavia, potrebbe suddividere una parola in modo da adattarla anche al fumetto. In lingue quali giapponese, cinese e tailandese, in cui gli spazi non vengono usati per interrompere le parole, inserire un carattere di spazio a larghezza zero Unicode (0x200B) tra i caratteri per definire interruzioni di parola logiche.

> [!Note]  
> Impostare l'ID lingua del carattere (usando [**IAgentCharacterEx:: SetLanguageID**](iagentcharacterex--setlanguageid.md) prima di usare il metodo [**IAgentCharacter:: Speak**](iagentcharacter--speak.md) per garantire la visualizzazione del testo appropriata all'interno del fumetto di Word.

 

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon:: GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx:: Sestyle**](iagentballoonex--setstyle.md), [**IAgentCharacter:: Speak**](iagentcharacter--speak.md)


 

 
---
title: IAgentCharacterEx Think
description: IAgentCharacterEx Think
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a513a070104605df0cf3e0e722852a2b68d5845f4bcdb1ef6073954b3f9a18c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105439"
---
# <a name="iagentcharacterexthink"></a>IAgentCharacterEx::Think

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

Visualizza il fumetto delle parole di pensare del carattere con il testo specificato.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

Testo da visualizzare nel fumetto di idea del carattere.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID **richiesta think.**

</dd> </dl>

Analogamente al [**metodo IAgentCharacter::Speak,**](iagentcharacter--speak.md) il metodo **Think** è una richiesta in coda che visualizza il testo in un fumetto di parole, ad eccezione del fatto che le opinioni vengono visualizzate in un fumetto di idea speciale. Il balloon di riconoscimento vocale supporta solo il tag bookmark speech control **\\ (Mrk)** e ignora qualsiasi altro tag di controllo vocale. A **differenza di IAgentCharacter::Speak,** il **metodo Think** non modifica lo stato di animazione del carattere.

Le [**impostazioni di IAgentBalloon**](/windows/desktop/lwef/iagentballoon) si applicano anche allo stile di aspetto del fumetto di pensare. Ad esempio, anche la proprietà [**Enabled del**](enabled-property.md) balloon deve essere **True** per il testo da visualizzare.

Il word breaking automatico di Microsoft Agent nel fumetto delle parole interrompe le parole usando spazi vuoti, ad esempio spazi e tabulazioni. Tuttavia, potrebbe anche interrompere una parola per adattarsi al fumetto. In lingue come il giapponese, il cinese e il thai, in cui gli spazi non vengono usati per interrompere le parole, inserire uno spazio unicode di larghezza zero (0x200B) tra i caratteri per definire interruzioni di parola logiche.

> [!Note]  
> Impostare l'ID lingua del carattere (usando [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) prima di usare il [**metodo IAgentCharacter::Speak**](iagentcharacter--speak.md) per garantire la visualizzazione del testo appropriata all'interno del fumetto di parole.

 

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md)


 

 
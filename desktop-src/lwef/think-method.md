---
title: Metodo think
description: Metodo think
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a896c499e11aeaf50bfe9adc82a8330e61fc693
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872426"
---
# <a name="think-method"></a>Metodo think

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Consente di visualizzare il testo specificato per il carattere specificato in un fumetto di parola "pensata".

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *").* *  \[ *Testo* interazione\]



| Parte   | Descrizione                                                       |
|--------|-------------------------------------------------------------------|
| *Text* | facoltativo. Stringa che specifica l'output del pensiero del carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Analogamente al metodo [**Speak**](speak-method.md) , il metodo **think** è una richiesta in coda che Visualizza il testo in un fumetto di Word, ad eccezione del fatto che il fumetto **think** Word differisce visivamente. Inoltre, il fumetto supporta solo il tag di controllo vocale segnalibro (**\\ MRK**) e ignora tutti gli altri tag di controllo vocale. Diversamente da **Speak**, il metodo **think** non modifica lo stato di animazione del carattere.

Le proprietà dell'oggetto [**Balloon**](/windows/desktop/lwef/the-balloon-object) influiscono sull'output dei metodi [**Speak**](speak-method.md) e **think** . La proprietà [**Enabled**](enabled-property.md) dell'oggetto **Balloon** , ad esempio, deve essere **true** per visualizzare il testo.

Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) . Inoltre, se il file non è stato caricato, il server imposta la proprietà [**status**](status-property.md) dell'oggetto **richiesta** su "failed" con un numero di codice di errore appropriato.

Il Word Breaking automatico dell'agente in Word Balloon interrompe le parole usando spazi vuoti (ad esempio, spazio o tabulazione). Tuttavia, se non è possibile, potrebbe interrompere una parola per adattarla al fumetto. In lingue quali giapponese, cinese e tailandese, in cui gli spazi non vengono usati per interrompere le parole, inserire un carattere di spazio a larghezza zero Unicode (0x200B) tra i caratteri per definire interruzioni di parola logiche.

> [!Note]  
> Impostare l'ID lingua del carattere prima di utilizzare il metodo [**Speak**](speak-method.md) per garantire la visualizzazione del testo appropriata all'interno del fumetto di Word.

 

 

 
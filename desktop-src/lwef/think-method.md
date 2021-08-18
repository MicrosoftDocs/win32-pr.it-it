---
title: Metodo Think
description: Metodo Think
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c535912962a51961ae3f88f5cca412a55ecfa27506442aa78274fe697f2d7a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975511"
---
# <a name="think-method"></a>Metodo Think

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Visualizza il testo specificato per il carattere specificato in un fumetto di parole "pensato".

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Testo_ *  \[ *di think*\]



| Parte   | Descrizione                                                       |
|--------|-------------------------------------------------------------------|
| *Text* | facoltativo. Stringa che specifica l'output di riflessione del carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Analogamente al [**metodo Speak,**](speak-method.md) il **metodo Think** è una richiesta in coda che visualizza testo in un fumetto di parole, ad eccezione del fatto che il fumetto **think** word differisce visivamente. Inoltre, il fumetto supporta solo il tag di controllo vocale Segnalibro (**\\ Mrk**) e ignora eventuali altri tag di controllo voce. A **differenza di Speak,** **il metodo Think** non modifica lo stato di animazione del carattere.

Le [**proprietà dell'oggetto**](/windows/desktop/lwef/the-balloon-object) Balloon influiscono sull'output dei [**metodi Speak**](speak-method.md) e **Think.** Ad esempio, la **proprietà Enabled** dell'oggetto [**Balloon**](enabled-property.md) deve essere **Impostata** su True per visualizzare il testo.

Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito [**un oggetto Request.**](/windows/desktop/lwef/the-request-object) Inoltre, se il file non è stato caricato, il server imposta la proprietà [**Status**](status-property.md) dell'oggetto **Request** su "failed" con un numero di codice di errore appropriato.

L'interruzione automatica delle parole di Agent nel fumetto di parole interrompe le parole usando spazi vuoti, ad esempio Spazio o Tab. Tuttavia, se non è possibile, potrebbe interrompere una parola per adattarla al fumetto. In lingue come il giapponese, il cinese e il tailandese in cui gli spazi non vengono usati per interrompere le parole, inserire uno spazio unicode a larghezza zero (0x200B) tra i caratteri per definire interruzioni di parola logiche.

> [!Note]  
> Impostare l'ID lingua del carattere prima di usare il [**metodo Speak**](speak-method.md) per garantire la visualizzazione del testo appropriato all'interno del fumetto della parola.

 

 

 
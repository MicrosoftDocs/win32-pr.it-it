---
title: Proprietà Visible (oggetto Balloon)
description: Visible (proprietà)
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba58993a3328a4c99dbe7da43b43460f6048bf57
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047665"
---
# <a name="visible-property-balloon-object"></a>Proprietà Visible (oggetto Balloon)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta l'impostazione visibile per la parola Balloon per il carattere specificato.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agente ***. Caratteri (**"* CharacterID *" * *).* *  \[  =  *Valore booleano* Balloon. Visible\]



| Parte      | Descrizione                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se la parola Balloon è visibile.<br/> Valore **true** Il fumetto è visibile.<br/> **False** Il fumetto è nascosto.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si segue una chiamata [**Speak**](speak-method.md) o [**think**](think-method.md) con un'istruzione per tentare di modificare la proprietà del fumetto, potrebbe non influire sullo stato visibile del fumetto perché la chiamata **Speak** o **think** viene accodata, ma la chiamata non imposta lo stato visibile del fumetto. Pertanto, impostare questo valore solo quando nessuna chiamata a **Speak** o **think** si trova nella coda del carattere.

Se si tenta di impostare questa proprietà quando il carattere è in conversazione, lo spostare o il trascinamento, l'impostazione della proprietà non diventa effettiva fino al completamento dell'operazione precedente.

La chiamata ai metodi [**Speak**](speak-method.md) e [**think**](think-method.md) rende automaticamente visibile il fumetto, impostando la proprietà [**Visible**](visible-property.md) su **true**. Se la proprietà Nascondi automaticamente del fumetto del carattere è abilitata, il fumetto viene nascosto automaticamente dopo la pronuncia del testo di output. Quando si fa clic o si trascina un carattere che non è in corso di conversazione, il fumetto viene nascosto automaticamente anche se l'impostazione Nascondi automaticamente è disabilitata. È possibile modificare l'impostazione Nascondi automaticamente del carattere usando la proprietà [**Style**](style-property.md) del fumetto.

### <a name="see-also"></a>Vedere anche

[**Style (proprietà)**](style-property.md)


 

 






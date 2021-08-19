---
title: Proprietà Visible (oggetto Balloon)
description: Informazioni sulla proprietà Visible dell'oggetto Balloon, che restituisce o imposta l'impostazione visibile per il fumetto per il carattere specificato.
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101d454f90e01ebcf31619b935d1b90512648baf33a11883b6b971c3178fb871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975481"
---
# <a name="visible-property-balloon-object"></a>Proprietà Visible (oggetto Balloon)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta l'impostazione visibile per il fumetto per il carattere specificato.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Booleano Balloon.Visible* *  \[  =  \]



| Parte      | Descrizione                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se il fumetto della parola è visibile.<br/> **True** Il fumetto è visibile.<br/> **False** Il fumetto è nascosto.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si segue una chiamata [**Speak**](speak-method.md) o Think con un'istruzione per tentare di modificare la proprietà del fumetto, potrebbe non influire sullo stato Visible del fumetto perché la chiamata **Speak** o [**Think**](think-method.md) viene accodata, ma la chiamata che imposta lo stato visibile del fumetto non lo fa.  Pertanto, impostare questo valore solo quando nessuna **chiamata Speak** o **Think** è presente nella coda del carattere.

Se si tenta di impostare questa proprietà mentre il carattere parla, si sposta o viene trascinato, l'impostazione della proprietà non ha effetto fino al completamento dell'operazione precedente.

La chiamata [**dei metodi Speak**](speak-method.md) e [**Think**](think-method.md) rende automaticamente visibile il fumetto, impostando la [**proprietà Visible**](visible-property.md) su **True.** Se la proprietà AutoHide del fumetto del carattere è abilitata, il fumetto viene automaticamente nascosto dopo la pronuncia del testo di output. Se si fa clic o si trascina un carattere che attualmente non parla, il fumetto viene nascosto automaticamente anche se l'impostazione Nascondi automaticamente è disabilitata. È possibile modificare l'impostazione AutoHide del carattere usando la proprietà [**Style del fumetto.**](style-property.md)

### <a name="see-also"></a>Vedere anche

[**Style - proprietà**](style-property.md)


 

 






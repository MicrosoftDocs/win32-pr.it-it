---
title: Proprietà Enabled (oggetto AudioOutput)
description: Proprietà Enabled
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dff9153a1aa7a6bf5346d46f43f80bf48809c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047762"
---
# <a name="enabled-property-audiooutput-object"></a>Proprietà Enabled (oggetto AudioOutput)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore booleano che indica se l'output audio (parlato) è abilitato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente * * *. AudioOutput. Enabled**



| Valore     | Descrizione                               |
|-----------|-------------------------------------------|
| **True**  | Predefinita L'output audio parlato è abilitato. |
| **False** | L'output audio parlato è disabilitato.          |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà riflette l'opzione Riproduci output audio nella pagina output della finestra delle proprietà dell'agente (Opzioni carattere avanzate). Quando la proprietà [**Enabled**](enabled-property.md) restituisce **true**, il metodo [**Speak**](speak-method.md) produce l'output audio se è installato un motore TTS compatibile o si usano file audio per l'output parlato. Quando restituisce **false**, significa che l'output vocale non è installato o è stato disabilitato dall'utente. L'impostazione della proprietà si applica a tutti i caratteri degli agenti ed è di sola lettura. il valore della proprietà può essere impostato solo dall'utente.

## <a name="see-also"></a>Vedere anche

[Evento AgentPropertyChange](agentpropertychange-event.md)


 

 





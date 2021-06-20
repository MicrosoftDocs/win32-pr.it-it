---
title: Proprietà Enabled (oggetto AudioOutput)
description: Informazioni sulla proprietà dell'oggetto Enabled AudioOutput. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807b4cadcc9a0157b4efa400dd9d0e3cb5cf21a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407344"
---
# <a name="enabled-property-audiooutput-object"></a>Proprietà Enabled (oggetto AudioOutput)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore booleano che indica se l'output audio (parlato) è abilitato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. AudioOutput.Enabled**



| Valore     | Descrizione                               |
|-----------|-------------------------------------------|
| **True**  | (Impostazione predefinita) L'output audio parlato è abilitato. |
| **False** | L'output audio parlato è disabilitato.          |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà riflette l'opzione Riproduci output audio nella pagina Output della finestra delle proprietà agente (Opzioni carattere avanzate). Quando la [**proprietà Enabled**](enabled-property.md) restituisce **True,** il metodo [**Speak**](speak-method.md) produce output audio se è installato un motore TTS compatibile o si usano file audio per l'output parlato. Quando restituisce **False,** significa che l'output vocale non è installato o è stato disabilitato dall'utente. L'impostazione della proprietà si applica a tutti i caratteri di Agent ed è di sola lettura. solo l'utente può impostare questo valore della proprietà.

## <a name="see-also"></a>Vedere anche

[Evento AgentPropertyChange](agentpropertychange-event.md)


 

 





---
title: Proprietà ListeningTip
description: Proprietà ListeningTip
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402fd970bf902f034fd6ffb713029e3a27095c8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298791"
---
# <a name="listeningtip-property"></a>Proprietà ListeningTip

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore booleano che indica l'impostazione dell'utente corrente per il suggerimento di ascolto.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agente * * *. SpeechInput.ListeningTip**



| Valore     | Descrizione                    |
|-----------|--------------------------------|
| **True**  | Il suggerimento di ascolto è abilitato.  |
| **False** | Il suggerimento di ascolto è disabilitato. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà **ListeningTip** indica se l'opzione Visualizza suggerimento in ascolto nella finestra delle proprietà di Microsoft Agent (opzioni avanzate per i caratteri) è abilitata. Quando **ListeningTip** restituisce **true** e l'input vocale è abilitato, il server Visualizza la finestra di suggerimento quando l'utente preme il tasto di attesa.

## <a name="see-also"></a>Vedere anche

[**Evento AgentPropertyChange**](agentpropertychange-event.md)


 

 





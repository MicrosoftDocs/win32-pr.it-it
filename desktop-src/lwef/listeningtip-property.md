---
title: Proprietà ListeningTip
description: Proprietà ListeningTip
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a743eb26d1e2b57d106e72d77c3774938ffe7e56ca4ba4147001d74bb99f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665441"
---
# <a name="listeningtip-property"></a>Proprietà ListeningTip

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore booleano che indica l'impostazione utente corrente per il suggerimento per l'ascolto.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agent***. SpeechInput.ListeningTip**



| Valore     | Descrizione                    |
|-----------|--------------------------------|
| **True**  | Il suggerimento per l'ascolto è abilitato.  |
| **False** | Il suggerimento per l'ascolto è disabilitato. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La **proprietà ListeningTip** indica se l'opzione Visualizza suggerimento in ascolto nella finestra delle proprietà di Microsoft Agent (Opzioni carattere avanzate) è abilitata. Quando **ListeningTip restituisce** **True** e l'input vocale è abilitato, il server visualizza la finestra del suggerimento quando l'utente preme il tasto Listening.

## <a name="see-also"></a>Vedere anche

[**Evento AgentPropertyChange**](agentpropertychange-event.md)


 

 





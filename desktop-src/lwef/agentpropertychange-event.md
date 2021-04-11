---
title: Evento AgentPropertyChange
description: Evento AgentPropertyChange
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bd643797e766543877497330a995d492f982d8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044496"
---
# <a name="agentpropertychange-event"></a>Evento AgentPropertyChange

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando l'utente modifica una proprietà nella finestra Opzioni carattere avanzate.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

Agente **secondario** *. * * * AgentPropertyChange**

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento indica quando l'utente ha modificato e applicato qualsiasi proprietà inclusa nella finestra delle opzioni dei caratteri avanzati.

Nel codice per la gestione di questo evento, è possibile eseguire una query per le impostazioni specifiche delle proprietà degli oggetti [AudioOutput](the-audiooutput-object.md) o [SpeechInput](the-speechinput-object.md) .

### <a name="see-also"></a>Vedere anche

[**Evento DefaultCharacterChange**](defaultcharacterchange-event.md)


 

 




